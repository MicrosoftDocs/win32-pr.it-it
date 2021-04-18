---
description: Rappresenta le impostazioni per un controller di visualizzazione 3D sintetico per una macchina virtuale.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Classe Msvm_Synthetic3DDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310005"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="18740-103">\_Classe MSVM Synthetic3DDisplayControllerSettingData</span><span class="sxs-lookup"><span data-stu-id="18740-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="18740-104">Rappresenta le impostazioni per un controller di visualizzazione 3D sintetico per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="18740-105">Questa classe viene utilizzata solo con le macchine virtuali che utilizzano RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="18740-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="18740-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="18740-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18740-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18740-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
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
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="18740-108">Members</span><span class="sxs-lookup"><span data-stu-id="18740-108">Members</span></span>

<span data-ttu-id="18740-109">La **classe \_ Synthetic3DDisplayControllerSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="18740-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="18740-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18740-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18740-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18740-111">Properties</span></span>

<span data-ttu-id="18740-112">La **classe \_ Synthetic3DDisplayControllerSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="18740-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18740-113">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="18740-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-116">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-116">The address of the resource.</span></span> <span data-ttu-id="18740-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="18740-118">Si tratta di una proprietà di sola lettura, ma se la proprietà **ResourceType** è 20 (controller grafico), è possibile modificarla utilizzando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="18740-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="18740-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="18740-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-122">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="18740-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="18740-123">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="18740-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="18740-124">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="18740-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-128">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="18740-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="18740-129">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="18740-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18740-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18740-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-133">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18740-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="18740-134">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="18740-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="18740-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18740-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-138">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18740-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="18740-139">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-140">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="18740-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18740-143">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="18740-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="18740-144">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18740-144">A short description of the object.</span></span> <span data-ttu-id="18740-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18740-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18740-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="18740-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-147">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="18740-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18740-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-149">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-149">The device to which this resource is connected.</span></span> <span data-ttu-id="18740-150">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="18740-151">Si tratta di una proprietà di sola lettura, ma se 1) la proprietà **ResourceType** è 17 (porta seriale), o 2) la **Proprietà ResourceType** è 21 (extent di archiviazione) e la proprietà **ResourceSubType** è "Microsoft Virtual Hard Disk", può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="18740-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="18740-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="18740-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18740-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18740-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-155">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="18740-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="18740-156">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="18740-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="18740-160">A description of the object.</span></span> <span data-ttu-id="18740-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18740-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18740-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18740-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-165">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18740-165">A display name for the object.</span></span> <span data-ttu-id="18740-166">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18740-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="18740-167">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="18740-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="18740-168">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="18740-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-169">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="18740-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18740-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-171">È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="18740-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="18740-172">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="18740-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="18740-173">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18740-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-177">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="18740-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18740-178">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18740-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18740-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="18740-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-180">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18740-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18740-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-182">Quantità massima di risorse host corrispondenti che possono essere utilizzate dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="18740-183">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-184">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="18740-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18740-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18740-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-187">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="18740-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="18740-188">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-189">**MaximumMonitors**</span><span class="sxs-lookup"><span data-stu-id="18740-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-190">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18740-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18740-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="18740-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18740-192">Numero massimo di monitor disponibili per il controller di visualizzazione 3D.</span><span class="sxs-lookup"><span data-stu-id="18740-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="18740-193">Il numero minimo di monitoraggi è 1 e il valore massimo dipende dalla risoluzione massima dello schermo.</span><span class="sxs-lookup"><span data-stu-id="18740-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="18740-194">La tabella seguente definisce il numero massimo di monitoraggi consentiti per diverse risoluzioni.</span><span class="sxs-lookup"><span data-stu-id="18740-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="18740-195">Soluzione</span><span class="sxs-lookup"><span data-stu-id="18740-195">Resolution</span></span>            | <span data-ttu-id="18740-196">Numero massimo di monitoraggi</span><span class="sxs-lookup"><span data-stu-id="18740-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="18740-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="18740-197">1024  768</span></span><br/>  | <span data-ttu-id="18740-198">4</span><span class="sxs-lookup"><span data-stu-id="18740-198">4</span></span><br/>     |
| <span data-ttu-id="18740-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="18740-199">1280  1024</span></span><br/> | <span data-ttu-id="18740-200">4</span><span class="sxs-lookup"><span data-stu-id="18740-200">4</span></span><br/>     |
| <span data-ttu-id="18740-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="18740-201">1600  1200</span></span><br/> | <span data-ttu-id="18740-202">3</span><span class="sxs-lookup"><span data-stu-id="18740-202">3</span></span><br/>     |
| <span data-ttu-id="18740-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="18740-203">1920  1200</span></span><br/> | <span data-ttu-id="18740-204">2</span><span class="sxs-lookup"><span data-stu-id="18740-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="18740-205">**MaximumScreenResolution**</span><span class="sxs-lookup"><span data-stu-id="18740-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-206">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="18740-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18740-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-208">Specifica la risoluzione massima dello schermo per il controller di visualizzazione 3D.</span><span class="sxs-lookup"><span data-stu-id="18740-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="18740-209">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="18740-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="18740-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="18740-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18740-211">La risoluzione massima è 1024 768.</span><span class="sxs-lookup"><span data-stu-id="18740-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="18740-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="18740-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18740-213">La risoluzione massima è 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="18740-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="18740-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="18740-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18740-215">La risoluzione massima è 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="18740-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="18740-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="18740-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18740-217">La risoluzione massima è 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="18740-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="18740-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="18740-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18740-219">La risoluzione massima è 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="18740-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="18740-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="18740-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18740-221">La risoluzione massima è 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="18740-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="18740-222">Aggiunta in Windows 10 e Windows Server 2016. MSVM \_ synte</span><span class="sxs-lookup"><span data-stu-id="18740-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18740-223">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="18740-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-226">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="18740-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="18740-227">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-228">**Parent**</span><span class="sxs-lookup"><span data-stu-id="18740-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-231">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-231">The parent of the resource.</span></span> <span data-ttu-id="18740-232">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-233">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="18740-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-236">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="18740-237">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-238">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="18740-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-239">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18740-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18740-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-241">Quantità di risorse della CPU riservate per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="18740-242">Queste risorse sono sicuramente disponibili per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="18740-243">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="18740-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-247">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="18740-248">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="18740-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="18740-249">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="18740-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-251">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18740-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18740-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-253">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="18740-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="18740-254">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="18740-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-256">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18740-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18740-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-258">Il numero totale di core nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="18740-259">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-260">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="18740-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="18740-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18740-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-263">Specifica l'unità di misura per la proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="18740-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="18740-264">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="18740-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="18740-265">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="18740-266">**VRAMSizeBytes**</span><span class="sxs-lookup"><span data-stu-id="18740-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-267">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18740-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18740-268">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="18740-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18740-269">Dimensioni della memoria del video per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="18740-270">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="18740-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="18740-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="18740-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18740-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="18740-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18740-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="18740-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18740-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="18740-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="18740-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="18740-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18740-276">**Weight**</span><span class="sxs-lookup"><span data-stu-id="18740-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18740-277">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18740-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18740-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="18740-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18740-279">Intero che definisce il peso per ogni processore di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18740-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="18740-280">Una volta soddisfatte tutte le riservate, la capacità del processore fisico rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi.</span><span class="sxs-lookup"><span data-stu-id="18740-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="18740-281">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="18740-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="18740-282">0</span><span class="sxs-lookup"><span data-stu-id="18740-282">0</span></span>

<span data-ttu-id="18740-283">Intervallo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="18740-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18740-284">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18740-284">Requirements</span></span>



| <span data-ttu-id="18740-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="18740-285">Requirement</span></span> | <span data-ttu-id="18740-286">Valore</span><span class="sxs-lookup"><span data-stu-id="18740-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18740-287">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18740-287">Minimum supported client</span></span><br/> | <span data-ttu-id="18740-288">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="18740-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18740-289">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18740-289">Minimum supported server</span></span><br/> | <span data-ttu-id="18740-290">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="18740-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18740-291">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18740-291">Namespace</span></span><br/>                | <span data-ttu-id="18740-292">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="18740-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18740-293">MOF</span><span class="sxs-lookup"><span data-stu-id="18740-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18740-294"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18740-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18740-295">DLL</span><span class="sxs-lookup"><span data-stu-id="18740-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18740-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18740-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

