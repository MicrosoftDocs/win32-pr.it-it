---
description: Rappresenta lo stato configurato di una porta Fibre Channel sintetica o di una porta di commutazione Fibre Channel.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Classe Msvm_FcPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307917"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="518be-103">\_Classe MSVM FcPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="518be-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="518be-104">Rappresenta lo stato configurato di una porta Fibre Channel sintetica o di una porta di commutazione Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="518be-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="518be-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="518be-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="518be-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="518be-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="518be-107">Members</span><span class="sxs-lookup"><span data-stu-id="518be-107">Members</span></span>

<span data-ttu-id="518be-108">La **classe \_ FcPortAllocationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="518be-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="518be-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="518be-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="518be-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="518be-110">Properties</span></span>

<span data-ttu-id="518be-111">La **classe \_ FcPortAllocationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="518be-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="518be-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="518be-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-115">The address of the resource.</span></span> <span data-ttu-id="518be-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="518be-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="518be-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="518be-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="518be-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="518be-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="518be-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="518be-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="518be-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="518be-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="518be-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="518be-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="518be-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="518be-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="518be-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="518be-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="518be-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="518be-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="518be-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="518be-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="518be-141">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="518be-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="518be-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="518be-142">A short description of the object.</span></span> <span data-ttu-id="518be-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="518be-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="518be-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="518be-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-145">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="518be-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="518be-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-147">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-147">The device to which this resource is connected.</span></span> <span data-ttu-id="518be-148">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="518be-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="518be-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="518be-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-152">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="518be-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="518be-153">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-154">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="518be-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-157">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="518be-157">A description of the object.</span></span> <span data-ttu-id="518be-158">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="518be-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="518be-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="518be-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-162">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="518be-162">A display name for the object.</span></span> <span data-ttu-id="518be-163">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="518be-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="518be-164">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="518be-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="518be-165">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="518be-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="518be-166">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="518be-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-167">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="518be-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="518be-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-169">È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="518be-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="518be-170">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="518be-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="518be-171">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="518be-172">Si tratta di una proprietà di sola lettura, ma se la proprietà **ResourceType** è 22 (disco) e la proprietà **ResourceSubType** è "unità disco fisico Microsoft", può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="518be-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="518be-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="518be-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="518be-176">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="518be-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="518be-177">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="518be-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="518be-178">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="518be-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="518be-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="518be-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-180">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="518be-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="518be-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-182">Quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="518be-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="518be-183">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="518be-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="518be-184">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-185">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="518be-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-186">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="518be-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="518be-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-188">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="518be-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="518be-189">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-190">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="518be-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-193">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="518be-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="518be-194">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-195">**Parent**</span><span class="sxs-lookup"><span data-stu-id="518be-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-198">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-198">The parent of the resource.</span></span> <span data-ttu-id="518be-199">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-200">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="518be-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-203">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="518be-204">Per le istanze associate a una macchina virtuale, si tratta di "Microsoft:*GUID* \\ *dati specifici del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="518be-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="518be-205">Per le istanze che definiscono le potenziali impostazioni per una macchina virtuale, questo sarà "Microsoft: Definition \\ *GUID* \\ *Type*", dove *Type* può essere "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="518be-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="518be-206">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-207">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="518be-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-208">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="518be-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="518be-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-210">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="518be-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="518be-211">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="518be-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="518be-212">Queste risorse sono sicuramente disponibili per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="518be-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="518be-213">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="518be-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-217">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="518be-218">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="518be-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="518be-219">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="518be-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="518be-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="518be-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-223">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="518be-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="518be-224">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="518be-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="518be-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="518be-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="518be-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="518be-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="518be-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="518be-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="518be-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="518be-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="518be-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="518be-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="518be-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="518be-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="518be-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="518be-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="518be-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="518be-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="518be-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="518be-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="518be-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="518be-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="518be-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="518be-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="518be-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="518be-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="518be-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="518be-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="518be-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="518be-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="518be-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="518be-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="518be-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="518be-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (17)</span><span class="sxs-lookup"><span data-stu-id="518be-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="518be-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (18)</span><span class="sxs-lookup"><span data-stu-id="518be-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="518be-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (19)</span><span class="sxs-lookup"><span data-stu-id="518be-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="518be-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (20)</span><span class="sxs-lookup"><span data-stu-id="518be-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="518be-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (21)</span><span class="sxs-lookup"><span data-stu-id="518be-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="518be-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="518be-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="518be-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Nastro** (23)</span><span class="sxs-lookup"><span data-stu-id="518be-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="518be-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (24)</span><span class="sxs-lookup"><span data-stu-id="518be-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="518be-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controller FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="518be-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="518be-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="518be-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="518be-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="518be-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="518be-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)</span><span class="sxs-lookup"><span data-stu-id="518be-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="518be-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="518be-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="518be-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="518be-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="518be-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="518be-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="518be-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="518be-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-257">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="518be-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="518be-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-259">Specifica la quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="518be-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="518be-260">L'unità di misura per questa proprietà viene specificata dalla proprietà **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="518be-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="518be-261">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-262">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="518be-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="518be-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="518be-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-265">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="518be-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="518be-266">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="518be-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="518be-267">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="518be-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="518be-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="518be-269">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="518be-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="518be-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="518be-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="518be-271">Intero che definisce il peso relativo per ogni processore di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="518be-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="518be-272">Una volta soddisfatte tutte le riservate, la capacità del processore fisico rimanente della piattaforma di hosting verrà allocata alle macchine virtuali in base ai pesi relativi.</span><span class="sxs-lookup"><span data-stu-id="518be-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="518be-273">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="518be-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="518be-274">Intervallo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="518be-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="518be-275">Requisiti</span><span class="sxs-lookup"><span data-stu-id="518be-275">Requirements</span></span>



| <span data-ttu-id="518be-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="518be-276">Requirement</span></span> | <span data-ttu-id="518be-277">Valore</span><span class="sxs-lookup"><span data-stu-id="518be-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="518be-278">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="518be-278">Minimum supported client</span></span><br/> | <span data-ttu-id="518be-279">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="518be-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="518be-280">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="518be-280">Minimum supported server</span></span><br/> | <span data-ttu-id="518be-281">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="518be-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="518be-282">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="518be-282">Namespace</span></span><br/>                | <span data-ttu-id="518be-283">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="518be-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="518be-284">MOF</span><span class="sxs-lookup"><span data-stu-id="518be-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="518be-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="518be-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="518be-286">DLL</span><span class="sxs-lookup"><span data-stu-id="518be-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="518be-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="518be-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

