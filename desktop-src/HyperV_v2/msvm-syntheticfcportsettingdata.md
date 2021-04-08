---
description: Rappresenta lo stato configurato di una porta Fibre Channel sintetica.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Classe Msvm_SyntheticFcPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750199"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="b6c07-103">\_Classe MSVM SyntheticFcPortSettingData</span><span class="sxs-lookup"><span data-stu-id="b6c07-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="b6c07-104">Rappresenta lo stato configurato di una porta Fibre Channel sintetica.</span><span class="sxs-lookup"><span data-stu-id="b6c07-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="b6c07-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b6c07-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c07-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6c07-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="b6c07-107">Members</span><span class="sxs-lookup"><span data-stu-id="b6c07-107">Members</span></span>

<span data-ttu-id="b6c07-108">La **classe \_ SyntheticFcPortSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b6c07-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b6c07-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6c07-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6c07-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6c07-110">Properties</span></span>

<span data-ttu-id="b6c07-111">La **classe \_ SyntheticFcPortSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6c07-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6c07-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="b6c07-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-115">The address of the resource.</span></span> <span data-ttu-id="b6c07-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="b6c07-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="b6c07-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b6c07-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="b6c07-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b6c07-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="b6c07-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-126">Unità di allocazione utilizzata dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="b6c07-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b6c07-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="b6c07-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6c07-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b6c07-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="b6c07-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="b6c07-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6c07-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b6c07-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="b6c07-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b6c07-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-141">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="b6c07-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6c07-142">A short description of the object.</span></span> <span data-ttu-id="b6c07-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b6c07-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-144">**ChapEnabled**</span><span class="sxs-lookup"><span data-stu-id="b6c07-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b6c07-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-147">Indica che questa porta è stata configurata con un segreto condiviso usando DH-CHAP, che consente all'infrastruttura Fibre Channel di autenticare che questa macchina virtuale può usare in modo legittimo i nomi universali assegnati a questa porta.</span><span class="sxs-lookup"><span data-stu-id="b6c07-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-148">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b6c07-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-149">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b6c07-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-151">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-151">The device to which this resource is connected.</span></span> <span data-ttu-id="b6c07-152">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-153">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="b6c07-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c07-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-156">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="b6c07-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="b6c07-157">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-158">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b6c07-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-161">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b6c07-161">A description of the object.</span></span> <span data-ttu-id="b6c07-162">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b6c07-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b6c07-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-166">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6c07-166">A display name for the object.</span></span> <span data-ttu-id="b6c07-167">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6c07-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="b6c07-168">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="b6c07-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="b6c07-169">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c07-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-170">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="b6c07-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-171">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b6c07-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-173">È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="b6c07-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="b6c07-174">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="b6c07-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="b6c07-175">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b6c07-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-179">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b6c07-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-180">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b6c07-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b6c07-181">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6c07-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-182">**Limite**</span><span class="sxs-lookup"><span data-stu-id="b6c07-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-183">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b6c07-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-185">Quantità massima di risorse host corrispondenti che possono essere utilizzate dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="b6c07-186">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-187">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="b6c07-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c07-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-190">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="b6c07-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="b6c07-191">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-192">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="b6c07-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-195">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b6c07-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="b6c07-196">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b6c07-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-197">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b6c07-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-200">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-200">The parent of the resource.</span></span> <span data-ttu-id="b6c07-201">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-202">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="b6c07-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-205">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="b6c07-206">Per le istanze associate a una macchina virtuale, si tratta di "Microsoft:*GUID* \\ *dati specifici del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="b6c07-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="b6c07-207">Per le istanze che definiscono le potenziali impostazioni per una macchina virtuale, questo sarà "Microsoft: Definition \\ *GUID* \\ *Type*", dove *Type* può essere "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="b6c07-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="b6c07-208">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-209">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="b6c07-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-210">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b6c07-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-212">Quantità di risorse riservate per l'utilizzo da parte della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="b6c07-213">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b6c07-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b6c07-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-217">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="b6c07-218">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c07-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="b6c07-219">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b6c07-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6c07-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-223">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="b6c07-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="b6c07-224">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="b6c07-225">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c07-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="b6c07-226">Significato</span><span class="sxs-lookup"><span data-stu-id="b6c07-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="b6c07-227"><dt>**HBA FC**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b6c07-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="b6c07-228">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="b6c07-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b6c07-229">**SecondaryWWNN**</span><span class="sxs-lookup"><span data-stu-id="b6c07-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-232">Indica il nome del nodo universale della porta HBA virtuale da utilizzare durante la migrazione in tempo reale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-233">**SecondaryWWPN**</span><span class="sxs-lookup"><span data-stu-id="b6c07-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-236">Indica il nome della porta universale della porta HBA virtuale da utilizzare durante la migrazione in tempo reale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-237">**VirtualPortWWNN**</span><span class="sxs-lookup"><span data-stu-id="b6c07-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-240">Indica il nome del nodo universale della porta HBA virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-241">**VirtualPortWWPN**</span><span class="sxs-lookup"><span data-stu-id="b6c07-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-244">Indica il nome della porta universale della porta HBA virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b6c07-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-246">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b6c07-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-248">Specifica la quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="b6c07-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="b6c07-249">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-250">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="b6c07-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b6c07-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-253">Specifica l'unità di misura per la proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="b6c07-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="b6c07-254">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b6c07-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="b6c07-255">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b6c07-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-256">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="b6c07-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-257">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b6c07-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-259">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="b6c07-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-260">Matrice di stringhe di identificatori di questa risorsa presentata al sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="b6c07-261">Gli indici e i valori per indice vengono definiti in base alle singole risorse, ovvero per ogni valore di **ResourceType** enumerato.</span><span class="sxs-lookup"><span data-stu-id="b6c07-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="b6c07-262">Questa proprietà non viene utilizzata</span><span class="sxs-lookup"><span data-stu-id="b6c07-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="b6c07-263">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b6c07-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c07-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6c07-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6c07-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b6c07-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6c07-266">Intero che definisce il peso relativo per ogni processore di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6c07-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="b6c07-267">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b6c07-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6c07-268">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6c07-268">Requirements</span></span>



| <span data-ttu-id="b6c07-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c07-269">Requirement</span></span> | <span data-ttu-id="b6c07-270">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c07-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c07-271">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6c07-271">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c07-272">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b6c07-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b6c07-273">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6c07-273">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c07-274">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b6c07-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6c07-275">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6c07-275">Namespace</span></span><br/>                | <span data-ttu-id="b6c07-276">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6c07-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b6c07-277">MOF</span><span class="sxs-lookup"><span data-stu-id="b6c07-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6c07-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6c07-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6c07-279">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c07-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c07-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6c07-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

