---
description: Rappresenta un computer fisico o una macchina virtuale.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem classe
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
ms.openlocfilehash: a8a81d5e1503c868865f1f1fae7238be74f024c1bd1c992f5610ce75b5702ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531786"
---
# <a name="msvm_computersystem-class"></a>Classe Msvm \_ ComputerSystem

Rappresenta un computer fisico o una macchina virtuale.

Per recuperare informazioni per vmm, usare la [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ ComputerSystem** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ ComputerSystem** dispone di questi metodi.



| Metodo                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Inserisce un interrupt non mascherabile nella macchina virtuale. Questo metodo è supportato solo per le istanze della **classe Msvm \_ ComputerSystem** che rappresentano una macchina virtuale.<br/> **Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Richiede che lo stato di replica della macchina virtuale sia impostato sul valore specificato. Questo metodo è supportato solo per le istanze della **classe Msvm \_ ComputerSystem** che rappresentano una macchina virtuale.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Richiede che lo stato di replica della macchina virtuale sia impostato sul valore specificato. Questo metodo è supportato solo per le istanze della **classe Msvm \_ ComputerSystem** che rappresentano una macchina virtuale.<br/> **Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Richiede la modifica dello stato della macchina virtuale. Questo metodo è supportato solo per le istanze della **classe Msvm \_ ComputerSystem** che rappresentano una macchina virtuale.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Questo metodo non è supportato.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ComputerSystem** ha queste proprietà.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il *parametro RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica dello stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities,** dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85)) Questa proprietà può essere non **Null se** un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **Null se** un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresta** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Inattiva** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DmTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata dalla [**classe \_ CIM ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e conterrà uno dei valori seguenti.



| Valore                                                                                                | Significato                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Macchina virtuale"</dt> </dl>         | L'istanza rappresenta una macchina virtuale.<br/>    |
| <dl> <dt>"Hosting Computer System"</dt> </dl> | L'istanza rappresenta il computer host.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza di . Questa proprietà viene ereditata dal [**sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "Msvm \_ ComputerSystem".

</dd> <dt>

**Dedicato**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il sistema del computer è un sistema per scopi specifici (dedicato a un uso specifico) rispetto a un sistema per utilizzo generico. Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 0 (non dedicato).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata [**da CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e conterrà uno dei valori seguenti.



| Valore                                                                                                          | Significato                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Microsoft Virtual Computer System"</dt> </dl> | L'istanza rappresenta una macchina virtuale.<br/>    |
| <dl> <dt>"Microsoft Hosting Computer System"</dt> </dl> | L'istanza rappresenta il computer host.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la proprietà **PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata sul nome visualizzato del computer per una macchina virtuale o sul nome NetBIOS del sistema operativo di gestione.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà può anche indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata dalla classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e viene impostata su 2 (Abilitato) per un computer fisico o su uno dei valori seguenti per una macchina virtuale. Per una visualizzazione grafica di questi stati, vedere Osservazioni.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | Impossibile determinare lo stato dell'elemento.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altri**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>                                                 | L'elemento è in esecuzione.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | L'elemento è disattivato.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Arresto 4**</dt> <dt></dt> </dl>                         | L'elemento sta per essere disabilitato.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>5</dt> </dl>                     | L'elemento non supporta l'a abilitato o disabilitato.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | L'elemento potrebbe completare i comandi e elimina eventuali nuove richieste.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Nel test**</dt> <dt>7</dt> </dl>                                                 | L'elemento è in uno stato di test.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Posticipato**</dt> <dt>8</dt> </dl>                                             | L'elemento potrebbe completare i comandi, ma accoderà tutte le nuove richieste.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Disattivazione**</dt> <dt>9</dt> </dl>                                                 | L'elemento è abilitato ma in modalità limitata. Il comportamento dell'elemento è simile allo stato Abilitato (2), ma elabora solo un set limitato di comandi. Tutte le altre richieste vengono accodati.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**A partire**</dt> <dt>da 10</dt> </dl>                                            | L'elemento è in corso di attivazione dello stato Abilitato (2). Le nuove richieste vengono accodati.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica lo stato corrente della modalità sessione avanzata nella macchina virtuale.

Il provider WMI Hyper-V genera un [**\_ \_ evento InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) ogni volta che **cambia EnhancedSessionModeState** della **classe Msvm \_ ComputerSystem.** Se una sessione vmconnection attiva riceve **\_ \_ un evento InstanceModificationEvent,** tenta di passare alla modalità sessione avanzata se l'utente ha abilitato tale impostazione.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

Tipo di punto dati di ripristino applicato durante l'operazione di failover.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; Usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente con l'applicazione** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Pianificato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente quella dei relativi sottocomponenti.

Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate. Anche **la proprietà EnabledState** può contenere altre informazioni. Ad esempio, quando lo spazio su disco è criticamente basso, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (In pausa).

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)



| Valore                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | La macchina virtuale è completamente funzionante e funziona entro i normali parametri operativi e senza errori.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Errore principale**</dt> <dt>20</dt> </dl>             | La macchina virtuale ha subito un errore grave. Questo valore viene usato quando uno o più dischi che contengono i dischi rigidi virtuali della macchina virtuale hanno spazio su disco insufficiente e la macchina virtuale è stata sospesa.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Errore critico**</dt> <dt>25</dt> </dl> | L'elemento non è funzionante e il ripristino potrebbe non essere possibile. Ciò può indicare che il processo di lavoro per la macchina virtuale (Vmwp.exe) non risponde alle richieste di controllo o informazioni o che uno o più dischi che contengono i dischi rigidi virtuali per la macchina virtuale sono a basso contenuto di spazio su disco.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **Null.**

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **Null,** per un sistema operativo di gestione. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

In Windows 8 è presente una singola istanza di [**ReplicationSettingData**](msvm-replicationsettingdata.md) per ogni computer o macchina virtuale. Ad Windows 8.1, una macchina virtuale di ripristino ha due istanze di **ReplicationSettingData**. Questa modifica differenzia e associa i dati di impostazione alla relazione di replica.



| Nome proprietà  | Windows 8 valore               | Windows 8.1 valore                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: <vmguid> \\ HVR | Microsoft: <vmguid> \\ HVR \\<0/1> |



 

Nel valore Windows 8.1, 0 indica la replica primaria e 1 indica la replica estesa. Per altre informazioni sulla replica estesa, vedere [**Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

Ora in cui è stata ricevuta l'ultima replica coerente con l'applicazione per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; Usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

Ora in cui viene ricevuta l'ultima replica al momento del ripristino per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; Usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

Tipo dell'ultima replica ricevuta per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; Usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normale** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente con l'applicazione** (2)


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

Ora in cui è stato completato l'ultimo backup riuscito per la macchina virtuale.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ System**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "*GUID*".

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che identifica il modo in cui è stato generato il nome del sistema, usando l'euristica della sottoclasse. Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **Null.**

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di nodi NUMA (NonUniform Memory Access) del sistema informatico. Quando **Msvm \_ ComputerSystem rappresenta** il sistema del computer di hosting, questa proprietà contiene il numero di nodi NUMA fisici. Quando **Msvm \_ ComputerSystem** rappresenta una macchina virtuale, questa proprietà contiene il numero di nodi NUMA virtuali presentati al sistema operativo guest tramite la tabella SRAT (System Resource Affinity Table) ACPI.

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")
</dt> </dl>

Per la macchina virtuale, questa proprietà indica il tempo, in millisecondi, dall'ultima volta che la macchina è stata accesa, reimpostata o ripristinata. Questa volta esclude l'ora in cui la macchina virtuale è stata sospesa. Per il sistema operativo di gestione, questa proprietà è impostata su **Null.**

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

Matrice contenente gli stati correnti dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) Il valore in corrispondenza dell'indice zero (0) è uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | La macchina virtuale funziona e funziona normalmente.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradato**</dt> <dt>3</dt> </dl>                                         | La macchina virtuale è solo parzialmente funzionante. Ciò indica che l'archiviazione che contiene la configurazione non è accessibile. Una macchina virtuale in questo stato può essere solo spenta o eliminata. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Errore predittivo**</dt> <dt>5</dt> </dl> | La macchina virtuale è funzionante ma potrebbe non riuscire in futuro. Ciò indica che lo spazio di archiviazione che contiene il disco rigido virtuale della macchina virtuale è insufficiente. La macchina virtuale verrà sospesa se non viene reso disponibile più spazio su disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Arrestato**</dt> <dt>10</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene arrestata, il valore della proprietà **EnabledState** sarà 3 (Disabilitato).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**Nel servizio**</dt> <dt>11</dt> </dl>                                | La macchina virtuale sta elaborando una richiesta.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inattiva**</dt> <dt>15</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene sospesa o sospesa, il valore della proprietà **EnabledState** sarà 32769 (Sospeso) o 32768 (Sospeso).<br/>                                                                                    |



 

Il valore in corrispondenza dell'indice uno (1) è facoltativo e contiene informazioni sullo stato secondario. Un client deve usare lo stato primario dall'indice zero (0) per determinare se è possibile eseguire una nuova richiesta alla macchina virtuale. Se **OperationalStatus** \[ 0 è \] 2 (OK), l'operazione indicata da **OperationalStatus** \[ 1 può essere \] interrotta.

Il valore **in OperationalStatus** \[ 1 è uno dei valori \] seguenti.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creazione dello snapshot**</dt> <dt>32768</dt> </dl>                                 | È in corso la creazione di uno snapshot per la macchina virtuale.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Applicazione dello snapshot**</dt> <dt>32769</dt> </dl>                                 | È in corso l'applicazione di uno snapshot alla macchina virtuale.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminazione dello snapshot**</dt> <dt>32770</dt> </dl>                                 | È in corso l'eliminazione di uno snapshot dalla macchina virtuale.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**In attesa dell'avvio**</dt> <dt>32771</dt> </dl>                                     | La macchina virtuale verrà avviata dopo che è trascorso il ritardo di avvio automatico.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Unione di dischi**</dt> <dt>32772</dt> </dl>                                                 | È in corso il merge dei dischi rigidi virtuali degli snapshot eliminati in precedenza.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Esportazione della macchina virtuale**</dt> <dt>32773</dt> </dl> | È in corso l'esportazione della macchina virtuale.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrazione della macchina virtuale**</dt> <dt>32774</dt> </dl> | La macchina virtuale viene migrata in tempo reale da un computer fisico a un altro.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (Altro). Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **Null.**

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato della macchina virtuale quando la **proprietà EnabledState** è impostata su 1 (Altro). Questa proprietà deve essere impostata su **Null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **Null.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), ma non viene usata.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che indica come è possibile raggiungere il proprietario del sistema primario, ad esempio un numero di telefono o un indirizzo di posta elettronica. Questa proprietà viene ereditata dal [**sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)e viene sempre impostata su **Null.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario del sistema primario. Questa proprietà viene ereditata dal [**sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)e viene sempre impostata su **Null.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del processo in cui è in esecuzione la macchina virtuale. Questo valore può essere usato per identificare in modo univoco l'istanza di Vmwp.exe nel sistema che esegue la macchina virtuale.

</dd> <dt>

**Replicationhealth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Integrità della replica per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

I valori possibili sono:

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la modalità di replica per la macchina virtuale. Questo sarà uno dei valori seguenti.

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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

Stato di replica per la macchina virtuale.

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.

 

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

**Replica** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replica sincronizzata completata** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Recuperato** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Commit** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Sospeso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**In attesa di avviare la risincronizzazione** (9)


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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per la macchina virtuale passato al metodo [**RequestStateChange**](requeststatechange-msvm-computersystem.md) oppure 12 (Non applicabile) se non è in corso alcuna modifica dello stato. Lo stato effettivo dell'elemento è rappresentato da **EnabledState.** Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e quello corrente abilitato o disabilitato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 1 (Altro).

</dd> <dt>

**Ruoli**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che descrivono i ruoli del sistema nell'ambiente informatico. Questa proprietà viene ereditata dal [**sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **Null.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
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
</dt> <dt>

Qualificatori: **ArrayType** ("Indexed")
</dt> </dl>

Matrice che contiene stringhe che descrivono i valori della **matrice OperationalStatus** corrispondenti. Ad esempio, se 11 (In Service) è il valore assegnato a **OperationalStatus** \[ \] 0, **StatusDescriptions** 0 può contenere una spiegazione del motivo per cui la macchina virtuale sta elaborando \[ una \] richiesta. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima modifica del file di configurazione della macchina virtuale. Il file di configurazione viene modificato durante determinate operazioni della macchina virtuale, nonché quando una delle impostazioni della macchina virtuale o del dispositivo viene aggiunta, modificata o rimossa.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui l'istanza è in fase di transizione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))ma non viene usata.

</dd> </dl>

## <a name="remarks"></a>Commenti

La figura seguente mostra i **valori EnabledState.**

![Diagramma di stato per i valori enabledstate per Windows Server 2008 r2](images/msvm-computersystem-enabledstate-win2008r2.png)

Quando viene modificata una proprietà **della classe Msvm \_ ComputerSystem,** il provider WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) che descrive le modifiche. Lo stato precedente è contenuto nella **proprietà PreviousInstance** e il nuovo stato è contenuto nella **proprietà TargetInstance.** Questo evento è asincrono. al momento **\_ \_ dell'elaborazione dell'evento InstanceModificationEvent,** la **proprietà TargetInstance** potrebbe non riflettere lo stato corrente.

L'accesso alla **classe Msvm \_ ComputerSystem** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

Vedere [Esecuzione di query sugli oggetti di rete.](querying-networking-objects.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**Msvm \_ ComputerSystem (V1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Classi di sistema virtuale](virtual-system-classes.md)
</dt> </dl>

 

