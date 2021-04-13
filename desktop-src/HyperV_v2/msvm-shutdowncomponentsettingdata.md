---
description: Rappresenta lo stato configurato del servizio di arresto.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Classe Msvm_ShutdownComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226624"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="c005e-103">\_Classe MSVM ShutdownComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="c005e-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="c005e-104">Rappresenta lo stato configurato del servizio di arresto.</span><span class="sxs-lookup"><span data-stu-id="c005e-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="c005e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c005e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c005e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c005e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="c005e-107">Members</span><span class="sxs-lookup"><span data-stu-id="c005e-107">Members</span></span>

<span data-ttu-id="c005e-108">La **classe \_ ShutdownComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c005e-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c005e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c005e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c005e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c005e-110">Properties</span></span>

<span data-ttu-id="c005e-111">La **classe \_ ShutdownComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c005e-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c005e-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="c005e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c005e-115">The address of the resource.</span></span> <span data-ttu-id="c005e-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="c005e-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="c005e-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c005e-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="c005e-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c005e-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="c005e-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="c005e-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c005e-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="c005e-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c005e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c005e-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c005e-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="c005e-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c005e-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c005e-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="c005e-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c005e-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c005e-141">A short description of the object.</span></span> <span data-ttu-id="c005e-142">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Shutdown".</span><span class="sxs-lookup"><span data-stu-id="c005e-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="c005e-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c005e-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-144">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c005e-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c005e-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-146">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c005e-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="c005e-147">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="c005e-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c005e-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-151">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="c005e-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="c005e-152">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c005e-153">Valore</span><span class="sxs-lookup"><span data-stu-id="c005e-153">Value</span></span>                                                                        | <span data-ttu-id="c005e-154">Significato</span><span class="sxs-lookup"><span data-stu-id="c005e-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="c005e-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c005e-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c005e-156">Virtualizzato</span><span class="sxs-lookup"><span data-stu-id="c005e-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c005e-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c005e-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="c005e-160">A description of the object.</span></span> <span data-ttu-id="c005e-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c005e-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c005e-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-165">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c005e-165">A display name for the object.</span></span> <span data-ttu-id="c005e-166">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c005e-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c005e-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c005e-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-170">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="c005e-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c005e-171">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c005e-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c005e-172">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="c005e-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c005e-173">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="c005e-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c005e-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="c005e-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-175">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c005e-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c005e-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-177">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c005e-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="c005e-178">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c005e-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c005e-182">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="c005e-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c005e-183">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c005e-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c005e-184">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c005e-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-185">**Limite**</span><span class="sxs-lookup"><span data-stu-id="c005e-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-186">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c005e-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-188">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c005e-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="c005e-189">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-190">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="c005e-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c005e-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-193">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c005e-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c005e-194">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-195">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="c005e-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-198">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c005e-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="c005e-199">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-200">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c005e-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-203">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c005e-203">The parent of the resource.</span></span> <span data-ttu-id="c005e-204">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-205">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="c005e-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-208">ID del pool di risorse da cui viene allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c005e-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="c005e-209">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-210">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="c005e-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-211">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c005e-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-213">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c005e-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="c005e-214">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="c005e-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-218">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c005e-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="c005e-219">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c005e-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c005e-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-223">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="c005e-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="c005e-224">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c005e-225">Valore</span><span class="sxs-lookup"><span data-stu-id="c005e-225">Value</span></span>                                                                        | <span data-ttu-id="c005e-226">Significato</span><span class="sxs-lookup"><span data-stu-id="c005e-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="c005e-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c005e-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c005e-228">Altro</span><span class="sxs-lookup"><span data-stu-id="c005e-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c005e-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c005e-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-230">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c005e-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-232">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="c005e-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="c005e-233">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-234">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="c005e-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c005e-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-237">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c005e-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="c005e-238">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c005e-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="c005e-239">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c005e-240">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c005e-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c005e-241">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c005e-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c005e-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c005e-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c005e-243">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="c005e-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="c005e-244">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c005e-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c005e-245">Commenti</span><span class="sxs-lookup"><span data-stu-id="c005e-245">Remarks</span></span>

<span data-ttu-id="c005e-246">L'accesso alla **classe \_ ShutdownComponentSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c005e-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c005e-247">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c005e-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c005e-248">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c005e-248">Requirements</span></span>



| <span data-ttu-id="c005e-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="c005e-249">Requirement</span></span> | <span data-ttu-id="c005e-250">Valore</span><span class="sxs-lookup"><span data-stu-id="c005e-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c005e-251">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c005e-251">Minimum supported client</span></span><br/> | <span data-ttu-id="c005e-252">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c005e-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c005e-253">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c005e-253">Minimum supported server</span></span><br/> | <span data-ttu-id="c005e-254">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c005e-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c005e-255">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c005e-255">Namespace</span></span><br/>                | <span data-ttu-id="c005e-256">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c005e-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c005e-257">MOF</span><span class="sxs-lookup"><span data-stu-id="c005e-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c005e-258"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c005e-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c005e-259">DLL</span><span class="sxs-lookup"><span data-stu-id="c005e-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c005e-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c005e-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c005e-261">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c005e-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c005e-262">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c005e-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="c005e-263">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c005e-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

