---
description: Rappresenta lo stato configurato del componente Desktop remoto Virtualization (RDV). Lo stato predefinito è abilitato.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Classe Msvm_RdvComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882170"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="b2b47-104">\_Classe MSVM RdvComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="b2b47-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="b2b47-105">Rappresenta lo stato configurato del componente Desktop remoto Virtualization (RDV).</span><span class="sxs-lookup"><span data-stu-id="b2b47-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="b2b47-106">Lo stato predefinito è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b2b47-106">The default state is Enabled.</span></span>

<span data-ttu-id="b2b47-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2b47-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b47-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2b47-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
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

## <a name="members"></a><span data-ttu-id="b2b47-109">Members</span><span class="sxs-lookup"><span data-stu-id="b2b47-109">Members</span></span>

<span data-ttu-id="b2b47-110">La **classe \_ RdvComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2b47-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2b47-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2b47-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2b47-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2b47-112">Properties</span></span>

<span data-ttu-id="b2b47-113">La **classe \_ RdvComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2b47-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2b47-114">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="b2b47-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-117">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-117">The address of the resource.</span></span> <span data-ttu-id="b2b47-118">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="b2b47-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-122">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="b2b47-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b2b47-123">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="b2b47-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b2b47-124">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="b2b47-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-128">Unità di allocazione utilizzata dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="b2b47-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b2b47-129">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="b2b47-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2b47-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-133">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b2b47-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="b2b47-134">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="b2b47-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2b47-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-138">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b2b47-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="b2b47-139">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-140">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b2b47-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-143">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="b2b47-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-144">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2b47-144">A short description of the object.</span></span> <span data-ttu-id="b2b47-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Settings".</span><span class="sxs-lookup"><span data-stu-id="b2b47-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b2b47-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-147">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b2b47-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-149">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-149">The device to which this resource is connected.</span></span> <span data-ttu-id="b2b47-150">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-151">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="b2b47-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b47-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-154">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="b2b47-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="b2b47-155">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 3 (virtualizzata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-156">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b2b47-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-159">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b2b47-159">A description of the object.</span></span> <span data-ttu-id="b2b47-160">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Settings".</span><span class="sxs-lookup"><span data-stu-id="b2b47-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b2b47-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-164">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b2b47-164">A display name for the object.</span></span> <span data-ttu-id="b2b47-165">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2b47-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="b2b47-166">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="b2b47-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b2b47-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b47-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-170">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b2b47-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b2b47-171">I valori validi sono 2 (abilitato) e 3 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="b2b47-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="b2b47-172">Il valore predefinito è 2 (abilitato).</span><span class="sxs-lookup"><span data-stu-id="b2b47-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="b2b47-173">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b47-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="b2b47-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-175">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b2b47-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-177">È possibile assegnare una sola risorsa host a ogni dispositivo nel Commuter virtuale, pertanto è possibile impostare solo il primo elemento di questa matrice.</span><span class="sxs-lookup"><span data-stu-id="b2b47-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="b2b47-178">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="b2b47-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="b2b47-179">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2b47-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-183">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b2b47-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-184">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b2b47-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b2b47-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b2b47-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-186">**Limite**</span><span class="sxs-lookup"><span data-stu-id="b2b47-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-187">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b47-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-189">Quantità massima di risorse host corrispondenti che possono essere utilizzate dal Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2b47-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="b2b47-190">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-191">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="b2b47-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b47-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-194">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="b2b47-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="b2b47-195">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-196">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="b2b47-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-199">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b2b47-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="b2b47-200">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b2b47-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-201">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b2b47-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-204">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-204">The parent of the resource.</span></span> <span data-ttu-id="b2b47-205">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-206">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="b2b47-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-209">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="b2b47-210">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-211">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="b2b47-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-212">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b47-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-214">Quantità di risorse riservate per l'utilizzo da parte del Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2b47-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="b2b47-215">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b2b47-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-219">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="b2b47-220">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2b47-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="b2b47-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b2b47-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2b47-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-225">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="b2b47-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="b2b47-226">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 33 (Ethernet Connection).</span><span class="sxs-lookup"><span data-stu-id="b2b47-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b2b47-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2b47-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-230">Numero totale di porte nel Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2b47-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="b2b47-231">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-232">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="b2b47-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2b47-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-235">Specifica l'unità di misura per la proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="b2b47-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="b2b47-236">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b2b47-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="b2b47-237">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b2b47-238">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b2b47-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2b47-239">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2b47-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2b47-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2b47-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2b47-241">Intero che definisce il peso per ogni Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2b47-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="b2b47-242">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b2b47-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="b2b47-243">Intervallo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="b2b47-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b47-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2b47-244">Requirements</span></span>



| <span data-ttu-id="b2b47-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b47-245">Requirement</span></span> | <span data-ttu-id="b2b47-246">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b47-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b47-247">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b47-247">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b47-248">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b2b47-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2b47-249">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b47-249">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b47-250">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b2b47-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2b47-251">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2b47-251">Namespace</span></span><br/>                | <span data-ttu-id="b2b47-252">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2b47-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2b47-253">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b47-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b47-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b47-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b47-255">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b47-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b47-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2b47-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

