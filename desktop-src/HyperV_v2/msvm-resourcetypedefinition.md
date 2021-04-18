---
description: Definisce un mapping di un tipo di risorsa alle relative classi di implementazione.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Classe Msvm_ResourceTypeDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314826"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="0bb64-103">\_Classe MSVM ResourceTypeDefinition</span><span class="sxs-lookup"><span data-stu-id="0bb64-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="0bb64-104">Definisce un mapping di un tipo di risorsa alle relative classi di implementazione.</span><span class="sxs-lookup"><span data-stu-id="0bb64-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="0bb64-105">La sintassi seguente è semplificata Managed Object Format codice (MOF).</span><span class="sxs-lookup"><span data-stu-id="0bb64-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb64-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bb64-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="0bb64-107">Members</span><span class="sxs-lookup"><span data-stu-id="0bb64-107">Members</span></span>

<span data-ttu-id="0bb64-108">La **classe \_ ResourceTypeDefinition di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0bb64-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="0bb64-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb64-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bb64-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb64-110">Properties</span></span>

<span data-ttu-id="0bb64-111">La **classe \_ ResourceTypeDefinition di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0bb64-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bb64-112">**LogicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="0bb64-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb64-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0bb64-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb64-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb64-115">Nome della classe derivata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che implementa il dispositivo logico per questo tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bb64-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="0bb64-116">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0bb64-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb64-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0bb64-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb64-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-119">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0bb64-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0bb64-120">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0bb64-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="0bb64-121">Esiste una corrispondenza con la proprietà **OtherResourceType** di [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0bb64-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0bb64-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="0bb64-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb64-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0bb64-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb64-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-125">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0bb64-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0bb64-126">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bb64-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="0bb64-127">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bb64-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="0bb64-128">Esiste una corrispondenza con la proprietà **ResourceSubType** di [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0bb64-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0bb64-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0bb64-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb64-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bb64-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb64-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-132">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0bb64-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0bb64-133">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="0bb64-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="0bb64-134">Esiste una corrispondenza con la proprietà **ResourceType** di [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0bb64-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="0bb64-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bb64-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="0bb64-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="0bb64-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="0bb64-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="0bb64-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="0bb64-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="0bb64-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="0bb64-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="0bb64-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="0bb64-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="0bb64-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="0bb64-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="0bb64-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="0bb64-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="0bb64-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="0bb64-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (17)</span><span class="sxs-lookup"><span data-stu-id="0bb64-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (18)</span><span class="sxs-lookup"><span data-stu-id="0bb64-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (19)</span><span class="sxs-lookup"><span data-stu-id="0bb64-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (20)</span><span class="sxs-lookup"><span data-stu-id="0bb64-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (21)</span><span class="sxs-lookup"><span data-stu-id="0bb64-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="0bb64-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Nastro** (23)</span><span class="sxs-lookup"><span data-stu-id="0bb64-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (24)</span><span class="sxs-lookup"><span data-stu-id="0bb64-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controller FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="0bb64-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="0bb64-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="0bb64-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)</span><span class="sxs-lookup"><span data-stu-id="0bb64-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="0bb64-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="0bb64-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="0bb64-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0bb64-166">**SettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="0bb64-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb64-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0bb64-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bb64-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb64-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb64-169">Nome della classe derivata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che implementa le impostazioni per questo tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0bb64-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bb64-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bb64-170">Remarks</span></span>

<span data-ttu-id="0bb64-171">L'accesso alla **classe \_ ResourceTypeDefinition di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0bb64-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0bb64-172">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0bb64-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb64-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bb64-173">Requirements</span></span>



| <span data-ttu-id="0bb64-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb64-174">Requirement</span></span> | <span data-ttu-id="0bb64-175">Valore</span><span class="sxs-lookup"><span data-stu-id="0bb64-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb64-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb64-176">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb64-177">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0bb64-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0bb64-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb64-178">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb64-179">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0bb64-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bb64-180">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0bb64-180">End of client support</span></span><br/>    | <span data-ttu-id="0bb64-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0bb64-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0bb64-182">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0bb64-182">End of server support</span></span><br/>    | <span data-ttu-id="0bb64-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0bb64-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0bb64-184">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bb64-184">Namespace</span></span><br/>                | <span data-ttu-id="0bb64-185">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0bb64-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0bb64-186">MOF</span><span class="sxs-lookup"><span data-stu-id="0bb64-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bb64-187"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bb64-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bb64-188">DLL</span><span class="sxs-lookup"><span data-stu-id="0bb64-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bb64-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0bb64-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

