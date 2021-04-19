---
description: Definisce i mezzi mediante i quali un client può individuare l'intervallo valido di impostazioni predefinite per una risorsa virtuale.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Classe Msvm_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317767"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="639d8-103">\_Classe MSVM AllocationCapabilities</span><span class="sxs-lookup"><span data-stu-id="639d8-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="639d8-104">Definisce i mezzi mediante i quali un client può individuare l'intervallo valido di impostazioni predefinite per una risorsa virtuale.</span><span class="sxs-lookup"><span data-stu-id="639d8-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="639d8-105">Un oggetto **MSVM \_ AllocationCapabilities** è associato a ogni pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="639d8-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="639d8-106">Quattro [**oggetti \_ ResourceAllocationSettingData di MSVM**](msvm-resourceallocationsettingdata.md) sono associati all'oggetto **MSVM \_ AllocationCapabilities** per descrivere i valori minimo, massimo, predefinito e incrementale per l'allocazione della risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="639d8-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="639d8-107">Insieme, queste classi descrivono la gamma complessiva di funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="639d8-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="639d8-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="639d8-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="639d8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="639d8-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="639d8-110">Members</span><span class="sxs-lookup"><span data-stu-id="639d8-110">Members</span></span>

<span data-ttu-id="639d8-111">La **classe \_ AllocationCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="639d8-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="639d8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="639d8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="639d8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="639d8-113">Properties</span></span>

<span data-ttu-id="639d8-114">La **classe \_ AllocationCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="639d8-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="639d8-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="639d8-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="639d8-118">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="639d8-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="639d8-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="639d8-119">A short description of the object.</span></span> <span data-ttu-id="639d8-120">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="639d8-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="639d8-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-124">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="639d8-124">A description of the object.</span></span> <span data-ttu-id="639d8-125">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="639d8-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="639d8-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-129">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="639d8-129">A display name for the object.</span></span> <span data-ttu-id="639d8-130">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="639d8-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="639d8-131">Anche la proprietà [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) della classe **CIM \_ ManagedSystemElement** è definita come nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="639d8-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="639d8-132">Tuttavia, è spesso sottoclassato come una chiave.</span><span class="sxs-lookup"><span data-stu-id="639d8-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="639d8-133">Non è ragionevole che la stessa proprietà possa fornire identità e un nome visualizzato, senza incoerenze.</span><span class="sxs-lookup"><span data-stu-id="639d8-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="639d8-134">Dove [**Name**](msvm-keyboard.md) esiste e non è una chiave, ad esempio per le istanze di un dispositivo logico, le stesse informazioni possono essere presenti nelle proprietà **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="639d8-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="639d8-135">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="639d8-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="639d8-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-139">Identificatore univoco per questo pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="639d8-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="639d8-140">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="639d8-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-141">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="639d8-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-144">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore "other".</span><span class="sxs-lookup"><span data-stu-id="639d8-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="639d8-145">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-146">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="639d8-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="639d8-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-149">Indica se è supportata la richiesta di una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="639d8-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="639d8-150">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="639d8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="639d8-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="639d8-152">Significato</span><span class="sxs-lookup"><span data-stu-id="639d8-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="639d8-153"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="639d8-154">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="639d8-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="639d8-155"><dt>**Specifica**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="639d8-156">La richiesta può includere una richiesta per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="639d8-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="639d8-157"><dt>**Generale**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="639d8-158">La richiesta non include una richiesta per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="639d8-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="639d8-159"><dt>**Entrambi**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="639d8-160">Sono supportate sia richieste specifiche che richieste generali.</span><span class="sxs-lookup"><span data-stu-id="639d8-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="639d8-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="639d8-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="639d8-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-164">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="639d8-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="639d8-165">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="639d8-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="639d8-166">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="639d8-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="639d8-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="639d8-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-170">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="639d8-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="639d8-171">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="639d8-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="639d8-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="639d8-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="639d8-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="639d8-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="639d8-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="639d8-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="639d8-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="639d8-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="639d8-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="639d8-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="639d8-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="639d8-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="639d8-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="639d8-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="639d8-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="639d8-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="639d8-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="639d8-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="639d8-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="639d8-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="639d8-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="639d8-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="639d8-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="639d8-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="639d8-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="639d8-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="639d8-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="639d8-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="639d8-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="639d8-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="639d8-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="639d8-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="639d8-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="639d8-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="639d8-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="639d8-207">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="639d8-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="639d8-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="639d8-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-210">Indica il modo in cui viene concesso l'accesso a una risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="639d8-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="639d8-211">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="639d8-212">Valore</span><span class="sxs-lookup"><span data-stu-id="639d8-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="639d8-213">Significato</span><span class="sxs-lookup"><span data-stu-id="639d8-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="639d8-214"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="639d8-215">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="639d8-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="639d8-216"><dt>**Dedicato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="639d8-217">Accesso esclusivo a una risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="639d8-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="639d8-218"><dt>**Condiviso**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="639d8-219">Uso condiviso di una risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="639d8-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="639d8-220">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="639d8-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-221">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="639d8-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="639d8-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-223">Indica gli Stati a cui il sistema a cui verrà associata la risorsa può trovarsi quando viene creata una nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="639d8-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="639d8-224">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="639d8-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="639d8-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="639d8-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="639d8-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="639d8-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="639d8-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="639d8-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (7)</span><span class="sxs-lookup"><span data-stu-id="639d8-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="639d8-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="639d8-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="639d8-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="639d8-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (12)</span><span class="sxs-lookup"><span data-stu-id="639d8-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="639d8-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="639d8-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="639d8-239">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="639d8-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="639d8-240">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="639d8-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="639d8-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="639d8-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="639d8-242">Indica gli Stati a cui il sistema a cui è associata la risorsa può trovarsi quando la risorsa viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="639d8-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="639d8-243">Questa proprietà viene ereditata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="639d8-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="639d8-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="639d8-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="639d8-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="639d8-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="639d8-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="639d8-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="639d8-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (7)</span><span class="sxs-lookup"><span data-stu-id="639d8-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="639d8-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="639d8-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="639d8-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="639d8-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (12)</span><span class="sxs-lookup"><span data-stu-id="639d8-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="639d8-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="639d8-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="639d8-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="639d8-258">Commenti</span><span class="sxs-lookup"><span data-stu-id="639d8-258">Remarks</span></span>

<span data-ttu-id="639d8-259">L'accesso alla **classe \_ AllocationCapabilities di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="639d8-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="639d8-260">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="639d8-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="639d8-261">Requisiti</span><span class="sxs-lookup"><span data-stu-id="639d8-261">Requirements</span></span>



| <span data-ttu-id="639d8-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="639d8-262">Requirement</span></span> | <span data-ttu-id="639d8-263">Valore</span><span class="sxs-lookup"><span data-stu-id="639d8-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639d8-264">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639d8-264">Minimum supported client</span></span><br/> | <span data-ttu-id="639d8-265">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="639d8-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="639d8-266">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639d8-266">Minimum supported server</span></span><br/> | <span data-ttu-id="639d8-267">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="639d8-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="639d8-268">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="639d8-268">Namespace</span></span><br/>                | <span data-ttu-id="639d8-269">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="639d8-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="639d8-270">MOF</span><span class="sxs-lookup"><span data-stu-id="639d8-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="639d8-271"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="639d8-272">DLL</span><span class="sxs-lookup"><span data-stu-id="639d8-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639d8-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="639d8-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="639d8-274">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="639d8-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639d8-275">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="639d8-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="639d8-276">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="639d8-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="639d8-277">**MSVM \_ AllocationCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="639d8-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="639d8-278">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="639d8-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

