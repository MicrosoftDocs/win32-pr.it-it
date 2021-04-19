---
description: Rappresenta lo stato configurato del servizio di scambio di coppie chiave/valore.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Classe Msvm_KvpExchangeComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311799"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="c08ef-103">\_Classe MSVM KvpExchangeComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="c08ef-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="c08ef-104">Rappresenta lo stato configurato del servizio di scambio di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="c08ef-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="c08ef-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c08ef-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c08ef-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="c08ef-107">Members</span><span class="sxs-lookup"><span data-stu-id="c08ef-107">Members</span></span>

<span data-ttu-id="c08ef-108">La **classe \_ KvpExchangeComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c08ef-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c08ef-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c08ef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c08ef-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c08ef-110">Properties</span></span>

<span data-ttu-id="c08ef-111">La **classe \_ KvpExchangeComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c08ef-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c08ef-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="c08ef-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c08ef-115">The address of the resource.</span></span> <span data-ttu-id="c08ef-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c08ef-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="c08ef-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="c08ef-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c08ef-121">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="c08ef-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c08ef-122">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="c08ef-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-126">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="c08ef-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c08ef-127">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="c08ef-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c08ef-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-131">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c08ef-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c08ef-132">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="c08ef-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c08ef-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-136">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c08ef-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="c08ef-137">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c08ef-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c08ef-141">A short description of the object.</span></span> <span data-ttu-id="c08ef-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c08ef-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c08ef-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-144">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c08ef-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-146">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c08ef-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="c08ef-147">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c08ef-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="c08ef-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c08ef-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-151">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="c08ef-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="c08ef-152">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c08ef-153">Valore</span><span class="sxs-lookup"><span data-stu-id="c08ef-153">Value</span></span>                                                                        | <span data-ttu-id="c08ef-154">Significato</span><span class="sxs-lookup"><span data-stu-id="c08ef-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="c08ef-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c08ef-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c08ef-156">Virtualizzato</span><span class="sxs-lookup"><span data-stu-id="c08ef-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c08ef-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c08ef-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="c08ef-160">A description of the object.</span></span> <span data-ttu-id="c08ef-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c08ef-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-162">**DisableHostKVPItems**</span><span class="sxs-lookup"><span data-stu-id="c08ef-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-163">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c08ef-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c08ef-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-165">Questa proprietà Disabilita l'host populatinghost automaticamente le informazioni sul nome e sul sistema operativo all'interno del Guest.</span><span class="sxs-lookup"><span data-stu-id="c08ef-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="c08ef-166">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="c08ef-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="c08ef-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c08ef-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-170">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c08ef-170">A display name for the object.</span></span> <span data-ttu-id="c08ef-171">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c08ef-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c08ef-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c08ef-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-175">Stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c08ef-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c08ef-176">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="c08ef-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c08ef-177">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="c08ef-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c08ef-178">**HostExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="c08ef-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-179">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c08ef-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-181">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="c08ef-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-182">Matrice di istanze di [**\_ KvpExchangeDataItem MSVM**](msvm-kvpexchangedataitem.md) incorporate che rappresentano le coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="c08ef-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-183">**HostOnlyItems**</span><span class="sxs-lookup"><span data-stu-id="c08ef-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-184">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c08ef-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-186">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="c08ef-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-187">Matrice di istanze di [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) contenenti le coppie chiave/valore archiviate nel file di configurazione ma non scambiate con il sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="c08ef-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="c08ef-188">Ciò consente alle applicazioni di archiviare i dati specifici della macchina virtuale che non devono essere visibili al sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="c08ef-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="c08ef-189">Gli elementi vengono formattati allo stesso modo degli elementi nella proprietà **HostExchangeItems** , ad eccezione della proprietà **source** dell'istanza **MSVM \_ KvpExchangeDataItem** , impostata su 4.</span><span class="sxs-lookup"><span data-stu-id="c08ef-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="c08ef-190">Ogni file di configurazione è limitato a 128 coppie chiave/valore, dove ogni campo valore può avere dimensioni massime di 16 KB e il campo chiave può essere fino a 512 byte.</span><span class="sxs-lookup"><span data-stu-id="c08ef-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-191">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="c08ef-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-192">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c08ef-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-194">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c08ef-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="c08ef-195">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c08ef-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c08ef-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-199">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="c08ef-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-200">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c08ef-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c08ef-201">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c08ef-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="c08ef-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c08ef-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-205">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c08ef-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="c08ef-206">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="c08ef-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c08ef-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-210">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="c08ef-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c08ef-211">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c08ef-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="c08ef-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-215">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c08ef-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="c08ef-216">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c08ef-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-220">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c08ef-220">The parent of the resource.</span></span> <span data-ttu-id="c08ef-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c08ef-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="c08ef-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-225">ID del pool di risorse da cui viene allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c08ef-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="c08ef-226">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-227">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="c08ef-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c08ef-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-230">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c08ef-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="c08ef-231">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="c08ef-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-235">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="c08ef-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="c08ef-236">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c08ef-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c08ef-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-240">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="c08ef-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="c08ef-241">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c08ef-242">Valore</span><span class="sxs-lookup"><span data-stu-id="c08ef-242">Value</span></span>                                                                        | <span data-ttu-id="c08ef-243">Significato</span><span class="sxs-lookup"><span data-stu-id="c08ef-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="c08ef-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c08ef-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c08ef-245">Altro</span><span class="sxs-lookup"><span data-stu-id="c08ef-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c08ef-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c08ef-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-247">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c08ef-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-249">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="c08ef-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="c08ef-250">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-251">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="c08ef-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c08ef-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-254">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c08ef-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="c08ef-255">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c08ef-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="c08ef-256">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c08ef-257">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c08ef-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08ef-258">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c08ef-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c08ef-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08ef-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08ef-260">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="c08ef-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="c08ef-261">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c08ef-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c08ef-262">Commenti</span><span class="sxs-lookup"><span data-stu-id="c08ef-262">Remarks</span></span>

<span data-ttu-id="c08ef-263">L'accesso alla **classe \_ KvpExchangeComponentSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c08ef-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c08ef-264">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c08ef-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c08ef-265">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c08ef-265">Requirements</span></span>



| <span data-ttu-id="c08ef-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08ef-266">Requirement</span></span> | <span data-ttu-id="c08ef-267">Valore</span><span class="sxs-lookup"><span data-stu-id="c08ef-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08ef-268">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08ef-268">Minimum supported client</span></span><br/> | <span data-ttu-id="c08ef-269">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c08ef-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c08ef-270">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08ef-270">Minimum supported server</span></span><br/> | <span data-ttu-id="c08ef-271">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c08ef-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c08ef-272">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c08ef-272">Namespace</span></span><br/>                | <span data-ttu-id="c08ef-273">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c08ef-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c08ef-274">MOF</span><span class="sxs-lookup"><span data-stu-id="c08ef-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c08ef-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c08ef-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c08ef-276">DLL</span><span class="sxs-lookup"><span data-stu-id="c08ef-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c08ef-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c08ef-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c08ef-278">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c08ef-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08ef-279">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c08ef-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="c08ef-280">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c08ef-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

