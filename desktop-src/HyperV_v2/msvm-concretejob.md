---
description: Rappresenta un'unità di lavoro e viene utilizzato per tenere traccia dello stato di avanzamento delle operazioni asincrone.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Msvm_ConcreteJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9542d53ad56c736d8dc2fc3950e6e95c92f923b8179f03d52639c0c7ad898c60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531731"
---
# <a name="msvm_concretejob-class"></a>Classe Msvm \_ ConcreteJob

Versione concreta del processo. Questa classe rappresenta un'unità di lavoro generica e istantanea, ad esempio un batch o un processo di stampa, e viene usata in modo specifico in Hyper-V per tenere traccia dello stato di avanzamento delle operazioni asincrone.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ConcreteJob** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ ConcreteJob** include questi metodi.



| Metodo                                                            | Descrizione                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-concretejob.md)                     | Recupera l'oggetto errore per il processo, se esistente.<br/>                |
| [**GetErrorEx**](geterrorex-msvm-concretejob.md)                 | Recupera gli oggetti errore per il processo, se presenti.<br/>                |
| **KillJob**                                                       | Questo metodo non è supportato.<br/>                                         |
| [**RequestStateChange**](requeststatechange-msvm-concretejob.md) | Richiede che lo stato del processo sia stato modificato nello stato specificato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ConcreteJob** ha queste proprietà.

<dl> <dt>

**Annullabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il processo può essere annullato. Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il processo deve essere eliminato automaticamente al completamento. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Completa la proprietà **PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo in cui è stato eseguito il processo o tempo totale di esecuzione se il processo è stato completato. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice di errore specifico del fornitore. Il valore deve essere impostato su zero se il processo è stato completato senza errori. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa contenente la descrizione dell'errore del fornitore. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**PROCESSO CIM \_**](cim-job.md).**ErrorCode**")
</dt> </dl>

Descrizione di riepilogo dell'errore, se presente. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente dei relativi sottocomponenti. I valori possibili sono da 0 a 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionante. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **Null.**

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di volte in cui il processo deve essere eseguito. Il valore 1 indica che il processo non è ricorrente, mentre qualsiasi valore diverso da zero indica un limite al numero di volte in cui il processo verrà ricorrente. Zero indica che non esiste alcun limite al numero di volte in cui il processo può essere elaborato, ma verrà terminato dopo che è stato raggiunto **UntilTime** o il processo verrà terminato manualmente. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**JobState** è un'enumerazione integer che indica lo stato operativo di un processo. Può anche indicare le transizioni tra questi stati, ad esempio "Arresto in corso" e "Avvio in corso". Questa proprietà viene ereditata da [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))



| Valore                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Nuovo**</dt> <dt>2</dt> </dl>                                                           | Il processo non è mai stato avviato.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**A partire**</dt> <dt>da 3</dt> </dl>                                       | Il processo si sposta dallo stato 2 (Nuovo), 5 (Sospeso) o 11 (Servizio) allo stato 4 (In esecuzione).<br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Esecuzione**</dt> <dt>di 4</dt> </dl>                                           | Il processo è in esecuzione.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Sospeso**</dt> <dt>5</dt> </dl>                                   | Il processo viene arrestato, ma può essere riavviato in modo trasparente.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Arresto in fase**</dt> <dt>di arresto 6</dt> </dl>                   | Il processo sta passando a uno stato 7 (Completato), 8 (Terminato) o 9 (Terminato).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Completata**</dt> <dt>7</dt> </dl>                                   | Il processo è stato completato normalmente.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Terminato 8**</dt> <dt></dt> </dl>                               | Il processo è stato arrestato da una richiesta di modifica dello stato "Terminate". Il processo e tutti i processi sottostanti vengono terminati e possono essere riavviati solo come nuovo processo. Il requisito che il processo venga riavviato solo come nuovo processo è specifico del processo.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**9**</dt> <dt>disammati</dt> </dl>                                               | Il processo è stato arrestato da una richiesta di modifica dello stato "Kill". I processi sottostanti potrebbero essere ancora in esecuzione e potrebbe essere necessaria una pulizia per liberare risorse.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Eccezione**</dt> <dt>10</dt> </dl>                                  | Il processo si trova in uno stato anomalo che potrebbe essere indicativo di una condizione di errore. Lo stato effettivo del processo potrebbe essere disponibile tramite oggetti specifici del processo.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Servizio**</dt> <dt>11</dt> </dl>                                          | Il processo si trova in uno stato specifico del fornitore che supporta l'individuazione o la risoluzione dei problemi o entrambi.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>12 32767</dt> </dl>            | Riservato.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Fornitore riservato**</dt> <dt>32768 65535</dt> </dl> | Riservato.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**Stato processo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che rappresenta lo stato del processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tipo di processo monitorato da questo oggetto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Definire la macchina virtuale** (1)


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modificare la macchina virtuale** (2)


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Eliminare la macchina virtuale** (3)


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modificare le impostazioni del Impostazioni** gestione (4)


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Inizializzare la macchina** virtuale (10)


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**In attesa dell'avvio della macchina virtuale** (11)


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Avviare la macchina virtuale** (12)


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Spegnere la macchina virtuale** (13)


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Salvare la macchina virtuale** (14)


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Ripristinare una macchina virtuale** (15)


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Arrestare la macchina virtuale** (16)


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Sospendere la macchina virtuale** (26)


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Riprendere la macchina virtuale** (27)


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reimpostare la macchina virtuale** (28)


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Riavviare la macchina** virtuale (29)


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Aggiungere risorse macchina virtuale** (30)


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modificare le risorse delle macchine virtuali** (31)


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Rimuovere le risorse della macchina virtuale** (32)


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Richiedere la memoria iniziale della macchina virtuale** (40)


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Aggiungere memoria alla macchina virtuale** (41)


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Rimuovere memoria dalla macchina virtuale** (42)


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Unione di dischi rigidi virtuali** (50)


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Creare uno snapshot VSS all'interno della macchina** virtuale (51)


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Ottenere i dati delle impostazioni di importazione** (60)


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Importare una macchina** virtuale (61)


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Esportare una macchina** virtuale (62)


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Registrare la** configurazione (63)


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Annullare la registrazione della** configurazione (64)


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Macchina virtuale snapshot** (70)


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Applicare lo snapshot della macchina virtuale** (71)


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Eliminare lo snapshot della macchina virtuale** (72)


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Cancellare lo stato dello snapshot della macchina virtuale** (73)


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Aggiungere risorse al pool di risorse** (80)


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Rimuovere risorse dal pool di risorse** (81)


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modificare l'Impostazioni** server di replica (90)


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Creare una relazione di** replica (91)


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modificare la relazione di Impostazioni** (92)


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Rimuovere la relazione di** replica (93)


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Avviare la replica iniziale inband** (94)


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Replica di** importazione (95)


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicare la modifica dello** stato (96)


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Avviare il failover** (97)


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Ripristinare il failover** (98)


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Failover di commit** (99)


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Avviare la replica sincronizzata** (100)


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Annullare la replica sincronizzata** (101)


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Avviare la replica di** test (102)


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Rimuovere la replica di** test (103)


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Replica inversa** (104)


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Delta invio replica** (105)


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Delta ricezione replica** (106)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (107)


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Applicare il log delle** modifiche (108)


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Arrestare la replica** iniziale (109)


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Interrompi risincronizzazione** (110)


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Ottenere le statistiche della** replica (111)


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Preparare il controllo di coerenza** (112)


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Verifica coerenza** (113)


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Arrestare verifica coerenza** (114)


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Testare la connessione di** replica (115)


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Invio della replica iniziale** (116)


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Avviare la risincronizzazione della replica iniziale** (117)


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Avviare l'esportazione della replica** iniziale (118)


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reimpostare le statistiche della** replica (119)


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Applicare delta registrati** (120)


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Risincronizzazione della replica estesa** (121)


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Lettura della configurazione della replica di** test (122)


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Impostare la modalità di replica su primaria** (123)


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Avviare il failback** (124)


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Aggiornare il set di dischi** (125)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Definire il commutatore Ethernet** (130)


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modificare l'impostazione del Impostazioni Ethernet** (131)


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Eliminare il commutatore Ethernet** (132)


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Aggiungere risorse commutatore Ethernet** (133)


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modificare le risorse del commutatore Ethernet** (134)


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Rimuovere le risorse del commutatore Ethernet** (135)


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Convalidare la macchina virtuale** pianificata (140)


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creazione di un pool di** risorse (150)


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Modifica delle risorse padre di un pool di risorse** (151)


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Modifica del valore non di Impostazioni di un pool di risorse** (152)


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Eliminazione di un pool di** risorse (153)


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Abilitare la GPU RemoteFx** (160)


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disabilitare la GPU RemoteFx** (161)


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modificare l'Impostazioni 3D** (162)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup macchina virtuale** (170)


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Interfaccia del servizio guest** (180)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Eseguire query sulle informazioni sul cluster guest** (181)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Definire la** raccolta (190)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rinomina raccolta** (192)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Aggiungere un membro alla raccolta** (193)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Rimuovere un membro dalla raccolta** (194)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Aggiungere un'impostazione alla raccolta** (195)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Rimuovere l'impostazione dalla raccolta** (196)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modificare l'impostazione per la** raccolta (197)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Raccolta snapshot** (198)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convertire uno snapshot in un punto di riferimento** (200)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Creare un punto di** riferimento (201)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Eliminare il punto di** riferimento (202)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Esportare il punto di** riferimento (203)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Rimuovere i dati associati dal punto di riferimento** (204)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Creare un punto di riferimento nella raccolta** (205)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Esportare il punto di riferimento nella** raccolta (206)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Rimuovere i dati associati dal punto di riferimento nella raccolta** (207)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Eliminare un punto di riferimento nella raccolta** (208)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importare metadati del punto di** riferimento (209)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10 come **punto di riferimento di pulizia.**

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Montare o smontare un dispositivo assegnabile** (260)


</dt> <dd>

> [!Note]  
> Valore aggiunto in Windows 10.

 

</dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le ore rappresentate nelle **proprietà RunStartInterval** e **UntilTime** rappresentano l'ora locale o l'ora UTC. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Ora locale** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Ora UTC** (2 )
</dt> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome visualizzato per questa istanza di un processo. Inoltre, il nome visualizzato può essere usato come proprietà per una ricerca o una query. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utente che viene notificato al completamento o all'errore del processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere usato per fornire maggiori dettagli rispetto al valore della **proprietà EnabledState.** Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati correnti dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice viene sempre impostato su 2 (OK).

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive l'azione di ripristino quando la **proprietà RecoveryAction** dell'istanza è 1 (Altro). Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utente che ha inviato il processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )
</dt> </dl>

Percentuale di completamento del processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire lo stato di integrità generale e dettagliato dell'elemento e dei relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Importanza dell'esecuzione di un processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'azione di ripristino da eseguire per un processo che non è stato eseguito correttamente. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Non continuare** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continua con processo successivo** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Eseguire di nuovo il processo** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Esegui processo di ripristino** (5 )
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MinValue** ( -31 ), **MaxValue** ( 31 )
</dt> </dl>

Giorno del mese in cui deve essere elaborato il processo. Esistono interpretazioni diverse per questa proprietà, a seconda del valore di **RunDayOfWeek.**

Quando **RunDayOfWeek** è 0 e **RunDay** è positivo, **RunDay** definisce il giorno del mese in cui viene elaborato il processo. Ad esempio, se **RunDayOfWeek** è 0 e **RunDay** è 12, il processo verrà elaborato il 12° giorno del mese.<sup></sup>

Quando **RunDayOfWeek** è 0 e **RunDay** è negativo, **RunDay** definisce il numero di giorni prima dell'ultimo giorno del mese in cui viene elaborato il processo.  1 indica l'ultimo giorno del mese, 2 indica un giorno prima dell'ultimo giorno del mese e così via. Ad esempio, se **RunDayOfWeek** è 0 e **RunDay** è 1, il processo verrà elaborato l'ultimo giorno del mese.

Quando **RunDayOfWeek** non è 0, **RunDayOfWeek** è il giorno della settimana in cui verrà elaborato il processo, relativo a **RunDay**. Ad esempio, se **RunDay** è 15 e **RunDayOfWeek** è 7 (+sabato), il processo verrà elaborato il primo sabato il giorno o dopo il 15° giorno del mese.<sup></sup> Se **RunDay** è 20 e **RunDayOfWeek** è 7 (sabato), il processo verrà elaborato il primo sabato il giorno o prima del 20° giorno del mese.<sup></sup> Se **RunDay** è 1 e **RunDayOfWeek** è 1 ( domenica), il processo verrà elaborato l'ultima domenica del mese.

Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intero positivo o negativo utilizzato in combinazione con **RunDay** per indicare il giorno della settimana o del mese in cui viene elaborato il processo. Per altre informazioni, vedere la descrizione della proprietà **RunDay.** Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** (7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** (6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Giovedì** ( 5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Mercoledì** ( 4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** (3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** (2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** (1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domenica** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunedì** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martedì** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Mercoledì** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Giovedì** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Venerdì** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sabato** (7 )
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Mese durante il quale deve essere elaborato il processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Gennaio** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febbraio** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**Aprile** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Maggio** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Giugno** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Luglio** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Settembre** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Ottobre** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembre** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dicembre** (11 )
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo dopo la mezzanotte in cui deve essere elaborato il processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio pianificata per il processo, se applicabile. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio del processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ma non viene usata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus.** Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Periodo di tempo, in minuti, in cui il processo viene mantenuto al termine dell'esecuzione, in caso di esito positivo o negativo dell'esecuzione. Il processo deve rimanere in esecuzione per un certo periodo di tempo indipendentemente dal valore della **proprietà DeleteOnCompletion.** Il valore predefinito è 5 minuti. Questa proprietà viene ereditata da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))ed è sempre impostata su 0000000000500.000000:000.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'ultima modifica dello stato del processo. Se lo stato del processo non è stato modificato e questa proprietà viene popolata, è necessario impostarla su un valore di intervallo pari a 0. Se una modifica dello stato è stata richiesta ma rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata. Questa proprietà viene ereditata da [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di invio del processo. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora in cui il processo non è valido o deve essere arrestato. Questa proprietà viene ereditata dal [**processo CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ConcreteJob** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

