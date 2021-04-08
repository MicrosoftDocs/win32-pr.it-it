---
description: Rappresenta lo stato configurato della memoria per una macchina virtuale.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Classe Msvm_MemorySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967428"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="1ad52-103">\_Classe MSVM MemorySettingData</span><span class="sxs-lookup"><span data-stu-id="1ad52-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="1ad52-104">Rappresenta lo stato configurato della memoria per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="1ad52-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1ad52-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad52-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ad52-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="1ad52-107">Members</span><span class="sxs-lookup"><span data-stu-id="1ad52-107">Members</span></span>

<span data-ttu-id="1ad52-108">La **classe \_ MemorySettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1ad52-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1ad52-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ad52-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ad52-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ad52-110">Properties</span></span>

<span data-ttu-id="1ad52-111">La **classe \_ MemorySettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ad52-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ad52-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="1ad52-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-115">The address of the resource.</span></span> <span data-ttu-id="1ad52-116">Ad esempio, l'indirizzo MAC di una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1ad52-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="1ad52-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="1ad52-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-121">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="1ad52-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="1ad52-122">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="1ad52-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="1ad52-123">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="1ad52-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-127">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="1ad52-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="1ad52-128">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="1ad52-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-132">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="1ad52-133">Ad esempio, quando questa proprietà è impostata su **true** e la macchina virtuale che lo utilizza è accesa, questa risorsa verrebbe allocata.</span><span class="sxs-lookup"><span data-stu-id="1ad52-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="1ad52-134">Il valore **false** indica che la risorsa deve essere allocata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1ad52-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="1ad52-135">Ad esempio, l'impostazione può rappresentare supporti rimovibili, ad esempio un CD-ROM o un disco floppy, in cui all'avvio, il supporto non è presente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="1ad52-136">Per allocare la risorsa è necessaria un'operazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="1ad52-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="1ad52-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-138">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="1ad52-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-141">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="1ad52-142">Ad esempio, quando questa proprietà è impostata su **true** e la macchina virtuale che lo utilizza è accesa, questa risorsa verrebbe allocata.</span><span class="sxs-lookup"><span data-stu-id="1ad52-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="1ad52-143">Quando questa proprietà è **false**, la risorsa deve essere allocata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1ad52-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="1ad52-144">Ad esempio, l'impostazione può rappresentare supporti rimovibili, ad esempio un CD-ROM o un disco floppy, in cui all'avvio, il supporto non è presente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="1ad52-145">Per allocare la risorsa è necessaria un'operazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="1ad52-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="1ad52-146">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-147">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1ad52-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-150">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1ad52-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-151">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ad52-151">A short description of the object.</span></span> <span data-ttu-id="1ad52-152">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1ad52-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-153">**Connection**</span><span class="sxs-lookup"><span data-stu-id="1ad52-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-154">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1ad52-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-156">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-156">The device to which this resource is connected.</span></span> <span data-ttu-id="1ad52-157">Ad esempio, una rete denominata o una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="1ad52-157">For example, a named network or switch port.</span></span> <span data-ttu-id="1ad52-158">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="1ad52-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ad52-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-162">Descrive la visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="1ad52-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="1ad52-163">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-164">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1ad52-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-167">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1ad52-167">A description of the object.</span></span> <span data-ttu-id="1ad52-168">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1ad52-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="1ad52-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-172">Indica se la memoria dinamica è abilitata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1ad52-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-176">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ad52-176">A display name for the object.</span></span> <span data-ttu-id="1ad52-177">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ad52-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-178">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="1ad52-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-179">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1ad52-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-181">Il primo elemento di questa matrice contiene un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="1ad52-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="1ad52-182">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="1ad52-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="1ad52-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1ad52-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-186">Indica se la memoria è supportata da 1 GB di pagine.</span><span class="sxs-lookup"><span data-stu-id="1ad52-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ad52-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-190">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="1ad52-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-191">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1ad52-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1ad52-192">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1ad52-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-193">**Virtualizzato**</span><span class="sxs-lookup"><span data-stu-id="1ad52-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-194">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-196">Indica se il dispositivo è virtualizzato o passato.</span><span class="sxs-lookup"><span data-stu-id="1ad52-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="1ad52-197">Se è impostato su **false**, viene utilizzata la risorsa host o sottostante.</span><span class="sxs-lookup"><span data-stu-id="1ad52-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="1ad52-198">Nella proprietà **DeviceID** deve essere presente almeno un elemento.</span><span class="sxs-lookup"><span data-stu-id="1ad52-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="1ad52-199">Quando è impostato su **true**, la risorsa è virtualizzata e non può essere mappata direttamente a una risorsa sottostante/host.</span><span class="sxs-lookup"><span data-stu-id="1ad52-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="1ad52-200">Alcune implementazioni possono supportare un'assegnazione specifica per le risorse virtualizzate, nel qual caso le risorse host vengono esposte tramite la proprietà **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="1ad52-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="1ad52-201">Questa proprietà è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="1ad52-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="1ad52-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ad52-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-205">Quantità massima di memoria che può essere utilizzata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="1ad52-206">Per una macchina virtuale con la memoria dinamica abilitata, rappresenta l'impostazione di memoria massima.</span><span class="sxs-lookup"><span data-stu-id="1ad52-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="1ad52-207">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="1ad52-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-209">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ad52-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-211">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="1ad52-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="1ad52-212">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-213">**MaxMemoryBlocksPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="1ad52-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-214">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ad52-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-216">Quantità massima di memoria che può essere osservata all'interno della macchina virtuale come appartenente a un singolo nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="1ad52-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="1ad52-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-220">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore "other".</span><span class="sxs-lookup"><span data-stu-id="1ad52-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="1ad52-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1ad52-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-225">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-225">The parent of the resource.</span></span> <span data-ttu-id="1ad52-226">Ad esempio, un controller per l'allocazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="1ad52-227">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="1ad52-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-231">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="1ad52-232">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-233">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="1ad52-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-234">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ad52-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-236">Specifica la quantità di memoria garantita per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="1ad52-237">Per una macchina virtuale con la memoria dinamica abilitata, rappresenta l'impostazione minima della memoria.</span><span class="sxs-lookup"><span data-stu-id="1ad52-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="1ad52-238">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1ad52-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-242">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="1ad52-243">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ad52-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="1ad52-244">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1ad52-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-246">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ad52-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-248">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="1ad52-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="1ad52-249">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 4 (memoria).</span><span class="sxs-lookup"><span data-stu-id="1ad52-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-250">**SgxEnabled**</span><span class="sxs-lookup"><span data-stu-id="1ad52-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-253">Indica se SGX è abilitato.</span><span class="sxs-lookup"><span data-stu-id="1ad52-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="1ad52-254">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="1ad52-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ad52-255">**SgxSize**</span><span class="sxs-lookup"><span data-stu-id="1ad52-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-256">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ad52-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-258">Quantità di memoria SGX da allocare per la macchina virtuale, in MB.</span><span class="sxs-lookup"><span data-stu-id="1ad52-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="1ad52-259">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="1ad52-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ad52-260">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="1ad52-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-261">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ad52-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-263">**True** se il paging di secondo livello è attivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1ad52-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-264">**TargetMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="1ad52-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-265">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ad52-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-267">Definisce la quantità di memoria aggiuntiva che deve essere riservata per una macchina virtuale in fase di esecuzione, come percentuale della memoria totale necessaria per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="1ad52-268">Questo vale solo per le macchine virtuali con la memoria dinamica abilitata.</span><span class="sxs-lookup"><span data-stu-id="1ad52-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="1ad52-269">Questa proprietà può essere compresa tra 5 e 2000.</span><span class="sxs-lookup"><span data-stu-id="1ad52-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="1ad52-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-271">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ad52-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-273">Quantità totale di RAM nella macchina virtuale, come osservato dal sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="1ad52-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="1ad52-274">Per una macchina virtuale con la memoria dinamica abilitata, rappresenta la memoria iniziale disponibile all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1ad52-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="1ad52-275">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-276">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="1ad52-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ad52-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-279">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1ad52-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="1ad52-280">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1ad52-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="1ad52-281">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1ad52-282">**Weight**</span><span class="sxs-lookup"><span data-stu-id="1ad52-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ad52-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ad52-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ad52-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ad52-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ad52-285">Definisce il valore di ponderazione dell'allocazione di memoria per ogni macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ad52-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="1ad52-286">Una volta soddisfatte tutte le riservate, la memoria rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi (non superare il valore specificato dalla proprietà **limit** ).</span><span class="sxs-lookup"><span data-stu-id="1ad52-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="1ad52-287">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1ad52-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ad52-288">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ad52-288">Remarks</span></span>

<span data-ttu-id="1ad52-289">L'accesso alla **classe \_ MemorySettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="1ad52-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1ad52-290">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1ad52-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="1ad52-291">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ad52-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="1ad52-292">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ad52-292">Requirements</span></span>



| <span data-ttu-id="1ad52-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ad52-293">Requirement</span></span> | <span data-ttu-id="1ad52-294">Valore</span><span class="sxs-lookup"><span data-stu-id="1ad52-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad52-295">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ad52-295">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad52-296">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ad52-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ad52-297">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ad52-297">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad52-298">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ad52-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ad52-299">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ad52-299">Namespace</span></span><br/>                | <span data-ttu-id="1ad52-300">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ad52-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ad52-301">MOF</span><span class="sxs-lookup"><span data-stu-id="1ad52-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ad52-302"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ad52-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ad52-303">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad52-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ad52-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ad52-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ad52-305">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ad52-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad52-306">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1ad52-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="1ad52-307">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1ad52-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="1ad52-308">Classi di memoria</span><span class="sxs-lookup"><span data-stu-id="1ad52-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

