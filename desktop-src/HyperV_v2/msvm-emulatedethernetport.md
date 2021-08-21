---
description: Rappresenta una scheda Ethernet emulata.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Classe Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ef4d061d709f83e5069614f169252c06a370106a938b98281afb88b5a11508fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148357"
---
# <a name="msvm_emulatedethernetport-class"></a>Classe Msvm \_ EmulatedEthernetPort

Rappresenta una scheda Ethernet emulata. Questa scheda viene usata quando una macchina virtuale non è in grado di eseguire la porta Ethernet sintetica quando nel guest non sono installati circuiti integrati.

> [!Note]  
> Questa classe non è disponibile per le macchine virtuali di seconda generazione.

 

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
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
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EmulatedEthernetPort** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ EmulatedEthernetPort** include questi metodi.



| Metodo                                                                     | Descrizione                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                           | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                           | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                          | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-emulatedethernetport-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-emulatedethernetport-reset.md)                           | Reimposta il dispositivo emulato.<br/>   |
| **Proprietà di ripristino**                                                      | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                         | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                          | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EmulatedEthernetPort** ha queste proprietà.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'unità massima di trasmissione attiva o negoziata (MTU) che può essere supportata. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 1500.

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi disponibilità e stato aggiuntivi del dispositivo, oltre a quello specificato nella **proprietà Availability.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 ("Non applicabile").

</dd> <dt>

**AutoSense**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su **True.**

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **Null.**

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

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità della porta Ethernet. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene usata.

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità della porta Ethernet indicata nella matrice **Capabilities.** Si noti che ogni voce di questa matrice è correlata alla voce nella matrice **Capabilities** che si trova in corrispondenza dello stesso indice. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene usata.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Porta Ethernet".

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

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave di questa classe, questa proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Msvm \_ EmulatedEthernetPort".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Emulated Ethernet Port".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la **proprietà PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo o altre informazioni di identificazione usate per assegnare un nome univoco al dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID* \\ *device-specific data".*

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Legacy Network Adapter".

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità abilitate dall'elenco di tutte le funzionalità supportate, definite nella matrice **Capabilities.** Questa proprietà viene ereditata da [**CIM \_ EthernetPort,**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)ma non viene usata.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su 2 ("Enabled").

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e viene sempre impostata su 5 ("Non applicabile").

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'errore segnalato in **LastErrorCode** è ora cancellato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce altre informazioni sull'errore registrato in **LastErrorCode** e informazioni su eventuali azioni correttive che è possibile eseguire. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta funziona in modalità full duplex. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su **True.**

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente quella dei relativi sottocomponenti. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 ("OK").

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che forniscono spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo.** Ogni voce di questa matrice è correlata alla voce in **OtherIdentifyingInfo** che si trova nello stesso indice. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore **datetime** che indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipi di collegamenti. Se impostata su 1 ("Altro"), la proprietà correlata **OtherLinkTechnology** contiene una descrizione stringa del tipo di collegamento. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ed è sempre impostata su 2 ("Ethernet").

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e viene sempre impostata su 1500.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**Maxspeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza di banda massima della porta, in bit al secondo. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))ed è sempre impostata su 100000000000.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, questa proprietà può essere sottoposta a override per essere una proprietà chiave. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "Porta Ethernet".

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi MAC Ethernet/802.3, formattati come dodici cifre esadecimali (ad esempio, "010203040506"), con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico (il bit dell'indirizzo del gruppo si trova nel bit di ordine basso del primo carattere della stringa). Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene usata.

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

Stati correnti dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e viene sempre impostata su 2 ("OK").

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per le funzionalità abilitate specificate come "Altro". Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene usata.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 ("Other"). Questa proprietà deve essere impostata su **Null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene usata.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tutti i dati, oltre alle informazioni sull'ID dispositivo, che possono essere usati per identificare un dispositivo logico. Ad esempio, è possibile usare questa proprietà per contenere il nome visualizzato del sistema operativo per il dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa che descrive **LinkTechnology** quando è impostato su 1 ("Altro"). Questa proprietà viene ereditata da [**CIM \_ NetworkPort,**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ma non viene usata.

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ed è impostata su **Null.**

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di modulo, quando **PortType** è impostato su 1 ("Other"). Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ed è sempre impostata su "Virtual Ethernet".

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete hardcoded in una porta. Questo indirizzo può essere modificato usando un aggiornamento del firmware o una configurazione software. Quando viene apportata questa modifica, il campo deve essere aggiornato contemporaneamente. Questa opzione deve essere lasciata vuota se non esiste alcun indirizzo hardcoded per la scheda di rete. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Portnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Le porte di rete sono spesso numerate rispetto a un modulo logico o a un elemento di rete. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Valore                                                                        | Significato                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0</dt> </dl> | La scheda di interfaccia di rete non è emulata.<br/> |
| <dl> <dt>1</dt> </dl> | La scheda di interfaccia di rete è emulata.<br/>     |



 

</dd> <dt>

**Porttype**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità specifica attualmente abilitata per la porta. Se impostata su 1 ("Altro"), la proprietà correlata **OtherPortType** contiene una descrizione stringa del tipo di porta. Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e viene sempre impostata su 1 ("Altro").

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità di risparmio energia del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il dispositivo può essere gestito dall'alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di ore consecutive di alimentazione del dispositivo, dall'ultimo ciclo di alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza di banda richiesta della porta, in bit al secondo. La larghezza di banda effettiva viene segnalata in LogicalPort.Speed. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))ed è sempre impostata su 10000000000.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per il servizio di gestione. Quando **EnabledState** è impostato su 5 ("Non applicabile"), questa proprietà non ha alcun significato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 ("Non applicabile").

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Larghezza di banda corrente della porta, in bit al secondo. Per le porte che variano in larghezza di banda o per quelle in cui non è possibile eseguire stime accurate, questa proprietà deve contenere la larghezza di banda nominale. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 10000000000.

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
</dt> </dl>

Stringhe che descrivono i vari **valori della matrice OperationalStatus.** Le voci in questa matrice sono correlate a quelle nello stesso indice di matrice in **OperationalStatus.** Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("Byte")
</dt> </dl>

Unità massima di trasmissione (MTU) che può essere supportata, in byte. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 1500.

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

ID macchina virtuale in **formato GUID.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'ultima **modifica di EnabledState** dell'elemento. Se lo stato dell'elemento non è stato modificato e questa proprietà viene popolata, deve essere impostata su un valore di intervallo pari a 0. Se una modifica dello stato è stata richiesta, ma rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene usata.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di ore di alimentazione del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene usata.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui l'istanza è in fase di transizione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))ma non viene usata.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end. Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 ("Senza restrizioni"). Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ed è sempre impostata su 4 ("Senza restrizioni").

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ EmulatedEthernetPort** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ EthernetPort**](cim-ethernetport.md)
</dt> <dt>

[**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

