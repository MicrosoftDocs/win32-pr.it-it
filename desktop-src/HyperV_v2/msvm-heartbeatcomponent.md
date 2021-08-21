---
description: Rappresenta lo stato del servizio heartbeat, responsabile del monitoraggio dello stato di una macchina virtuale segnalando un heartbeat a intervalli regolari.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Msvm_HeartbeatComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdea278fb6fdce57e938ce3cf2e53f8f453cbd98e73591c6710341157683e3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147817"
---
# <a name="msvm_heartbeatcomponent-class"></a>Classe Msvm \_ HeartbeatComponent

Rappresenta lo stato del servizio heartbeat, responsabile del monitoraggio dello stato di una macchina virtuale segnalando un heartbeat a intervalli regolari.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ HeartbeatComponent** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ HeartbeatComponent msvm** include questi metodi.



| Metodo                                                                   | Descrizione                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                         | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                         | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                        | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-heartbeatcomponent-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-heartbeatcomponent-reset.md)                           | Reimposta il dispositivo virtuale.<br/>    |
| **Proprietà di ripristino**                                                    | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                       | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                        | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nella classe **Msvm \_ HeartbeatComponent.**

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato aggiuntivi del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il *parametro RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica dello stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities,** dove i valori selezionati sono una funzione dello stato corrente di [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85)) Questa proprietà può essere non **Null se** un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **Null se** un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

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

Breve descrizione dell'oggetto. Questa proprietà viene ereditata dalla [**classe \_ CIM ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "Heartbeat".

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

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Msvm \_ HeartbeatComponent".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Heartbeat Service".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la proprietà **PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft: \\ *VMGUID GUID*" dove *VMGUID* è la proprietà **Name** di [**Msvm \_ ComputerSystem**](msvm-computersystem.md) associata al dispositivo.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Heartbeat".

</dd> <dt>

**Impostazione predefinita abilitata**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 7 (nessun valore predefinito).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.



| Valore                                                                                                                                                                                                                           | Significato                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>     | L'elemento è in esecuzione.<br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl> | L'elemento è disattivato.<br/> |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'errore segnalato in **LastErrorCode** è ora cancellato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene usata.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni su eventuali azioni correttive che è possibile eseguire. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene usata.

</dd> <dt>

**Stato di integrità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli sulle voci nella matrice di proprietà **OtherIdentifyingInfo.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione del servizio di integrazione nella macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà è stata deprecata. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stato corrente dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ \] 0.

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd>

Il servizio funziona normalmente. I valori delle proprietà **OperationalStatus** \[ 1 \] e **StatusDescriptions** \[ 1 possono \] contenere altre informazioni.

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)


</dt> <dd>

Il servizio funziona normalmente, ma il servizio guest ha negoziato una versione del protocollo di comunicazione compatibile. I valori delle proprietà **OperationalStatus** \[ 1 \] e **StatusDescriptions** \[ 1 possono \] contenere altre informazioni.

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore non ripristinabile** (7)


</dt> <dd>

Il guest non supporta una versione del protocollo compatibile. I valori delle proprietà **OperationalStatus** \[ 1 \] e **StatusDescriptions** \[ 1 possono \] contenere altre informazioni.

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)


</dt> <dd>

Il servizio guest non è installato o non è ancora stato contattato.

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)


</dt> <dd>

Il servizio guest non risponde più normalmente.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**In pausa** (15)


</dt> <dd>

La macchina virtuale è sospesa.

</dd> </dl>

Il **valore della proprietà OperationalStatus** \[ 1 indica i valori dello stato \] dell'applicazione uniti. Si tratta di uno dei valori seguenti.

> [!Note]  
> Lo stato di un'applicazione viene impostato nella macchina virtuale usando il [**metodo SetApplicationState.**](ivmapplicationhealthmonitor-setapplicationstate.md)

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd>

Le applicazioni in esecuzione all'interno della macchina virtuale operano normalmente.

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Mancata corrispondenza del protocollo** (32775)


</dt> <dd>

I componenti guest e host eseguono versioni del protocollo diverse.

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Stato critico dell'applicazione** (32782)


</dt> <dd>

Una o più applicazioni all'interno della macchina virtuale sono in uno stato critico.

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout comunicazione** (32783)


</dt> <dd>

Timeout in attesa di una risposta dal componente guest.

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Comunicazione non** riuscita (32784)


</dt> <dd>

Impossibile comunicare con il componente guest.

</dd> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 (Altro). Questa proprietà deve essere impostata **su Null** quando la **proprietà EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali dati aggiuntivi, oltre alle informazioni sull'ID dispositivo, che possono essere usati per identificare un dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **Null.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità di risparmio energia del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il dispositivo può essere gestito dall'alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di ore consecutive di accensione del dispositivo dall'ultimo ciclo di alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene usata.

</dd> <dt>

**Stato primario**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni generali sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene usata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari **valori della matrice OperationalStatus.** Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Msvm \_ ComputerSystem".

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è il nome del [**\_ ComputerSystem Msvm**](msvm-computersystem.md) associato a questo servizio heartbeat.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di ore di alimentazione del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

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

L'accesso alla **classe \_ HeartbeatComponent msvm** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

L'esempio C# seguente ottiene lo stato di integrità dell'applicazione di una macchina virtuale. Le utilità a cui si fa riferimento sono disponibili in [Utilità comuni per gli esempi di virtualizzazione (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Per funzionare correttamente, il codice seguente deve essere eseguito con privilegi di amministratore.

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[**Msvm \_ HeartbeatComponent**](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

