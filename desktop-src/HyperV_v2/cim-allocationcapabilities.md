---
description: Rappresenta le impostazioni di allocazione delle risorse di un elemento gestito per un tipo di risorsa specifico.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: Classe CIM_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305676"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="54f41-103">CIM \_ AllocationCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="54f41-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="54f41-104">Rappresenta le impostazioni di allocazione delle risorse di un elemento gestito per un tipo di risorsa specifico.</span><span class="sxs-lookup"><span data-stu-id="54f41-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54f41-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="54f41-106">Members</span><span class="sxs-lookup"><span data-stu-id="54f41-106">Members</span></span>

<span data-ttu-id="54f41-107">La classe **CIM \_ AllocationCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54f41-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="54f41-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54f41-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54f41-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54f41-109">Properties</span></span>

<span data-ttu-id="54f41-110">La classe **CIM \_ AllocationCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="54f41-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54f41-111">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="54f41-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54f41-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f41-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f41-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="54f41-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="54f41-115">Il tipo di risorsa per questa impostazione di allocazione quando la proprietà **ResourceType** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="54f41-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="54f41-116">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="54f41-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f41-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f41-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f41-119">Indica se è supportata la richiesta di una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="54f41-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f41-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="54f41-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="54f41-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specifico** (2)</span><span class="sxs-lookup"><span data-stu-id="54f41-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="54f41-122">La richiesta può includere una richiesta per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="54f41-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="54f41-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**Generale** (3)</span><span class="sxs-lookup"><span data-stu-id="54f41-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="54f41-124">La richiesta non include risorse specifiche.</span><span class="sxs-lookup"><span data-stu-id="54f41-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="54f41-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Entrambi** (4)</span><span class="sxs-lookup"><span data-stu-id="54f41-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="54f41-126">Sono supportate sia richieste specifiche che richieste generali.</span><span class="sxs-lookup"><span data-stu-id="54f41-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f41-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="54f41-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f41-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="54f41-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f41-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="54f41-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54f41-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f41-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f41-132">Descrizione di un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="54f41-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="54f41-133">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="54f41-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="54f41-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="54f41-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f41-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f41-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f41-137">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AllocationCapabilities**.**OtherResourceType**","[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="54f41-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="54f41-138">Tipo di risorsa assegnato a questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="54f41-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="54f41-139">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="54f41-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="54f41-140">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="54f41-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="54f41-141">**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="54f41-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="54f41-142">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="54f41-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="54f41-143">**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="54f41-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="54f41-144">**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="54f41-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="54f41-145">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="54f41-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="54f41-146">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="54f41-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="54f41-147">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="54f41-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="54f41-148">**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="54f41-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="54f41-149">**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="54f41-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="54f41-150">**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="54f41-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="54f41-151">**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="54f41-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="54f41-152">**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="54f41-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="54f41-153">**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="54f41-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="54f41-154">**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="54f41-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="54f41-155">**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="54f41-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="54f41-156">**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="54f41-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="54f41-157">**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="54f41-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="54f41-158">**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="54f41-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="54f41-159">**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="54f41-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="54f41-160">**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="54f41-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="54f41-161">**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="54f41-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="54f41-162">**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="54f41-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="54f41-163">**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="54f41-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="54f41-164">**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="54f41-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="54f41-165">**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="54f41-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="54f41-166">**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="54f41-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="54f41-167">**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="54f41-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="54f41-168">**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="54f41-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="54f41-169">**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="54f41-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="54f41-170">**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="54f41-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="54f41-171">**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="54f41-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f41-172">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="54f41-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f41-173">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="54f41-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f41-174">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="54f41-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-175">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f41-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f41-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f41-177">Indica il modo in cui viene concesso l'accesso alla risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="54f41-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="54f41-178">La quantità effettiva è controllata da min, dimensioni massime, pesi e così via.</span><span class="sxs-lookup"><span data-stu-id="54f41-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f41-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="54f41-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="54f41-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (2)</span><span class="sxs-lookup"><span data-stu-id="54f41-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="54f41-181">Accesso esclusivo alla risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="54f41-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="54f41-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Condiviso** (3)</span><span class="sxs-lookup"><span data-stu-id="54f41-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="54f41-183">Uso condiviso della risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="54f41-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f41-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="54f41-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f41-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="54f41-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f41-186">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="54f41-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-187">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f41-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54f41-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f41-189">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="54f41-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="54f41-190">Gli Stati del sistema supportati quando viene creata una nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="54f41-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f41-191">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="54f41-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="54f41-192">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="54f41-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="54f41-193">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="54f41-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="54f41-194">**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="54f41-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="54f41-195">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="54f41-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="54f41-196">**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="54f41-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="54f41-197">**In test** (7)</span><span class="sxs-lookup"><span data-stu-id="54f41-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="54f41-198">**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="54f41-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="54f41-199">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="54f41-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="54f41-200">**Avvio** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="54f41-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="54f41-201">In **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="54f41-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="54f41-202">**Sospeso** (12)</span><span class="sxs-lookup"><span data-stu-id="54f41-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f41-203">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="54f41-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f41-204">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="54f41-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f41-205">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="54f41-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f41-206">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f41-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54f41-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54f41-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f41-208">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="54f41-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="54f41-209">Gli Stati del sistema supportati quando una risorsa viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="54f41-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f41-210">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="54f41-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="54f41-211">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="54f41-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="54f41-212">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="54f41-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="54f41-213">**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="54f41-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="54f41-214">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="54f41-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="54f41-215">**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="54f41-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="54f41-216">**In test** (7)</span><span class="sxs-lookup"><span data-stu-id="54f41-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="54f41-217">**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="54f41-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="54f41-218">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="54f41-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="54f41-219">**Avvio** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="54f41-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="54f41-220">In **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="54f41-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="54f41-221">**Sospeso** (12)</span><span class="sxs-lookup"><span data-stu-id="54f41-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f41-222">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="54f41-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f41-223">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="54f41-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="54f41-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54f41-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="54f41-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54f41-225">Requirements</span></span>



| <span data-ttu-id="54f41-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="54f41-226">Requirement</span></span> | <span data-ttu-id="54f41-227">Valore</span><span class="sxs-lookup"><span data-stu-id="54f41-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f41-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54f41-228">Minimum supported client</span></span><br/> | <span data-ttu-id="54f41-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="54f41-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="54f41-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54f41-230">Minimum supported server</span></span><br/> | <span data-ttu-id="54f41-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54f41-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="54f41-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54f41-232">Namespace</span></span><br/>                | <span data-ttu-id="54f41-233">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="54f41-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54f41-234">MOF</span><span class="sxs-lookup"><span data-stu-id="54f41-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54f41-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54f41-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54f41-236">DLL</span><span class="sxs-lookup"><span data-stu-id="54f41-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54f41-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54f41-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54f41-238">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54f41-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f41-239">**\_Funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="54f41-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

