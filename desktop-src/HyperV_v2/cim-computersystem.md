---
description: Rappresenta una raccolta che fornisce funzionalità di elaborazione ed è costituita da \_ oggetti MANAGEDSYSTEMELEMENT CIM.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Classe CIM_ComputerSystem (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319058"
---
# <a name="cim_computersystem-class-hyper-v-management"></a>Classe CIM_ComputerSystem (gestione Hyper-V)

Rappresenta una raccolta che fornisce funzionalità di elaborazione ed è costituita da oggetti [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a>Members

La classe **CIM \_ ComputerSystem** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ ComputerSystem** presenta questi metodi.



| Metodo                                                    | Descrizione                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetPowerState**](cim-computersystem-setpowerstate.md) | Questo metodo è deprecato. Usare invece il metodo **RequestPowerStateChange** nella classe **CIM \_ PowerManagementService** .<br/> **Descrizione deprecata:** Imposta lo stato di alimentazione del computer.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ ComputerSystem** dispone di queste proprietà.

<dl> <dt>

**Dedicato**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. INCIs-T11 \| Platform \| PlatformType "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**OtherDedicatedDescriptions**")
</dt> </dl>

Lo scopo e le funzionalità del sistema informatico. Ad esempio, un sistema dedicato alla stampa potrebbe specificare "11" (Print). Un sistema di utilizzo generico con funzionalità di stampa può essere impostato su "0" (non dedicato) e "11" (Print).

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Non dedicato** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (2)


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Archiviazione** (3)


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Switch di livello 3** (6)


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Switch ufficio centrale** (7)


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Server di accesso** (9)


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Stampa** (11)


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span id="I_O"></span><span id="i_o"></span>**I/O** (12)


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Caching Web** (13)


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Gestione** (14)


</dt> <dd>

Questa istanza è dedicata all'hosting del software di gestione del sistema

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Blocca server** (15)


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File server** (16)


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Dispositivo utente mobile** (17)


</dt> <dd>

Un esempio di dispositivo utente dedicato è un telefono cellulare o uno scanner di codice a barre in un negozio che comunica tramite frequenza radio. Questi sistemi sono molto limitati in funzionalità e programmabilità e non sono considerati piattaforme di elaborazione "per utilizzo generico". In alternativa, un esempio di sistema mobile che è "utilizzo generico" (ad esempio, non è dedicato) è un computer portatile. Sebbene sia limitato nella programmabilità, è possibile scaricare il nuovo software e la relativa funzionalità espanso dall'utente.

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Ripetitore** (18)


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualizzatore di archiviazione** (21)


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Catalogo multimediale** (22)


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Testa NAS** (24)


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**NAS autonomo** (25)


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span id="UPS"></span><span id="ups"></span>**UPS** (26)


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Telefono IP** (27)


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Controller di gestione** (28)


</dt> <dd>

Questa istanza rappresenta hardware specializzato dedicato alla gestione dei sistemi, ad esempio un controller di gestione (BMC) o un processore di servizi di battiscopa.

L'ambito di gestione di un "controller di gestione" è in genere un singolo sistema gestito in cui è contenuto.

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Gestione chassis** (29)


</dt> <dd>

Questa istanza rappresenta un sistema dedicato alla gestione di uno chassis del pannello e dei relativi dispositivi contenuti. Questo valore verrebbe utilizzato per rappresentare un controller di scaffale. Un "gestore dello chassis" è un punto di aggregazione per la gestione e può basarsi su controller di gestione subordinati per la gestione delle parti costituenti.

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Controller RAID basato su host** (30)


</dt> <dd>

Questa istanza rappresenta un controller di archiviazione RAID contenuto in un computer host.

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Enclosure dispositivi di archiviazione** (31)


</dt> <dd>

Questa istanza rappresenta un'enclosure che contiene dispositivi di archiviazione.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portatile** (33)


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Libreria di nastri virtuale** (34)


</dt> <dd>

Emulazione di una libreria di nastri da parte di un sistema di libreria virtuale.

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Sistema di libreria virtuale** (35)


</dt> <dd>

Usa l'archiviazione su disco per emulare le librerie di nastri

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC di rete/thin client** (36)


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Switch FC** (37)


</dt> <dd>

Dedicato al cambio di frame Fibre Channel di livello 2.

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Switch Ethernet** (38)


</dt> <dd>

Dedicato al cambio di frame Ethernet di livello 2

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32568.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Formato del nome del sistema del computer.

<dt>



 ("Altro")


</dt> <dd></dd> <dt>



 ("IP")


</dt> <dd></dd> <dt>



 ("Dial")


</dt> <dd></dd> <dt>



 ("HID")


</dt> <dd></dd> <dt>



 ("NWA")


</dt> <dd></dd> <dt>



 ("HWA")


</dt> <dd></dd> <dt>



 ("X25")


</dt> <dd></dd> <dt>



 ("ISDN")


</dt> <dd></dd> <dt>



 ("IPX")


</dt> <dd></dd> <dt>



 ("DCC")


</dt> <dd></dd> <dt>



 ("ICD")


</dt> <dd></dd> <dt>



 ("E. 164")


</dt> <dd></dd> <dt>



 ("SNA")


</dt> <dd></dd> <dt>



 ("OID/OSI")


</dt> <dd></dd> <dt>



 ("WWN")


</dt> <dd></dd> <dt>



 ("NAA")


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Dedicato**")
</dt> </dl>

Viene descritto come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controlli di alimentazione del sistema DMTF \| 001,2 ")
</dt> </dl>

Questa proprietà è deprecata. Usare invece il metodo **PowerChangeCapabilities** nella classe **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** .

**Descrizione deprecata:** Funzionalità di risparmio energia del sistema.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non supportato** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Modalità di risparmio energia immesse automaticamente** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Stato di alimentazione impostabile** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Power Cycling supportato** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Alimentazione temporizzata supportata** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sicurezza hardware del sistema DMTF \| 001,4 ")
</dt> </dl>

Indica se il sistema supporta l'operazione di reimpostazione dell'hardware.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Non implementato** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Sistema CIM**](cim-system.md)
</dt> </dl>

 

