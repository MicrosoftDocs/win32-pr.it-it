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
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="549e8-103">CIM \_ ResourceAllocationSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="549e8-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="549e8-104">Rappresenta le impostazioni per una risorsa allocata che non rientrano nell'ambito della classe CIM utilizzata in genere per rappresentare la risorsa stessa.</span><span class="sxs-lookup"><span data-stu-id="549e8-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="549e8-105">Queste impostazioni includono informazioni specifiche dell'allocazione che potrebbero non essere visibili al consumer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="549e8-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="549e8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="549e8-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="549e8-107">Members</span><span class="sxs-lookup"><span data-stu-id="549e8-107">Members</span></span>

<span data-ttu-id="549e8-108">La classe **CIM \_ ResourceAllocationSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="549e8-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="549e8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="549e8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="549e8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="549e8-110">Properties</span></span>

<span data-ttu-id="549e8-111">La classe **CIM \_ ResourceAllocationSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="549e8-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="549e8-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="549e8-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-115">Indirizzo della risorsa, ad esempio l'indirizzo MAC di una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="549e8-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-116">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="549e8-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-119">Indirizzo della risorsa dal contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="549e8-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="549e8-120">Questa proprietà viene utilizzata per descrivere una relazione del controller e l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="549e8-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="549e8-121">Se, ad esempio, l'elemento padre è un controller PCI, questa proprietà specifica lo slot PCI del dispositivo figlio.</span><span class="sxs-lookup"><span data-stu-id="549e8-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-122">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="549e8-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-125">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Reservation**","**CIM \_ ResourceAllocationSettingData**.**Limite**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="549e8-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="549e8-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="549e8-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-127">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="549e8-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="549e8-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-130">**true** per allocare automaticamente la risorsa; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="549e8-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-131">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="549e8-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="549e8-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-134">**true** per deallocare automaticamente la risorsa; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="549e8-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-135">**Connection**</span><span class="sxs-lookup"><span data-stu-id="549e8-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-136">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="549e8-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="549e8-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-138">Matrice che indica gli oggetti connessi alla risorsa, ad esempio una rete denominata o una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="549e8-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-139">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="549e8-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="549e8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-142">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="549e8-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="549e8-143">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="549e8-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="549e8-144">**Passato** (2)</span><span class="sxs-lookup"><span data-stu-id="549e8-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="549e8-145">**Virtualizzato** (3)</span><span class="sxs-lookup"><span data-stu-id="549e8-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="549e8-146">**Non rappresentata** (4)</span><span class="sxs-lookup"><span data-stu-id="549e8-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="549e8-147">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="549e8-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="549e8-148">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="549e8-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="549e8-149">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="549e8-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-150">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="549e8-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="549e8-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-152">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**","**CIM \_ ResourceAllocationSettingData**.**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="549e8-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-153">Matrice che contiene l'assegnazione delle risorse allocate.</span><span class="sxs-lookup"><span data-stu-id="549e8-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="549e8-154">Ogni valore non null di questa proprietà deve essere formattato come URI basato su RFC3986.</span><span class="sxs-lookup"><span data-stu-id="549e8-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="549e8-155">Se la risorsa è modellata, il valore deve essere un URI WBEM.</span><span class="sxs-lookup"><span data-stu-id="549e8-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-156">**Limite**</span><span class="sxs-lookup"><span data-stu-id="549e8-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-157">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="549e8-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-159">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="549e8-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-160">Quantità massima di risorse da concedere all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="549e8-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="549e8-161">Il tipo di unità di questa proprietà è specificato dalla proprietà **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="549e8-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-162">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="549e8-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="549e8-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-165">Indica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="549e8-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="549e8-166">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="549e8-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="549e8-167">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="549e8-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="549e8-168">**Dedicato** (3)</span><span class="sxs-lookup"><span data-stu-id="549e8-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="549e8-169">**Affinità Soft** (4)</span><span class="sxs-lookup"><span data-stu-id="549e8-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="549e8-170">**Affinità hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="549e8-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="549e8-171">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="549e8-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="549e8-172">**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="549e8-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="549e8-173">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="549e8-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-176">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="549e8-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-177">Descrizione del tipo di risorsa quando la proprietà **ResourceType** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="549e8-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="549e8-178">**Parent**</span><span class="sxs-lookup"><span data-stu-id="549e8-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-181">Elemento padre della risorsa, ad esempio un controller per l'allocazione corrente.</span><span class="sxs-lookup"><span data-stu-id="549e8-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-182">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="549e8-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-185">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="549e8-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-186">ID del pool di risorse che ha generato la risorsa.</span><span class="sxs-lookup"><span data-stu-id="549e8-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-187">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="549e8-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-188">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="549e8-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-190">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="549e8-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-191">Il numero di risorse di cui è garantita la disponibilità per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="549e8-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="549e8-192">Nei sistemi che supportano l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione.</span><span class="sxs-lookup"><span data-stu-id="549e8-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="549e8-193">Il tipo di unità di questa proprietà è specificato dalla proprietà **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="549e8-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="549e8-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-197">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="549e8-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-198">Sottotipo specifico di implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="549e8-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="549e8-199">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="549e8-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="549e8-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-201">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="549e8-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-203">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**","**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="549e8-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-204">Tipo di risorsa rappresentata dalle impostazioni di allocazione.</span><span class="sxs-lookup"><span data-stu-id="549e8-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="549e8-205">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="549e8-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="549e8-206">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="549e8-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="549e8-207">**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="549e8-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="549e8-208">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="549e8-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="549e8-209">**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="549e8-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="549e8-210">**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="549e8-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="549e8-211">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="549e8-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="549e8-212">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="549e8-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="549e8-213">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="549e8-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="549e8-214">**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="549e8-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="549e8-215">**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="549e8-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="549e8-216">**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="549e8-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="549e8-217">**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="549e8-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="549e8-218">**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="549e8-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="549e8-219">**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="549e8-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="549e8-220">**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="549e8-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="549e8-221">**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="549e8-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="549e8-222">**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="549e8-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="549e8-223">**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="549e8-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="549e8-224">**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="549e8-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="549e8-225">**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="549e8-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="549e8-226">**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="549e8-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="549e8-227">**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="549e8-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="549e8-228">**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="549e8-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="549e8-229">**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="549e8-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="549e8-230">**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="549e8-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="549e8-231">**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="549e8-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="549e8-232">**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="549e8-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="549e8-233">**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="549e8-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="549e8-234">**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="549e8-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="549e8-235">**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="549e8-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="549e8-236">**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="549e8-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="549e8-237">**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="549e8-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="549e8-238">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="549e8-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="549e8-239">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="549e8-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="549e8-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="549e8-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-241">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="549e8-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-243">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="549e8-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="549e8-244">Il numero di risorse presentate al consumer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="549e8-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-245">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="549e8-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="549e8-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="549e8-248">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="549e8-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="549e8-249">Unità utilizzate dalla proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="549e8-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="549e8-250">**Weight**</span><span class="sxs-lookup"><span data-stu-id="549e8-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="549e8-251">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="549e8-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="549e8-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="549e8-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="549e8-253">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="549e8-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="549e8-254">Requisiti</span><span class="sxs-lookup"><span data-stu-id="549e8-254">Requirements</span></span>



| <span data-ttu-id="549e8-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="549e8-255">Requirement</span></span> | <span data-ttu-id="549e8-256">Valore</span><span class="sxs-lookup"><span data-stu-id="549e8-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549e8-257">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="549e8-257">Minimum supported client</span></span><br/> | <span data-ttu-id="549e8-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="549e8-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="549e8-259">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="549e8-259">Minimum supported server</span></span><br/> | <span data-ttu-id="549e8-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="549e8-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="549e8-261">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="549e8-261">Namespace</span></span><br/>                | <span data-ttu-id="549e8-262">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="549e8-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="549e8-263">MOF</span><span class="sxs-lookup"><span data-stu-id="549e8-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="549e8-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="549e8-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="549e8-265">DLL</span><span class="sxs-lookup"><span data-stu-id="549e8-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="549e8-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="549e8-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="549e8-267">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="549e8-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549e8-268">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="549e8-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

