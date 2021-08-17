---
description: Rappresenta le funzionalità e la gestione del controller seriale.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Classe Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04cf87a40b48e5f0fc505fe5bc921229ce208fe910d9418431ddae3187b2c5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950700"
---
# <a name="msvm_serialcontroller-class"></a>Classe Msvm \_ SerialController

Rappresenta le funzionalità e la gestione del controller seriale. I controller seriali sono dispositivi logici che sono sempre presenti in una macchina virtuale e pertanto non vengono allocati tramite un pool di risorse. Un'istanza del controller seriale è sempre presente in una macchina virtuale. I controller seriali hanno un numero fisso di istanze di porta. Questa implementazione supporta due porte per ogni controller.

> [!Note]  
> I controller seriali sono facoltativi [nelle macchine virtuali di seconda generazione.](virtualization-glossary.md)

 

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SerialController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SerialController** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ SerialController msvm** include questi metodi.



| Metodo                                                                 | Descrizione                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                       | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                       | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                      | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-serialcontroller-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-serialcontroller-reset.md)                           | Reimposta il dispositivo.<br/>            |
| **Proprietà di ripristino**                                                  | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                     | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                      | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ SerialController msvm** ha queste proprietà.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato aggiuntivi del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)



| Valore                                                                            | Significato                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{ 6 }</dt> </dl> |                           |
| <dl> <dt>6</dt> </dl>     | Non applicabile<br/> |



 

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)



| Valore                                                                        | Significato                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | Non applicabile<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il *parametro RequestedState* del **metodo RequestStateChange.** Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))ma non viene usata.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Buffering e altre funzionalità del controller seriale che potrebbero essere intrinseche nell'hardware del chip. Questa proprietà viene ereditata da [**CIM \_ SerialController.**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità del controller seriale indicata nella matrice **Capabilities.** Questa proprietà viene ereditata da [**CIM \_ SerialController.**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)

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

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione OK** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza di . Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

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

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore non ripristinabile** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in caso di** errore (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft: *<GUID>* ".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Impostazione predefinita abilitata**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))



| Valore                                                                        | Significato            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Attivato<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Può anche indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))



| Valore                                                                        | Significato                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>5</dt> </dl> | Non applicabile<br/> |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'errore segnalato nella **proprietà LastErrorCode** è ora cancellato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni su eventuali azioni correttive che possono essere eseguite. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Ciò esprime l'integrità di questo elemento, ma non necessariamente dei relativi sottocomponenti. I valori possibili sono da 0 a 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionante. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli sulle voci nella matrice di proprietà **OtherIdentifyingInfo.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **Null.**

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

**MaxBaudRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Velocità massima in baud, in bit al secondo, supportata dal controller seriale. Questa proprietà viene ereditata da [**CIM \_ SerialController.**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di entità indirizzabili direttamente supportate da questo controller. Se il numero è sconosciuto o illimitato, è necessario usare il valore 0. Protocollo usato dal controller per accedere ai dispositivi controllati. Questa proprietà viene ereditata dal [**\_ controller CIM.**](/windows/desktop/CIMWin32Prov/cim-controller)

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

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata [**da CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla **proprietà ElementName.**

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere usato per fornire maggiori dettagli rispetto al valore della **proprietà EnabledState.** Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partire** da (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattiva** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Disasserazione** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Creazione di snapshot** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati correnti dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 (Altro). Questa proprietà deve essere impostata su **Null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali dati aggiuntivi, oltre alle informazioni sull'ID dispositivo, che possono essere usati per identificare un dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **Null.**

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

Numero di ore consecutive di accensione del dispositivo dall'ultimo ciclo di alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ma non viene usata.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire lo stato di integrità generale e dettagliato dell'elemento e dei relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**ProtocolDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce altre informazioni correlate al protocollo supportato dal controller. Questa proprietà viene ereditata dal [**\_ controller CIM.**](/windows/desktop/CIMWin32Prov/cim-controller)

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo usato dal controller per accedere ai dispositivi controllati. Questa proprietà viene ereditata dal [**\_ controller CIM.**](/windows/desktop/CIMWin32Prov/cim-controller)



| Valore                                                                         | Significato             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <dt>26</dt> </dl> | IEEE-488<br/> |



 

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato da **EnabledState.** Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti abilitati o disabilitati. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))



| Valore                                                                         | Significato                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | Non applicabile<br/> |



 

</dd> <dt>

**Sicurezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sicurezza operativa per il controller. Questa proprietà viene ereditata da [**CIM \_ SerialController.**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)



| Valore                                                                        | Significato         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <dt>3</dt> </dl> | Nessuno<br/> |



 

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ma non viene usata.

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

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco per la macchina virtuale di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'ultima volta in cui il controller è stato acceso. Questa proprietà viene ereditata dal [**\_ controller CIM.**](/windows/desktop/CIMWin32Prov/cim-controller)

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

Indica lo stato di destinazione a cui è in fase di transizione l'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))ma non viene usata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SerialController** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> <dt>

[**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[Classi di dispositivi seriali](serial-devices-classes.md)
</dt> </dl>

 

