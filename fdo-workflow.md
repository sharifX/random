### Example workflow involving PID, PIT, DTR

![workflow](PID-workflow.png)

1. Agent (human or machine) encounters a FAIR Digital Object (FDO): 
[20.5000.1025/64ae0cf0dacb7bd20ba5](hdl.handle.net/http://hdl.handle.net/api/handles/20.5000.1025/64ae0cf0dacb7bd20ba5) 

2. Agent sends the PID to a PID service (DOI/Handle system)

http://hdl.handle.net/api/handles/20.5000.1025/64ae0cf0dacb7bd20ba5

**NOTE** We need to pay attention here which interface the agent will query. In this example, the Global Handle Server (GHS)
only returns 10320/loc and 0.TYPE/DOIPService, the typeName should be exposed here. 

Here is a a PID example from the CIMP6 datasets that exposes more elements to the GHS: 
http://hdl.handle.net/api/handles/21.14100/1d777d08-6ffe-3a8e-a191-bd01476b5345

Even though this is not using Type, it returns elements such as AGGREGATION_LEVEL, HAS_PARTS, VERSION_NUMBER, HOSTING_NODE, REPLICA_NODE that provide important context for the digital object. 


3. PID Service returns the PID Kernel Infomration (KI). 

**NOTE** We need to decide what this KI entails. Also depends on what the GHS stores. 

4. Agent parses KI. Decides what to do

5. Agent decides what to do with the FDO via DOIP/REST. Here the FDO repository comes into the play. For us this cordra (nsidr.org). 

6. Agent decides what extra information is needed for the operation. 
There are other extra information that the Agent can access which might not be available in step 2, 3,4? 
Such as type information. 

**NOTE** should this be done on step 3 or 4? 

is the communication now happening between agent and cordra? Or cordra and Handle system? 
For example, Cordra can query the DTR using a PID. 21.T11148/4ac7431c2616a213481e which is a PID-BasicInfoType 
(see https://github.com/hardistyar/openDS-schemas/blob/main/pid-info-types.md) 

7. Cordra accesses the DTR for Type information 

8. DTR returns the Type to Cordra

9. Cordra returns access contrlo and other metadata to the Agent. 

10. If authorized, Agent now requests the content from the data repository (REST or DOIP?). This could in cordra but another repo as well. 

11. Data Repository returns the requested object directly to the Agent. Is cordra not involved here anymore? 

