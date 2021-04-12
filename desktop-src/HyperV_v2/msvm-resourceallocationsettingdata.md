---
description: Rappresenta gli Stati di allocazione corrente e registrata di una risorsa virtuale.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Classe Msvm_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346051"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="6aa9b-103">\_Classe MSVM ResourceAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="6aa9b-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="6aa9b-104">Rappresenta gli Stati di allocazione corrente e registrata di una risorsa virtuale.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="6aa9b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa9b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aa9b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
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
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="6aa9b-107">Members</span><span class="sxs-lookup"><span data-stu-id="6aa9b-107">Members</span></span>

<span data-ttu-id="6aa9b-108">La **classe \_ ResourceAllocationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6aa9b-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6aa9b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6aa9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6aa9b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6aa9b-110">Properties</span></span>

<span data-ttu-id="6aa9b-111">La **classe \_ ResourceAllocationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6aa9b-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-115">The address of the resource.</span></span> <span data-ttu-id="6aa9b-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="6aa9b-117">Si tratta di una proprietà di sola lettura, ma se la proprietà **ResourceType** è 20 (controller grafico), è possibile modificarla utilizzando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-121">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="6aa9b-122">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="6aa9b-123">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-127">Unità di allocazione utilizzata dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="6aa9b-128">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-132">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="6aa9b-133">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-137">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="6aa9b-138">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-142">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-143">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-143">A short description of the object.</span></span> <span data-ttu-id="6aa9b-144">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-145">**Connection**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-146">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-148">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-148">The device to which this resource is connected.</span></span> <span data-ttu-id="6aa9b-149">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="6aa9b-150">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-150">This is a read-only property.</span></span> <span data-ttu-id="6aa9b-151">Tuttavia, se la proprietà **ResourceType** è 21 (porta seriale) e la proprietà **ResourceSubType** è "Microsoft: Hyper-V: Serial Port", la proprietà di **connessione** può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-155">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="6aa9b-156">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-160">A description of the object.</span></span> <span data-ttu-id="6aa9b-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-165">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-165">A display name for the object.</span></span> <span data-ttu-id="6aa9b-166">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="6aa9b-167">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="6aa9b-168">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-169">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-170">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-172">È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="6aa9b-173">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="6aa9b-174">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="6aa9b-175">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-175">This is a read-only property.</span></span> <span data-ttu-id="6aa9b-176">Tuttavia, se la proprietà **ResourceType** è 17 (disco) e la proprietà **ResourceSubType** è "Microsoft: Hyper-V: unità disco fisica", è possibile modificare la proprietà **HostResource** usando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-180">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-181">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6aa9b-182">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="6aa9b-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-183">**Limite**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-184">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-186">Quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="6aa9b-187">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="6aa9b-188">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-189">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-192">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="6aa9b-193">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-194">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-197">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="6aa9b-198">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-199">**Parent**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-202">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-202">The parent of the resource.</span></span> <span data-ttu-id="6aa9b-203">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-204">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-207">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="6aa9b-208">Per le istanze associate a una macchina virtuale, si tratta di "Microsoft:*GUID* \\ *dati specifici del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="6aa9b-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="6aa9b-209">Per le istanze che definiscono le potenziali impostazioni per una macchina virtuale, questo sarà "Microsoft: Definition \\ *GUID* \\ *Type*", dove *Type* può essere "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="6aa9b-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="6aa9b-210">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-211">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-212">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-214">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="6aa9b-215">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="6aa9b-216">Queste risorse sono sicuramente disponibili per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="6aa9b-217">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-221">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="6aa9b-222">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="6aa9b-223">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-225">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-227">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="6aa9b-228">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="6aa9b-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unità dischetto** (14)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="6aa9b-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6aa9b-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-265">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-267">Specifica la quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="6aa9b-268">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="6aa9b-269">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-270">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-273">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="6aa9b-274">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="6aa9b-275">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-276">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-277">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-279">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="6aa9b-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-280">Matrice di stringhe di identificatori di questa risorsa presentata al sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="6aa9b-281">Questi valori vengono utilizzati solo se la proprietà **ResourceType** è impostata su 6 (HBA SCSI parallelo) e la proprietà **ResourceSubType** è impostata su "Microsoft Synthetic SCSI controller".</span><span class="sxs-lookup"><span data-stu-id="6aa9b-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="6aa9b-282">Questa proprietà è impostata su "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="6aa9b-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="6aa9b-283">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa9b-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6aa9b-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa9b-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6aa9b-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6aa9b-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aa9b-287">Intero che definisce il peso relativo per ogni processore di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="6aa9b-288">Una volta soddisfatte tutte le riservate, la capacità del processore fisico rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="6aa9b-289">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="6aa9b-290">Intervallo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="6aa9b-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6aa9b-291">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aa9b-291">Remarks</span></span>

<span data-ttu-id="6aa9b-292">L'accesso alla **classe \_ ResourceAllocationSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="6aa9b-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6aa9b-293">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6aa9b-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa9b-294">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aa9b-294">Requirements</span></span>



| <span data-ttu-id="6aa9b-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa9b-295">Requirement</span></span> | <span data-ttu-id="6aa9b-296">Valore</span><span class="sxs-lookup"><span data-stu-id="6aa9b-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa9b-297">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa9b-297">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa9b-298">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6aa9b-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6aa9b-299">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa9b-299">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa9b-300">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6aa9b-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6aa9b-301">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6aa9b-301">Namespace</span></span><br/>                | <span data-ttu-id="6aa9b-302">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6aa9b-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6aa9b-303">MOF</span><span class="sxs-lookup"><span data-stu-id="6aa9b-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6aa9b-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6aa9b-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6aa9b-305">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa9b-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa9b-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6aa9b-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6aa9b-307">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aa9b-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa9b-308">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="6aa9b-309">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="6aa9b-310">**MSVM \_ ResourceAllocationSettingData (V1)**</span><span class="sxs-lookup"><span data-stu-id="6aa9b-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="6aa9b-311">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6aa9b-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

