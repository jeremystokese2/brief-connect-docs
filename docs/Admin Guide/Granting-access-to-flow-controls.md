##Controls
To learn about controls see: [Flow Controls](./Flow-Controls.md)

##Granting permissions for using controls

To grant permissions for users to use any of the controls, admins must go to the PermissionsSet table and create the appropriate permission set.

The controls to be defined are:

* **CanCancelRecord** -> for record cancellation
* **CanTakeNoFurtherAction** -> for marking the record as no further action
* **CanWithdrawRecord** -> for marking the record as withdrawn
* **CanPlaceRecordOnHold** -> for placing the record on hold

![image.png](.attachments/image-f940242b-5428-4f3c-8d1d-23091bee0aa2.png)

Once the Permission Set is configured, the permissions need to be granted through the RoleAssignments table. 