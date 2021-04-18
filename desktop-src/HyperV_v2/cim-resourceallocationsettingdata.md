---
description: Rappresenta le impostazioni per una risorsa allocata che non rientrano nell'ambito della classe CIM utilizzata in genere per rappresentare la risorsa stessa.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: Classe CIM_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312332"
---
# <a name="cim_resourceallocationsettingdata-class"></a>CIM \_ ResourceAllocationSettingData (classe)

Rappresenta le impostazioni per una risorsa allocata che non rientrano nell'ambito della classe CIM utilizzata in genere per rappresentare la risorsa stessa. Queste impostazioni includono informazioni specifiche dell'allocazione che potrebbero non essere visibili al consumer della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a>Members

La classe **CIM \_ ResourceAllocationSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ResourceAllocationSettingData** dispone di queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa, ad esempio l'indirizzo MAC di una porta Ethernet.

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa dal contesto dell'elemento padre. Questa proprietà viene utilizzata per descrivere una relazione del controller e l'ordine dei dispositivi in un controller. Se, ad esempio, l'elemento padre è un controller PCI, questa proprietà specifica lo slot PCI del dispositivo figlio.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Reservation**","**CIM \_ ResourceAllocationSettingData**.**Limite**"), **IsPUnit**
</dt> </dl>

Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** per allocare automaticamente la risorsa; in caso contrario, **false**.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** per deallocare automaticamente la risorsa; in caso contrario, **false**.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che indica gli oggetti connessi alla risorsa, ad esempio una rete denominata o una porta di commutazione.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La visibilità dei consumer per la risorsa allocata.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

**Passato** (2)


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

**Virtualizzato** (3)


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

**Non rappresentata** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32767.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**","**CIM \_ ResourceAllocationSettingData**.**MappingBehavior**")
</dt> </dl>

Matrice che contiene l'assegnazione delle risorse allocate. Ogni valore non null di questa proprietà deve essere formattato come URI basato su RFC3986. Se la risorsa è modellata, il valore deve essere un URI WBEM.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")
</dt> </dl>

Quantità massima di risorse da concedere all'allocazione. Il tipo di unità di questa proprietà è specificato dalla proprietà **AllocationUnits** .

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non supportato** (2)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**Dedicato** (3)


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

**Affinità Soft** (4)


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

**Affinità hardware** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32767.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")
</dt> </dl>

Descrizione del tipo di risorsa quando la proprietà **ResourceType** è impostata su 1 (other).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre della risorsa, ad esempio un controller per l'allocazione corrente.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**")
</dt> </dl>

ID del pool di risorse che ha generato la risorsa.

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")
</dt> </dl>

Il numero di risorse di cui è garantita la disponibilità per l'allocazione. Nei sistemi che supportano l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione.

Il tipo di unità di questa proprietà è specificato dalla proprietà **AllocationUnits** .

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")
</dt> </dl>

Sottotipo specifico di implementazione per questa risorsa. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**","**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**")
</dt> </dl>

Tipo di risorsa rappresentata dalle impostazioni di allocazione.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

**Computer System** (2)


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

**Processore** (3)


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

**Memoria** (4)


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

**Controller IDE** (5)


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

**HBA SCSI parallelo** (6)


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

**HBA FC** (7)


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

**HBA iSCSI** (8)


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

**IB HCA** (9)


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

**Scheda Ethernet** (10)


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

**Altra scheda di rete** (11)


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

**Slot I/O** (12)


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

**Dispositivo I/O** (13)


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

**Unità floppy** (14)


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

**Unità CD** (15)


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

**Unità DVD** (16)


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unità disco** (17)


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

**Unità nastro** (18)


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

**Extent di archiviazione** (19)


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

**Altro dispositivo di archiviazione** (20)


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

**Porta seriale** (21)


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Porta parallela** (22)


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

**Controller USB** (23)


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

**Controller grafica** (24)


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

**Controller IEEE 1394** (25)


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

**Unità partizionabile** (26)


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

**Unità partizionabile di base** (27)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

**Potenza** (28)


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

**Capacità di raffreddamento** (29)


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

**Porta switch Ethernet** (30)


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

**Disco logico** (31)


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

**Volume di archiviazione** (32)


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

**Connessione Ethernet** (33)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Il numero di risorse presentate al consumer della risorsa.

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Unità utilizzate dalla proprietà **VirtualQuantity** .

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

