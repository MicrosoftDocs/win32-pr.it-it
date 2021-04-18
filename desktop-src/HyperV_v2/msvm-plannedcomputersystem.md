---
description: Rappresenta una macchina virtuale pianificata.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318312"
---
# <a name="msvm_plannedcomputersystem-class"></a>\_Classe MSVM PlannedComputerSystem

Rappresenta una macchina virtuale pianificata.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a>Members

La **classe \_ PlannedComputerSystem di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ PlannedComputerSystem di MSVM** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-plannedcomputersystem.md) | Richiede che lo stato del sistema pianificato venga modificato nel valore specificato.<br/> |
| **SetPowerState**                                                           | Questo metodo non è supportato.<br/>                                                    |



 

### <a name="properties"></a>Proprietà

La **classe \_ PlannedComputerSystem di MSVM** dispone di queste proprietà.

<dl> <dt>

**AssignedNumaNodeList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di nodi NUMA (non-Uniform Memory Access) attualmente assegnati alla macchina virtuale.

</dd> <dt>

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

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "macchina virtuale pianificata".

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
</dt> <dt>

Qualificatori: **Key**, **maxlen** (256)
</dt> </dl>

Indica il nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**Dedicato**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di valori che indica gli scopi a cui è dedicato il sistema pianificato, se presente, e la funzionalità fornita. Ad esempio, è possibile specificare che il sistema è dedicato a "Print" (valore = 11) o funge da "hub" (valore = 8). È anche possibile indicare più scopi. Ad esempio, si tratta di un sistema per utilizzo generico che indica "non dedicato" (valore = 0) ma che ospita anche "stampa" (valore = 11) o "dispositivo utente mobile" (valore = 17) servizi.

Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .



| Valore                                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <dt>**Non dedicato**</dt> <dt>0</dt> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>1</dt> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>2</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <dt>**Archiviazione**</dt> <dt>3</dt> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <dt>**Router**</dt> <dt>4</dt> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <dt>**Switch**</dt> <dt>5</dt> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <dt>**Switch di livello 3**</dt> <dt>6</dt> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <dt>**Switch ufficio centrale**</dt> <dt>7</dt> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <dt>**Hub**</dt> <dt>8</dt> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <dt>**Accesso al server**</dt> <dt>9</dt> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <dt>**Firewall**</dt> <dt>10</dt> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <dt>**Stampa**</dt> <dt>11</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <dt>**I/O**</dt> <dt>12</dt> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <dt>**Caching Web**</dt> <dt>13</dt> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <dt>**Gestione**</dt> <dt>14</dt> </dl>                                                                 | Indica che questa istanza è dedicata all'hosting del software di gestione del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <dt>**Blocca server**</dt> <dt>15</dt> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <dt>**File server**</dt> <dt>16</dt> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <dt>**Dispositivo utente mobile**</dt> <dt>17</dt> </dl>                                 | Un esempio di dispositivo utente mobile dedicato è un telefono cellulare o uno scanner di codice a barre in un negozio che comunica tramite frequenza radio. Questi sistemi sono molto limitati in funzionalità e programmabilità e non sono considerati piattaforme di elaborazione per utilizzo generico. In alternativa, un esempio di sistema mobile che è generico (ovvero, non è dedicato) è un computer portatile. Sebbene sia limitato nella programmabilità, è possibile scaricare il nuovo software e la relativa funzionalità espanso dall'utente. <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <dt>**Repeater**</dt> <dt>18</dt> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <dt>**Bridge/Extender**</dt> <dt>19</dt> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <dt>**Gateway**</dt> <dt>20</dt> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <dt>**Virtualizzatore archiviazione**</dt> <dt>21</dt> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <dt>**Libreria multimediale**</dt> <dt>22</dt> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <dt>**ExtenderNode**</dt> <dt>23</dt> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <dt>**Server principale**</dt> <dt>24</dt> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <dt>**NAS autonomo**</dt> <dt>25</dt> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <dt>**UPS**</dt> <dt>26</dt> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <dt>**Telefono IP**</dt> <dt>27</dt> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <dt>**Controller di gestione**</dt> <dt>28</dt> </dl>                     | Indica che questa istanza rappresenta hardware specializzato dedicato alla gestione dei sistemi, ovvero un controller di gestione (BMC) o un processore di servizi di battiscopa. L'ambito di gestione di un controller di gestione è in genere un singolo sistema gestito in cui è contenuto.<br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <dt>**Gestione chassis**</dt> <dt>29</dt> </dl>                                             | Indica che questa istanza rappresenta un sistema dedicato alla gestione di uno chassis del pannello e dei relativi dispositivi contenuti. Questo valore verrebbe utilizzato per rappresentare un controller di scaffale. Uno chassis Manager è un punto di aggregazione per la gestione e può basarsi su controller di gestione subordinati per la gestione di parti costituenti. <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <dt>**Controller RAID basato su host**</dt> <dt>30</dt> </dl> | Indica che questa istanza rappresenta un controller di archiviazione RAID contenuto in un computer host.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <dt>**Enclosure del dispositivo di archiviazione**</dt> <dt>31</dt> </dl>         | Indica che questa istanza rappresenta un'enclosure che contiene dispositivi di archiviazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <dt>**Desktop**</dt> <dt>32</dt> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <dt>**Portatile**</dt> <dt>33</dt> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <dt>**Libreria di nastri virtuale**</dt> <dt>34</dt> </dl>                         | Emulazione di una libreria di nastri da parte di un sistema di libreria virtuale. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <dt>**Sistema di libreria virtuale**</dt> <dt>35</dt> </dl>                 | Usa l'archiviazione su disco per emulare le librerie di nastri.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <dt>**PC di rete/Thin Client**</dt> <dt>36</dt> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <dt>**Switch FC**</dt> <dt>37</dt> </dl>                                                                     | Indica che questa istanza è dedicata al cambio di frame Fibre Channel di livello 2. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <dt>**Switch Ethernet**</dt> <dt>38</dt> </dl>                                             | Indica che questa istanza è dedicata al cambio di frame Ethernet di livello 2. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>39.. 32567</dt> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32568 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "macchina virtuale pianificata Microsoft".

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

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). i possibili valori sono i seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | Il sistema è disattivato.<br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | Il sistema è abilitato, ma non è in linea. Tutte le nuove richieste verranno eliminate.<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica lo stato abilitato del sistema pianificato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | Il sistema è disattivato.<br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | Il sistema è abilitato, ma non è in linea. Tutte le nuove richieste verranno eliminate.<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti. I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).



| Valore                                                                        | Significato                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | Lo stato di integrità è Normal.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che forniscono spiegazioni e dettagli dietro le voci della matrice **OtherIdentifyingInfo** . Ogni voce di questa matrice è correlata alla voce in **OtherIdentifyingInfo** che si trova nello stesso indice. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**, **override**, **maxlen** (256)
</dt> </dl>

Il nome ereditato funge da chiave di un'istanza di sistema in un ambiente aziendale. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Identifica il modo in cui è stato generato il nome di sistema, usando l'euristica della sottoclasse. L'oggetto di sistema e i relativi derivati sono oggetti di primo livello di CIM. Forniscono l'ambito per numerosi componenti. È necessario disporre di chiavi di sistema univoche. È possibile definire un'euristica nelle singole sottoclassi di sistema per tentare di generare sempre la stessa chiave del nome di sistema. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")
</dt> </dl>

Tempo totale, in millisecondi, dall'ultima volta in cui la macchina virtuale è stata attivata, reimpostata o ripristinata. Questa volta esclude l'ora in cui la macchina virtuale è in stato di sospensione.

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

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive come o perché il sistema è dedicato quando la matrice dedicata include il valore 2, ovvero "altro". Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro"). Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key**, **maxlen** (256)
</dt> </dl>

Contiene dati aggiuntivi, oltre alle informazioni sul nome del sistema, che possono essere usati per identificare un ComputerSystem. Un esempio è quello di contenere il nome Fibre Channel universale (WWN) di un nodo. Se solo il nome del Fibre Channel è disponibile ed è univoco (in grado di essere usato come chiave di sistema), questa proprietà sarà **null** e WWN diventerebbe la chiave di sistema, i dati inseriti nella proprietà **Name** . Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , ma non è supportata.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **maxlen** (256)
</dt> </dl>

Stringa che fornisce informazioni sul modo in cui il proprietario del sistema primario può essere raggiunto, ad esempio numero di telefono, indirizzo di posta elettronica e così via. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Nome del proprietario del sistema primario. Il proprietario del sistema è l'utente principale del sistema. Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

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

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato da **EnabledState**. Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento. Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** . In tal caso, viene utilizzato il valore 12 ("non applicabile"). Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).



| Valore                                                                         | Significato                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Non applicabile.<br/> |



 

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le funzionalità di reimpostazione del computer. Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .



| Valore                                                                                                                                                                                                                                                            | Significato                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>2</dt> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                  | La reimpostazione dell'hardware non è consentita. <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>4</dt> </dl>                                      | Il sistema del computer può essere reimpostato utilizzando l'hardware (ad esempio, i pulsanti Power e reset). <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <dt> **Non implementato**</dt> <dt>5</dt> </dl> |                                                                                                            |



 

</dd> <dt>

**Ruoli**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice di stringhe che specifica i ruoli definiti dall'amministratore che questo sistema riproduce nell'ambiente gestito. Esempi potrebbero essere "Building 8 Server di stampa" o "directory utente Boise". Un singolo sistema può eseguire più ruoli. La visualizzazione strumentazione dei ruoli di un sistema viene definita creando un'istanza di una sottoclasse specifica di System o dalle proprietà in una sottoclasse oppure entrambe. Ad esempio, lo scopo di un ComputerSystem viene definito usando le proprietà **Dedicated** e **OtherDedicatedDescription** . Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .

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
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "il servizio è in esecuzione normalmente".

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

Data e ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).



| Valore                                                                                                                                                                                                                                                     | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <dt>**Arresta**</dt> <dt>4</dt> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <dt>**Nessuna modifica**</dt> <dt>5</dt> </dl>                       | Non è in corso alcuna transizione.<br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <dt>**Offline**</dt> <dt>6</dt> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <dt>**Test**</dt> <dt>7</dt> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <dt>**Rinvia**</dt> <dt>8</dt> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Mettere in stato**</dt> <dt>9</dt> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <dt>**Riavvio**</dt> <dt>10</dt> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <dt>**Reimposta**</dt> <dt>11</dt> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>12</dt> </dl>  | L'implementazione non supporta la rappresentazione delle transizioni in corso.<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **DMTF riservato**</dt> <dt>..</dt> </dl> |                                                                                  |



 

</dd> </dl>

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

[**\_VirtualSystemManagementService MSVM. Metodo ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

