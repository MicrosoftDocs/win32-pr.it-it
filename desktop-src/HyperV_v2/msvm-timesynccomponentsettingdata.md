---
description: Rappresenta lo stato configurato del servizio di sincronizzazione dell'ora.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Classe Msvm_TimeSyncComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966941"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="d897a-103">\_Classe MSVM TimeSyncComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="d897a-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="d897a-104">Rappresenta lo stato configurato del servizio di sincronizzazione dell'ora.</span><span class="sxs-lookup"><span data-stu-id="d897a-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="d897a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d897a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d897a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d897a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="d897a-107">Members</span><span class="sxs-lookup"><span data-stu-id="d897a-107">Members</span></span>

<span data-ttu-id="d897a-108">La **classe \_ TimeSyncComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d897a-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d897a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d897a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d897a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d897a-110">Properties</span></span>

<span data-ttu-id="d897a-111">La **classe \_ TimeSyncComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d897a-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d897a-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="d897a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d897a-115">The address of the resource.</span></span> <span data-ttu-id="d897a-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d897a-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d897a-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d897a-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="d897a-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d897a-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d897a-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="d897a-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d897a-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d897a-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d897a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d897a-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="d897a-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d897a-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d897a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d897a-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="d897a-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d897a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d897a-141">A short description of the object.</span></span> <span data-ttu-id="d897a-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d897a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="d897a-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-144">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d897a-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d897a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-146">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="d897a-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="d897a-147">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d897a-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d897a-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-151">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="d897a-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="d897a-152">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="d897a-153">Valore</span><span class="sxs-lookup"><span data-stu-id="d897a-153">Value</span></span>                                                                        | <span data-ttu-id="d897a-154">Significato</span><span class="sxs-lookup"><span data-stu-id="d897a-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="d897a-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d897a-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d897a-156">Virtualizzato</span><span class="sxs-lookup"><span data-stu-id="d897a-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d897a-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d897a-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d897a-160">A description of the object.</span></span> <span data-ttu-id="d897a-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d897a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d897a-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-165">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d897a-165">A display name for the object.</span></span> <span data-ttu-id="d897a-166">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d897a-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d897a-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d897a-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-170">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d897a-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d897a-171">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d897a-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="d897a-172">(2)</span><span class="sxs-lookup"><span data-stu-id="d897a-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="d897a-173">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d897a-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="d897a-174">3</span><span class="sxs-lookup"><span data-stu-id="d897a-174">3</span></span>
</dt> <dd>

<span data-ttu-id="d897a-175">Disabled</span><span class="sxs-lookup"><span data-stu-id="d897a-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d897a-176">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d897a-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-177">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d897a-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d897a-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-179">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="d897a-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="d897a-180">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d897a-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d897a-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d897a-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d897a-184">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d897a-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d897a-185">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d897a-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d897a-186">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d897a-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="d897a-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-188">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d897a-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-190">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="d897a-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="d897a-191">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-192">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d897a-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d897a-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-195">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="d897a-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d897a-196">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-197">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d897a-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-200">Il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore "other".</span><span class="sxs-lookup"><span data-stu-id="d897a-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="d897a-201">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-202">**Parent**</span><span class="sxs-lookup"><span data-stu-id="d897a-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-205">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d897a-205">The parent of the resource.</span></span> <span data-ttu-id="d897a-206">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-207">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="d897a-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-210">ID del pool di risorse da cui viene allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d897a-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="d897a-211">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-212">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="d897a-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-213">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d897a-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-215">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="d897a-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="d897a-216">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d897a-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-220">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="d897a-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="d897a-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d897a-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d897a-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d897a-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d897a-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-225">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="d897a-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="d897a-226">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="d897a-227">Valore</span><span class="sxs-lookup"><span data-stu-id="d897a-227">Value</span></span>                                                                        | <span data-ttu-id="d897a-228">Significato</span><span class="sxs-lookup"><span data-stu-id="d897a-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="d897a-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d897a-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d897a-230">Altro</span><span class="sxs-lookup"><span data-stu-id="d897a-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d897a-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d897a-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-232">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d897a-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-234">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="d897a-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="d897a-235">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-236">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d897a-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d897a-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-239">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d897a-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="d897a-240">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d897a-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="d897a-241">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d897a-242">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d897a-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d897a-243">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d897a-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d897a-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d897a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d897a-245">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="d897a-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="d897a-246">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="d897a-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d897a-247">Commenti</span><span class="sxs-lookup"><span data-stu-id="d897a-247">Remarks</span></span>

<span data-ttu-id="d897a-248">L'accesso alla **classe \_ TimeSyncComponentSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d897a-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d897a-249">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d897a-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d897a-250">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d897a-250">Requirements</span></span>



| <span data-ttu-id="d897a-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="d897a-251">Requirement</span></span> | <span data-ttu-id="d897a-252">Valore</span><span class="sxs-lookup"><span data-stu-id="d897a-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d897a-253">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d897a-253">Minimum supported client</span></span><br/> | <span data-ttu-id="d897a-254">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d897a-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d897a-255">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d897a-255">Minimum supported server</span></span><br/> | <span data-ttu-id="d897a-256">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d897a-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d897a-257">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d897a-257">Namespace</span></span><br/>                | <span data-ttu-id="d897a-258">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d897a-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d897a-259">MOF</span><span class="sxs-lookup"><span data-stu-id="d897a-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d897a-260"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d897a-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d897a-261">DLL</span><span class="sxs-lookup"><span data-stu-id="d897a-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d897a-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d897a-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d897a-263">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d897a-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d897a-264">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d897a-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="d897a-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d897a-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

