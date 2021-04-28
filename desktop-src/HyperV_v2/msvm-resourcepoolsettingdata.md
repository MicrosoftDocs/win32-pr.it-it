---
description: "Msvm_ResourcePoolSettingData classe: rappresenta le impostazioni di un'istanza \\_ di Msvm ResourcePool che non sono correlate all'allocazione."
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Msvm_ResourcePoolSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4fba27ec5c12e0c3cb18b8a6dfd4a863e59cad62
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111509"
---
# <a name="msvm_resourcepoolsettingdata-class"></a>Classe \_ Msvm ResourcePoolSettingData

Rappresenta le impostazioni di [**un'istanza di Msvm \_ ResourcePool**](msvm-resourcepool.md) che non sono correlate all'allocazione.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ResourcePoolSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ResourcePoolSettingData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**LoadBalancingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la strategia di allocazione che deve essere usata dal pool di risorse per bilanciare l'utilizzo delle risorse tra le risorse aggregate. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)
</dt> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (3)
</dt> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distribuito** (4)
</dt> <dt>

<span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidato** (5 )
</dt> </dl>

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il pool di risorse può tentare di usare altre risorse host per soddisfare la richiesta di allocazione se non è possibile allocare le risorse desiderate. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (3)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinità soft** (4)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinità rigida** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )
</dt> </dl>

</dd> <dt>

**MappingOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ordine in cui verranno selezionate le risorse host disponibili tramite questo pool quando si tenta di soddisfare una richiesta di allocazione e la risorsa host richiesta non è disponibile o non viene specificata alcuna risorsa host. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note fornite dall'utente finale correlate a questo pool di risorse. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su 0 (Altro). Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore per il pool. Questa proprietà viene usata per fornire la correlazione tra il salvataggio e il ripristino dei dati di configurazione nell'archiviazione permanente sottostante. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive un sottotipo specifico dell'implementazione per questo pool. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risorsa che il pool di risorse può allocare. Questa proprietà viene ereditata da [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallela** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di** rete (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot di I/O** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo di I/O** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di** archiviazione (19)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di** archiviazione (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafico** (24)
</dt> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)
</dt> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Alimentazione** (28)
</dt> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacità di raffreddamento** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta commutatore Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)
</dt> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF )
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 solo \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2012 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

