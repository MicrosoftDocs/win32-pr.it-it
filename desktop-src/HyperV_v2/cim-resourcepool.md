---
description: Rappresenta un pool di risorse, ovvero un'entità logica fornita dal sistema host per allocare e assegnare le risorse.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: Classe CIM_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129694"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="34a79-103">CIM \_ ResourcePool (classe)</span><span class="sxs-lookup"><span data-stu-id="34a79-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="34a79-104">Rappresenta un pool di risorse, ovvero un'entità logica fornita dal sistema host per allocare e assegnare le risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34a79-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="34a79-106">Members</span><span class="sxs-lookup"><span data-stu-id="34a79-106">Members</span></span>

<span data-ttu-id="34a79-107">La classe **CIM \_ ResourcePool** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="34a79-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="34a79-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34a79-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34a79-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34a79-109">Properties</span></span>

<span data-ttu-id="34a79-110">La classe **CIM \_ ResourcePool** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="34a79-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34a79-111">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="34a79-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-114">Qualificatori: **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="34a79-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="34a79-115">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="34a79-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="34a79-116">Ad esempio, quando **ResourceType** è impostato su "Processor", **AllocationUnits** può essere impostato su "Hertz \* 10 ^ 6" o "percent".</span><span class="sxs-lookup"><span data-stu-id="34a79-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="34a79-117">Il valore di questa proprietà deve essere un valore valido del qualificatore unità programmatiche dall'Appendice C. 1 di *DSP0004 v 2.4* o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="34a79-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-118">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="34a79-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-119">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34a79-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34a79-121">Quantità massima di prenotazioni che il pool di risorse può supportare.</span><span class="sxs-lookup"><span data-stu-id="34a79-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="34a79-122">La proprietà **AllocationUnits** specifica il tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="34a79-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-123">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="34a79-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-126">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**MaxConsumableResource**","**CIM \_ ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="34a79-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="34a79-127">Unità per **MaxConsumable** e proprietà **utilizzate** .</span><span class="sxs-lookup"><span data-stu-id="34a79-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-128">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="34a79-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34a79-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="34a79-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-132">Quantità di risorse attualmente presenti nel pool di risorse per i consumer di risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="34a79-133">Questa proprietà è diversa dalla proprietà **riservata** perché descrive la visualizzazione dei consumer della risorsa mentre la proprietà **riservata** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34a79-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="34a79-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-137">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="34a79-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-138">Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="34a79-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="34a79-139">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="34a79-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="34a79-140">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce la proprietà **InstanceID** , oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="34a79-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="34a79-141">*OrgID* non deve contenere i due punti.</span><span class="sxs-lookup"><span data-stu-id="34a79-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="34a79-142">I primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="34a79-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="34a79-143">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="34a79-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="34a79-144">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="34a79-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="34a79-145">Per le istanze definite da DMTF, il modello deve essere usato con *OrgID* impostato su "CIM".</span><span class="sxs-lookup"><span data-stu-id="34a79-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="34a79-146">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="34a79-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-147">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34a79-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-149">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="34a79-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-150">Il numero massimo di risorse utilizzabili che il pool di risorse può presentare ai consumer di risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="34a79-151">Questa proprietà è diversa dalla proprietà **Capacity** perché descrive la visualizzazione dei consumer della risorsa mentre la proprietà **Capacity** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34a79-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-152">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="34a79-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-155">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="34a79-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-156">Il tipo di risorsa quando la proprietà **ResourceType** è impostata su "0" (other).</span><span class="sxs-lookup"><span data-stu-id="34a79-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="34a79-157">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="34a79-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-160">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="34a79-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-161">Identificatore opaco per il pool.</span><span class="sxs-lookup"><span data-stu-id="34a79-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="34a79-162">Questa proprietà viene utilizzata per fornire la correlazione durante il salvataggio e il ripristino dei dati di configurazione nell'archivio permanente sottostante.</span><span class="sxs-lookup"><span data-stu-id="34a79-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-163">**Originale**</span><span class="sxs-lookup"><span data-stu-id="34a79-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-164">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="34a79-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34a79-166">**true** se il pool di risorse è primordiale.</span><span class="sxs-lookup"><span data-stu-id="34a79-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="34a79-167">**false** se il pool di risorse è un pool di risorse concrete.</span><span class="sxs-lookup"><span data-stu-id="34a79-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="34a79-168">Un pool di risorse primordiale è un pool di risorse che non viene creato o eliminato dai consumer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34a79-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="34a79-169">Un pool di risorse concrete può essere aggiornato dai servizi di allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="34a79-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-171">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34a79-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34a79-173">Numero corrente di prenotazioni distribuite in tutte le allocazioni attive da questo pool.</span><span class="sxs-lookup"><span data-stu-id="34a79-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="34a79-174">In una configurazione gerarchica rappresenta la somma di tutte le prenotazioni discendenti correnti.</span><span class="sxs-lookup"><span data-stu-id="34a79-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="34a79-175">La proprietà **AllocationUnits** specifica il tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="34a79-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="34a79-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="34a79-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-179">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="34a79-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-180">Sottotipo specifico dell'implementazione per il pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="34a79-181">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="34a79-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="34a79-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="34a79-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34a79-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34a79-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34a79-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34a79-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34a79-185">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**OtherResourceType**","**CIM \_ ResourcePool**.**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="34a79-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="34a79-186">Tipo di risorsa allocata dal pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="34a79-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34a79-187">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="34a79-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="34a79-188">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="34a79-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="34a79-189">**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="34a79-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="34a79-190">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="34a79-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="34a79-191">**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="34a79-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="34a79-192">**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="34a79-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="34a79-193">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="34a79-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="34a79-194">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="34a79-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="34a79-195">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="34a79-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="34a79-196">**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="34a79-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="34a79-197">**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="34a79-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="34a79-198">**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="34a79-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="34a79-199">**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="34a79-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="34a79-200">**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="34a79-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="34a79-201">**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="34a79-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="34a79-202">**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="34a79-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="34a79-203">**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="34a79-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="34a79-204">**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="34a79-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="34a79-205">**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="34a79-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="34a79-206">**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="34a79-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="34a79-207">**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="34a79-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="34a79-208">**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="34a79-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="34a79-209">**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="34a79-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="34a79-210">**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="34a79-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="34a79-211">**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="34a79-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="34a79-212">**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="34a79-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="34a79-213">**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="34a79-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="34a79-214">**Potenza** (28)</span><span class="sxs-lookup"><span data-stu-id="34a79-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="34a79-215">**Capacità di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="34a79-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="34a79-216">**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="34a79-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="34a79-217">**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="34a79-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="34a79-218">**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="34a79-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="34a79-219">**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="34a79-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="34a79-220">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="34a79-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="34a79-221">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="34a79-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="34a79-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="34a79-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="34a79-223">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34a79-223">Requirements</span></span>



| <span data-ttu-id="34a79-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a79-224">Requirement</span></span> | <span data-ttu-id="34a79-225">Valore</span><span class="sxs-lookup"><span data-stu-id="34a79-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a79-226">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34a79-226">Minimum supported client</span></span><br/> | <span data-ttu-id="34a79-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="34a79-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="34a79-228">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34a79-228">Minimum supported server</span></span><br/> | <span data-ttu-id="34a79-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34a79-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="34a79-230">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34a79-230">Namespace</span></span><br/>                | <span data-ttu-id="34a79-231">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="34a79-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="34a79-232">MOF</span><span class="sxs-lookup"><span data-stu-id="34a79-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34a79-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34a79-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34a79-234">DLL</span><span class="sxs-lookup"><span data-stu-id="34a79-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a79-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34a79-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34a79-236">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34a79-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a79-237">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="34a79-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

