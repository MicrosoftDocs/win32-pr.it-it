---
description: Rappresenta una porta Ethernet interna (scheda di rete).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752367"
---
# <a name="msvm_internalethernetport-class"></a>\_Classe MSVM InternalEthernetPort

Rappresenta una porta Ethernet interna (scheda di rete). Questo tipo di porta Ethernet consente alle macchine virtuali di accedere al server di virtualizzazione che esegue il software di rete. Le schede di rete interne consentono di instradare o filtrare il traffico di rete delle macchine virtuali prima di uscire dal sistema fisico.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Members

La **classe \_ InternalEthernetPort di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ InternalEthernetPort di MSVM** dispone di questi metodi.



| Metodo                                                                     | Descrizione                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                           | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                           | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                          | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-internalethernetport-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-internalethernetport-reset.md)                           | Reimposta il dispositivo virtuale.<br/>    |
| **RestoreProperties**                                                      | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                         | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                          | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ InternalEthernetPort di MSVM** dispone di queste proprietà.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** . Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Rilevamento automatico**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità della porta Ethernet. Se sono elencate le funzionalità di failover o bilanciamento del carico, è necessario definire anche un [**\_ SpareGroup CIM**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) o [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (bilanciamento del carico) per descrivere completamente la funzionalità. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)
</dt> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità della porta Ethernet indicate nell'array delle **funzionalità** . Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

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

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Un indirizzo o altre informazioni di identificazione utilizzate per assegnare un nome univoco al dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific Data*".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e viene generata in base alla scheda di interfaccia di rete presente nell'host.

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica quali funzionalità sono abilitate dall'elenco di tutti quelli supportati, definiti nella matrice delle **funzionalità** . Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)
</dt> </dl>

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite. Questa proprietà viene ereditata dalla proprietà [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta funziona in modalità full duplex. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** . Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **OtherIdentifyingInfo** che si trova nello stesso indice. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore **DateTime** che indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipi di collegamenti. Quando è impostata su 1 (other), la proprietà correlata **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Valore                                                                        | Significato             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | Ethernet<br/> |



 

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà è stata deprecata. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza di banda massima della porta, in bit al secondo. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Gli indirizzi MAC Ethernet/802.3 formattati come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico (il bit dell'indirizzo del gruppo viene trovato nel bit di ordine inferiore del primo carattere della stringa). Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

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

Stato corrente dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità abilitata specificata come 1 (other). Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tutti i dati, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico. Ad esempio, è possibile usare questa proprietà per conservare il nome visualizzato del sistema operativo per il dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa che descrive la proprietà **LinkTechnology** quando è impostata su 1 (other). Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà è deprecata. Utilizzare la proprietà **portType** . Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

Deprecated Description: tipo di modulo, quando la proprietà **portType** è impostata su 1 (other).

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di modulo, quando la proprietà **portType** è impostata su 1 (other). Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) .

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete hardcoded in una porta. Questo indirizzo può essere modificato usando un aggiornamento del firmware o una configurazione software. Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento. Questa operazione deve essere lasciata vuota se per la scheda di rete non esiste alcun indirizzo hardcoded. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**NumeroPorta**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete. Questo valore è 1 per le NIC emulate, 0 per tutti gli altri. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità specifica attualmente abilitata per la porta. Quando è impostata su 1 (other), la proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 rame 10BaseT** (50)
</dt> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)
</dt> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)
</dt> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)
</dt> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)
</dt> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)
</dt> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)
</dt> <dt>

<span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 fibre 100BASE-FX** (100)
</dt> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)
</dt> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)
</dt> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)
</dt> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)
</dt> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)
</dt> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)
</dt> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)
</dt> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)
</dt> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)
</dt> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)
</dt> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (16000 65535)
</dt> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità di risparmio energia del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il dispositivo può essere gestito da energia elettrica. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di ore consecutive in cui il dispositivo è stato alimentato, dall'ultimo ciclo di alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza di banda richiesta della porta, in bit al secondo. La larghezza di banda effettiva viene segnalata nella proprietà **velocità** . Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per il servizio di gestione. Quando la proprietà **EnabledState** è impostata su 5 (non applicabile), questa proprietà non ha alcun significato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **override**, **unità** ("bit al secondo")
</dt> </dl>

Larghezza di banda corrente della porta in bit al secondo. Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** . Le voci in questa matrice sono correlate a quelle nello stesso indice di matrice in **OperationalStatus**. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità di trasmissione massima (MTU) che può essere supportata. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non è supportata

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica apportata alla proprietà **EnabledState** dell'elemento. Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0. Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene utilizzata.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero totale di ore in cui il dispositivo è stato alimentato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).



| Valore                                                                        | Significato                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>4</dt> </dl> | Senza restrizioni<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ InternalEthernetPort di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ETHERNETPORT CIM**](cim-ethernetport.md)
</dt> <dt>

[**\_ETHERNETPORT CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

