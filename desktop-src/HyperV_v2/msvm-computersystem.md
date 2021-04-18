---
description: Rappresenta un sistema computer fisico o una macchina virtuale.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565740"
---
# <a name="msvm_computersystem-class"></a>\_Classe MSVM ComputerSystem

Rappresenta un sistema computer fisico o una macchina virtuale.

Per recuperare informazioni per VMMS, usare la classe [**\_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>Members

La **classe \_ ComputerSystem di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ComputerSystem di MSVM** dispone di questi metodi.



| Metodo                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Inserisce un interrupt non mascherabile nella macchina virtuale. Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.<br/> **Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Richiede che lo stato di replica della macchina virtuale venga modificato in un valore specificato. Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Richiede che lo stato di replica della macchina virtuale venga modificato in un valore specificato. Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.<br/> **Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Richiede che lo stato della macchina virtuale venga modificato. Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Questo metodo non è supportato.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Proprietà

La **classe \_ ComputerSystem di MSVM** dispone di queste proprietà.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (.. )
</dt> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e conterrà uno dei valori seguenti.



| Valore                                                                                                | Significato                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Macchina virtuale"</dt> </dl>         | L'istanza rappresenta una macchina virtuale.<br/>    |
| <dl> <dt>"Host computer System"</dt> </dl> | L'istanza rappresenta il computer host.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "MSVM \_ ComputerSystem".

</dd> <dt>

**Dedicato**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il sistema informatico è un sistema speciale (dedicato a un particolare uso), rispetto a un sistema di uso generale. Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 0 (non dedicata).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e conterrà uno dei valori seguenti.



| Valore                                                                                                          | Significato                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Microsoft Virtual computer System"</dt> </dl> | L'istanza rappresenta una macchina virtuale.<br/>    |
| <dl> <dt>"Microsoft hosting computer System"</dt> </dl> | L'istanza rappresenta il computer host.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata sul nome visualizzato del computer per una macchina virtuale o sul nome NetBIOS del sistema operativo di gestione.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà può anche indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata dalla classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è impostata su 2 (Enabled) per un computer fisico o su uno dei valori seguenti per una macchina virtuale. Per una visualizzazione grafica di questi Stati, vedere la sezione Osservazioni.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | Non è stato possibile determinare lo stato dell'elemento.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>                                                 | L'elemento è in esecuzione.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | L'elemento è disattivato.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Chiusura**</dt> di <dt>4</dt> </dl>                         | L'elemento è in corso di passaggio a uno stato disabilitato.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>5</dt> </dl>                     | L'elemento non supporta l'abilitazione o la disabilitazione.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Nel test**</dt> <dt>7</dt> </dl>                                                 | L'elemento si trova in uno stato di test.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Posticipato**</dt> <dt>8</dt> </dl>                                             | È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Mettere in stato**</dt> <dt>9</dt> </dl>                                                 | L'elemento è abilitato ma in modalità con restrizioni. Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato. Tutte le altre richieste vengono accodate.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**A partire**</dt> da <dt>10</dt> </dl>                                            | L'elemento è in corso di attivazione dello stato abilitato (2). Le nuove richieste vengono accodate.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica lo stato corrente della modalità sessione avanzata nella macchina virtuale.

Il provider WMI Hyper-V genera un' [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) ogni volta che viene modificato il **EnhancedSessionModeState** della classe **MSVM \_ ComputerSystem** . Se una sessione vmconnection attiva riceve un **\_ \_ InstanceModificationEvent**, tenta di passare alla modalità sessione avanzata se l'utente ha abilitato tale impostazione.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

**EnhancedSessionModeState** può essere uno dei valori seguenti:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Consentito e disponibile** (2)


</dt> <dd>

La modalità avanzata è consentita e disponibile nella macchina virtuale.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non consentito** (3)


</dt> <dd>

La modalità avanzata non è consentita nella macchina virtuale.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Consentito ma non disponibile** (6)


</dt> <dd>

La modalità avanzata è consentita e non è attualmente disponibile nella macchina virtuale.

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

Tipo di punto dati di ripristino applicato durante l'operazione di failover.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente** con l'applicazione (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Pianificato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica lo stato corrente dell'elemento. Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.

Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate. La proprietà **EnabledState** può inoltre contenere ulteriori informazioni. Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Valore                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | La macchina virtuale è completamente funzionante e funziona entro i normali parametri operativi e senza errori.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Errore principale**</dt> <dt>20</dt> </dl>             | Si è verificato un errore grave della macchina virtuale. Questo valore viene usato quando lo spazio su disco di uno o più dischi che contengono i VHD della macchina virtuale è insufficiente e la macchina virtuale è stata sospesa.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Errore critico**</dt> <dt>25</dt> </dl> | L'elemento è non funzionale e il ripristino potrebbe non essere possibile. Questo può indicare che il processo di lavoro della macchina virtuale (Vmwp.exe) non risponde alle richieste di controllo o informazioni oppure che uno o più dischi che contengono i dischi rigidi virtuali per la macchina virtuale hanno spazio su disco insufficiente.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **null**, per un sistema operativo di gestione. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

In Windows 8 esiste una singola istanza di [**ReplicationSettingData**](msvm-replicationsettingdata.md) per ogni sistema di computer o macchina virtuale. Per Windows 8.1, una macchina virtuale di ripristino dispone di due istanze di **ReplicationSettingData**. Questa modifica distingue e associa i dati all'impostazione con la relazione di replica.



| Nome proprietà  | Valore di Windows 8               | Valore Windows 8.1                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: <vmguid> \\ HVR | Microsoft: <vmguid> \\ HVR \\<0/1> |



 

Nel valore Windows 8.1 0 indica primario e 1 indica la replica estesa. Per ulteriori informazioni sulla replica estesa, vedere [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

Ora in cui è stata ricevuta l'ultima replica coerente con l'applicazione per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

Ora di ricezione dell'ultima replica durante il ripristino per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

Tipo dell'ultima replica ricevuta per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente** con l'applicazione (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Pianificato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di completamento dell'ultimo backup riuscito per la macchina virtuale.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "*GUID*".

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che identifica il modo in cui è stato generato il nome di sistema utilizzando l'euristica della sottoclasse. Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di nodi NUMA (non-Uniform Memory Access) del sistema del computer. Quando **MSVM \_ ComputerSystem** rappresenta il computer host, questa proprietà contiene il numero di nodi NUMA fisici. Quando **MSVM \_ ComputerSystem** rappresenta una macchina virtuale, questa proprietà contiene il numero di nodi NUMA virtuali presentati al sistema operativo guest tramite la tabella di affinità risorse di sistema ACPI (SRAT).

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")
</dt> </dl>

Per la macchina virtuale, questa proprietà indica l'intervallo di tempo, in millisecondi, dall'ultima volta in cui è stato attivato, reimpostato o ripristinato il computer. Questa volta esclude l'ora in cui la macchina virtuale è in stato di sospensione. Per il sistema operativo di gestione, questa proprietà è impostata su **null**.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** . Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene gli stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). Il valore in corrispondenza dell'indice zero (0) corrisponde a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | La macchina virtuale è funzionante e funziona normalmente.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt></dt> Ridotto <dt>3</dt> </dl>                                         | La macchina virtuale è solo parzialmente funzionante. Ciò indica che non è possibile accedere alla risorsa di archiviazione che contiene la configurazione. Una macchina virtuale in questo stato può essere disattivata o eliminata. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Errore predittivo**</dt> <dt>5</dt> </dl> | La macchina virtuale è funzionante, ma potrebbe non riuscire in futuro. Ciò indica che lo spazio disponibile nello spazio di archiviazione che contiene il disco rigido virtuale della macchina virtuale è insufficiente. La macchina virtuale verrà sospesa se non viene reso disponibile più spazio su disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Arrestato**</dt> <dt>10</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene arrestata, il valore della proprietà **EnabledState** sarà 3 (disabilitato).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**Nel servizio**</dt> <dt>11</dt> </dl>                                | La macchina virtuale sta elaborando una richiesta.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>15</dt> <dt>**inattivo**</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene sospesa o sospesa, la proprietà **EnabledState** avrà il valore 32769 (Suspended) o 32768 (Paused).<br/>                                                                                    |



 

Il valore in corrispondenza dell'indice uno (1) è facoltativo e contiene informazioni sullo stato secondario. Un client deve usare lo stato primario da index zero (0) per determinare se una nuova richiesta può essere rilasciata alla macchina virtuale. Se **OperationalStatus** \[ 0 \] è 2 (OK), l'operazione indicata da **OperationalStatus** \[ 1 \] può essere interrotta.

Il valore in **OperationalStatus** \[ 1 \] è uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creazione dello Snapshot**</dt> <dt>32768</dt> </dl>                                 | È in corso la creazione di uno snapshot per la macchina virtuale.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Applicazione dello Snapshot**</dt> <dt>32769</dt> </dl>                                 | È in corso l'applicazione di uno snapshot alla macchina virtuale.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminazione dello Snapshot**</dt> <dt>32770</dt> </dl>                                 | È in corso l'eliminazione di uno snapshot dalla macchina virtuale.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**In attesa dell'avvio**</dt> <dt>32771</dt> </dl>                                     | La macchina virtuale verrà avviata dopo che è trascorso il ritardo di avvio automatico.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Unione di dischi**</dt> <dt>32772</dt> </dl>                                                 | I dischi rigidi virtuali degli snapshot eliminati in precedenza vengono uniti.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Esportazione della macchina virtuale**</dt> <dt>32773</dt> </dl> | È in corso l'esportazione della macchina virtuale.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrazione della macchina virtuale**</dt> <dt>32774</dt> </dl> | È in corso la migrazione della macchina virtuale da un computer fisico a un altro.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other). Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato della macchina virtuale quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), ma non viene utilizzata.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che indica come è possibile raggiungere il proprietario del sistema primario (ad esempio, un numero di telefono o un indirizzo di posta elettronica). Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario del sistema primario. Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del processo in cui è in esecuzione la macchina virtuale. Questo valore può essere utilizzato per identificare in modo univoco l'istanza di Vmwp.exe nel sistema che esegue la macchina virtuale.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Stato di replica per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la modalità di replica per la macchina virtuale. Si tratta di uno dei valori seguenti.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primario** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)


</dt> <dd>

Ripristino

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Replica di test** (3)


</dt> <dd>

Replica

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Replica estesa** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

Stato di replica per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Pronto per la replica** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**In attesa del completamento della replica iniziale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replica** in corso (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replica sincronizzata completata** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Ripristino** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Commit eseguito** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Sospeso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**In attesa dell'avvio della risincronizzazione** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Risincronizzazione** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Risincronizzazione sospesa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover in corso** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Failback in corso** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Failback completato** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per la macchina virtuale passato al metodo [**RequestStateChange**](requeststatechange-msvm-computersystem.md) oppure 12 (non applicabile) se non è in corso alcuna modifica dello stato. Lo stato effettivo dell'elemento è rappresentato da **EnabledState**. Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 1 (other).

</dd> <dt>

**Ruoli**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che descrivono i ruoli riprodotti dal sistema nell'ambiente Information Technology. Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **arrayType** ("indicizzato")
</dt> </dl>

Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** . Se ad esempio 11 (in servizio) è il valore assegnato a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] può contenere una spiegazione del motivo per cui la macchina virtuale sta elaborando una richiesta. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'Ultima modifica del file di configurazione della macchina virtuale. Il file di configurazione viene modificato durante determinate operazioni della macchina virtuale, nonché quando vengono aggiunte, modificate o rimosse le impostazioni della macchina virtuale o del dispositivo.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nella figura seguente vengono mostrati i valori **EnabledState** .

![diagramma di stato per i valori EnabledState per Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

Quando viene modificata una proprietà della classe **MSVM \_ ComputerSystem** , il provider WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) che descrive le modifiche. Lo stato precedente è contenuto nella proprietà **PreviousInstance** e il nuovo stato è contenuto nella proprietà **TargetInstance** . Questo evento è asincrono. al momento dell'elaborazione dell'evento **\_ \_ InstanceModificationEvent** , è possibile che la proprietà **TargetInstance** non rifletta lo stato corrente.

L'accesso alla **classe \_ ComputerSystem di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ComputerSystem CIM**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**\_ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**MSVM \_ ComputerSystem (V1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Classi di sistema virtuali](virtual-system-classes.md)
</dt> </dl>

 

