The log contained an average of 863,153 events from 5,750 unique user equipments (UE), with 150 events per UE.  

Example of events in the file:  
```
[08:37:55.792054044] (+0.000001665) localhost.localdomain com_tieto_tnp_lte_ue:procedure:  
{ packet_seq_num = 34, cpu_id = 2 },  
{ vpid = 28825, vtid = 28825, procname = "cnsim" },  
{ cell_id = 0x9, ue_id = 0x14B3, proc_id = 0x4082, proc_name = "", new_state = "CNSIM_UE_TOP:ContextSetup" }  
```
com_tieto_tnp_lte_ue:procedure - trace name  
packet_seq_num - 64-bit sequence number tagging each packet sent over the network.  
cpu_id - cpu core id  
vpid - process id  
vtid - thread id  
procname - microservice name  
cell_id - cell identity that the user equipment is using (UE will always be using the same cell id in this log)  
ue_id - user equipment id  
proc_id - procedure id  
proc_name - procedure name  
new_state - provides information about what's happening in the application  
```
[08:37:55.793967920] (+0.000266605) localhost.localdomain com_tieto_tnp_lte_ue:sig_procedure:  
{ packet_seq_num = 88, cpu_id = 0 },  
{ vpid = 28825, vtid = 28825, procname = "cnsim" },  
{ cell_id = 0x9, ue_id = 0x1675, proc_id = 0x4088, sig_name = "UPLINK_NAS_TRANSPORT", sending_proc = "CU-CP", protocol = "S1AP" }  
```
com_tieto_tnp_lte_ue:sig_procedure - trace name  
sig_name - information about the signal sent or received  
sending_proc - the procedure that has sent a signal  
protocol - protocol name used for sending / receiving signals  
```
[08:32:55.270100962] (+0.000001163) localhost.localdomain com_tieto_tnp_lte_ue:map_procedure:  
{ packet_seq_num = 0, cpu_id = 0 },  
{ vpid = 28825, vtid = 28825, procname = "cnsim" },  
{ id1 = 0x1, id2 = 0x1, id1_name = "CU_CP_ue_id", id2_name = "MME_ue_id" }  
```
id1 - id of the first identity that should be mapped to id2  
id2 - id of the second identity that should be mapped to id1  
id1_name - the name of object 1 that uses id1  
id2_name - the name of object 2 that uses id2  
