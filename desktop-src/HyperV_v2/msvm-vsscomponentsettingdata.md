---
description: Rappresenta lo stato configurato del servizio Servizio Copia Shadow del volume (VSS).
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Classe Msvm_VssComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305971"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="fc13a-103">\_Classe MSVM VssComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="fc13a-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="fc13a-104">Rappresenta lo stato configurato del servizio Servizio Copia Shadow del volume (VSS).</span><span class="sxs-lookup"><span data-stu-id="fc13a-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="fc13a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fc13a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc13a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc13a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
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

## <a name="members"></a><span data-ttu-id="fc13a-107">Members</span><span class="sxs-lookup"><span data-stu-id="fc13a-107">Members</span></span>

<span data-ttu-id="fc13a-108">La **classe \_ VssComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fc13a-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fc13a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc13a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc13a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc13a-110">Properties</span></span>

<span data-ttu-id="fc13a-111">La **classe \_ VssComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc13a-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc13a-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="fc13a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc13a-115">The address of the resource.</span></span> <span data-ttu-id="fc13a-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="fc13a-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="fc13a-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fc13a-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="fc13a-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fc13a-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="fc13a-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="fc13a-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fc13a-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="fc13a-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc13a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc13a-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fc13a-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="fc13a-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc13a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc13a-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="fc13a-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fc13a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc13a-141">A short description of the object.</span></span> <span data-ttu-id="fc13a-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc13a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="fc13a-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-144">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fc13a-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-146">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc13a-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="fc13a-147">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="fc13a-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc13a-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-151">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="fc13a-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="fc13a-152">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="fc13a-153">Valore</span><span class="sxs-lookup"><span data-stu-id="fc13a-153">Value</span></span>                                                                        | <span data-ttu-id="fc13a-154">Significato</span><span class="sxs-lookup"><span data-stu-id="fc13a-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="fc13a-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fc13a-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="fc13a-156">Virtualizzato</span><span class="sxs-lookup"><span data-stu-id="fc13a-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fc13a-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fc13a-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="fc13a-160">A description of the object.</span></span> <span data-ttu-id="fc13a-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc13a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fc13a-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-165">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc13a-165">A display name for the object.</span></span> <span data-ttu-id="fc13a-166">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc13a-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fc13a-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc13a-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-170">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="fc13a-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fc13a-171">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e il valore predefinito è 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="fc13a-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="fc13a-172">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fc13a-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="fc13a-173">(2)</span><span class="sxs-lookup"><span data-stu-id="fc13a-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="fc13a-174">Abilitato</span><span class="sxs-lookup"><span data-stu-id="fc13a-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-175">3</span><span class="sxs-lookup"><span data-stu-id="fc13a-175">3</span></span>
</dt> <dd>

<span data-ttu-id="fc13a-176">Disabled</span><span class="sxs-lookup"><span data-stu-id="fc13a-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc13a-177">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="fc13a-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-180">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="fc13a-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="fc13a-181">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fc13a-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc13a-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-185">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="fc13a-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-186">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="fc13a-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fc13a-187">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc13a-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-188">**Limite**</span><span class="sxs-lookup"><span data-stu-id="fc13a-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-189">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc13a-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-191">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="fc13a-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="fc13a-192">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-193">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="fc13a-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-194">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc13a-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-196">Indica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="fc13a-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="fc13a-197">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-198">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fc13a-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-201">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="fc13a-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="fc13a-202">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-203">**Parent**</span><span class="sxs-lookup"><span data-stu-id="fc13a-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-206">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc13a-206">The parent of the resource.</span></span> <span data-ttu-id="fc13a-207">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-208">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="fc13a-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-211">ID del pool di risorse da cui viene allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc13a-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="fc13a-212">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-213">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="fc13a-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-214">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc13a-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-216">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="fc13a-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="fc13a-217">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fc13a-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-221">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc13a-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="fc13a-222">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="fc13a-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fc13a-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-224">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc13a-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-226">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="fc13a-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fc13a-227">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="fc13a-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="fc13a-228">Valore</span><span class="sxs-lookup"><span data-stu-id="fc13a-228">Value</span></span>                                                                        | <span data-ttu-id="fc13a-229">Significato</span><span class="sxs-lookup"><span data-stu-id="fc13a-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="fc13a-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc13a-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fc13a-231">Altro</span><span class="sxs-lookup"><span data-stu-id="fc13a-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fc13a-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fc13a-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-233">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc13a-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-235">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="fc13a-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="fc13a-236">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-237">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="fc13a-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fc13a-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-240">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fc13a-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="fc13a-241">Il valore di questa proprietà è un valore valido del qualificatore unità programmatiche come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="fc13a-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fc13a-242">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc13a-243">**Weight**</span><span class="sxs-lookup"><span data-stu-id="fc13a-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc13a-244">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc13a-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc13a-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc13a-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc13a-246">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc13a-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="fc13a-247">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc13a-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc13a-248">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc13a-248">Remarks</span></span>

<span data-ttu-id="fc13a-249">L'accesso alla **classe \_ VssComponentSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="fc13a-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fc13a-250">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fc13a-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc13a-251">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc13a-251">Requirements</span></span>



| <span data-ttu-id="fc13a-252">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc13a-252">Requirement</span></span> | <span data-ttu-id="fc13a-253">Valore</span><span class="sxs-lookup"><span data-stu-id="fc13a-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc13a-254">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc13a-254">Minimum supported client</span></span><br/> | <span data-ttu-id="fc13a-255">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fc13a-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc13a-256">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc13a-256">Minimum supported server</span></span><br/> | <span data-ttu-id="fc13a-257">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fc13a-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc13a-258">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc13a-258">Namespace</span></span><br/>                | <span data-ttu-id="fc13a-259">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc13a-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc13a-260">MOF</span><span class="sxs-lookup"><span data-stu-id="fc13a-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc13a-261"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc13a-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc13a-262">DLL</span><span class="sxs-lookup"><span data-stu-id="fc13a-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc13a-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc13a-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc13a-264">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc13a-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc13a-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fc13a-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fc13a-266">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fc13a-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

