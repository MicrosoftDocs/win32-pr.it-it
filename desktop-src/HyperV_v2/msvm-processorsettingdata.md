---
description: Rappresenta le impostazioni del processore virtuale per una macchina virtuale.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Classe Msvm_ProcessorSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312901"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="7eaac-103">\_Classe MSVM ProcessorSettingData</span><span class="sxs-lookup"><span data-stu-id="7eaac-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="7eaac-104">Rappresenta le impostazioni del processore virtuale per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="7eaac-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7eaac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eaac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7eaac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="7eaac-107">Members</span><span class="sxs-lookup"><span data-stu-id="7eaac-107">Members</span></span>

<span data-ttu-id="7eaac-108">La **classe \_ ProcessorSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7eaac-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7eaac-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eaac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eaac-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eaac-110">Properties</span></span>

<span data-ttu-id="7eaac-111">La **classe \_ ProcessorSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7eaac-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eaac-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="7eaac-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-115">The address of the resource.</span></span> <span data-ttu-id="7eaac-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="7eaac-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="7eaac-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="7eaac-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="7eaac-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="7eaac-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="7eaac-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="7eaac-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="7eaac-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="7eaac-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7eaac-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="7eaac-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="7eaac-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7eaac-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="7eaac-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7eaac-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-141">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7eaac-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7eaac-142">A short description of the object.</span></span> <span data-ttu-id="7eaac-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7eaac-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="7eaac-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-145">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7eaac-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-147">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-147">The device to which this resource is connected.</span></span> <span data-ttu-id="7eaac-148">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="7eaac-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eaac-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-152">Descrive la visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="7eaac-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="7eaac-153">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-154">**CpuGroupId**</span><span class="sxs-lookup"><span data-stu-id="7eaac-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-157">ID del gruppo di CPU a cui è associata questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="7eaac-158">Quando value è 0, significa che non è associato a un gruppo di CPU specifico.</span><span class="sxs-lookup"><span data-stu-id="7eaac-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="7eaac-159">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="7eaac-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaac-160">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7eaac-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-163">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7eaac-163">A description of the object.</span></span> <span data-ttu-id="7eaac-164">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7eaac-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7eaac-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-168">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7eaac-168">A display name for the object.</span></span> <span data-ttu-id="7eaac-169">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7eaac-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="7eaac-170">Se si modifica questa proprietà, viene modificato l' **elemento ElementName** del derivato del dispositivo logico associato.</span><span class="sxs-lookup"><span data-stu-id="7eaac-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-171">**EnableHostResourceProtection**</span><span class="sxs-lookup"><span data-stu-id="7eaac-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-174">Indica se la macchina virtuale deve abilitare le funzionalità che aumentano la protezione delle risorse host dal carico di lavoro in esecuzione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="7eaac-175">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7eaac-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaac-176">**ExposeVirtualizationExtensions**</span><span class="sxs-lookup"><span data-stu-id="7eaac-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-177">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-179">Indica se Hyper-V deve esporre le estensioni di virtualizzazione hardware virtualizzate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="7eaac-180">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="7eaac-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaac-181">**HideHypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="7eaac-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-182">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-184">Indica se Hyper-V deve segnalare che un hypervisor è presente nel Guest annidato.</span><span class="sxs-lookup"><span data-stu-id="7eaac-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="7eaac-185">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="7eaac-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaac-186">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="7eaac-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-187">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7eaac-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-189">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7eaac-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="7eaac-190">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7eaac-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-191">**HwThreadsPerCore**</span><span class="sxs-lookup"><span data-stu-id="7eaac-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-192">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-194">Indica il numero di thread SMT per core segnalato al Guest.</span><span class="sxs-lookup"><span data-stu-id="7eaac-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="7eaac-195">Questa segnalazione è indipendente dal fatto che sia presente l'hardware per SMT.</span><span class="sxs-lookup"><span data-stu-id="7eaac-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="7eaac-196">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="7eaac-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaac-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7eaac-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-200">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7eaac-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-201">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7eaac-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7eaac-202">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7eaac-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="7eaac-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-204">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-206">Quantità massima di risorse della CPU che possono essere utilizzate dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="7eaac-207">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7eaac-208">100000</span><span class="sxs-lookup"><span data-stu-id="7eaac-208">100000</span></span>

<span data-ttu-id="7eaac-209">Intervallo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="7eaac-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-210">**LimitCPUID**</span><span class="sxs-lookup"><span data-stu-id="7eaac-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-211">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-213">Indica se la macchina virtuale deve abbassare l'identificatore della CPU.</span><span class="sxs-lookup"><span data-stu-id="7eaac-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="7eaac-214">In alcuni sistemi operativi meno recenti potrebbe essere necessario limitare la funzionalità del processore in questo modo per poter essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="7eaac-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-215">**LimitProcessorFeatures**</span><span class="sxs-lookup"><span data-stu-id="7eaac-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7eaac-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-218">Indica se la macchina virtuale deve limitare le funzionalità della CPU esposte al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7eaac-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="7eaac-219">La limitazione delle funzionalità del processore consente la migrazione della macchina virtuale a diversi sistemi di computer host con processori diversi.</span><span class="sxs-lookup"><span data-stu-id="7eaac-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="7eaac-220">La migrazione di macchine virtuali tra computer con processori di fornitori diversi non è supportata.</span><span class="sxs-lookup"><span data-stu-id="7eaac-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-221">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="7eaac-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-222">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eaac-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-224">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7eaac-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="7eaac-225">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-226">**MaxNumaNodesPerSocket**</span><span class="sxs-lookup"><span data-stu-id="7eaac-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-227">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-229">Numero massimo di nodi NUMA che possono essere osservati all'interno della macchina virtuale come appartenenti a un socket a singolo processore.</span><span class="sxs-lookup"><span data-stu-id="7eaac-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-230">**MaxProcessorsPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="7eaac-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-231">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-233">Numero massimo di processori virtuali che possono essere osservati all'interno della macchina virtuale come appartenenti a un singolo nodo NUMA virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-234">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="7eaac-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-237">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7eaac-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="7eaac-238">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-239">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7eaac-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-242">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-242">The parent of the resource.</span></span> <span data-ttu-id="7eaac-243">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-244">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="7eaac-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-247">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="7eaac-248">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-249">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="7eaac-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-250">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-252">Quantità di risorse della CPU riservate per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="7eaac-253">Queste risorse sono sicuramente disponibili per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="7eaac-254">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7eaac-255">0</span><span class="sxs-lookup"><span data-stu-id="7eaac-255">0</span></span>

<span data-ttu-id="7eaac-256">Intervallo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="7eaac-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="7eaac-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-260">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="7eaac-261">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7eaac-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="7eaac-262">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="7eaac-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-264">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eaac-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-266">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="7eaac-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="7eaac-267">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="7eaac-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eaac-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-271">Il numero totale di core nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="7eaac-272">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="7eaac-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7eaac-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-276">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7eaac-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="7eaac-277">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7eaac-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="7eaac-278">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7eaac-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="7eaac-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eaac-280">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eaac-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eaac-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7eaac-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eaac-282">Il peso per ogni processore di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eaac-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="7eaac-283">Una volta soddisfatte tutte le riservate, la capacità del processore fisico rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi.</span><span class="sxs-lookup"><span data-stu-id="7eaac-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="7eaac-284">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7eaac-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7eaac-285">100</span><span class="sxs-lookup"><span data-stu-id="7eaac-285">100</span></span>

<span data-ttu-id="7eaac-286">Intervallo: 0 10000</span><span class="sxs-lookup"><span data-stu-id="7eaac-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eaac-287">Commenti</span><span class="sxs-lookup"><span data-stu-id="7eaac-287">Remarks</span></span>

<span data-ttu-id="7eaac-288">L'accesso alla **classe \_ ProcessorSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7eaac-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7eaac-289">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7eaac-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eaac-290">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7eaac-290">Requirements</span></span>



| <span data-ttu-id="7eaac-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eaac-291">Requirement</span></span> | <span data-ttu-id="7eaac-292">Valore</span><span class="sxs-lookup"><span data-stu-id="7eaac-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eaac-293">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eaac-293">Minimum supported client</span></span><br/> | <span data-ttu-id="7eaac-294">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7eaac-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7eaac-295">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eaac-295">Minimum supported server</span></span><br/> | <span data-ttu-id="7eaac-296">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7eaac-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7eaac-297">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7eaac-297">Namespace</span></span><br/>                | <span data-ttu-id="7eaac-298">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7eaac-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7eaac-299">MOF</span><span class="sxs-lookup"><span data-stu-id="7eaac-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eaac-300"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eaac-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eaac-301">DLL</span><span class="sxs-lookup"><span data-stu-id="7eaac-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eaac-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eaac-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eaac-303">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7eaac-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eaac-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7eaac-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="7eaac-305">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7eaac-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="7eaac-306">Classi del processore</span><span class="sxs-lookup"><span data-stu-id="7eaac-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

