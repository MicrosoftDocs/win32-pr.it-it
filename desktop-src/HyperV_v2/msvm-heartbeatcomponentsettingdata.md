---
description: Rappresenta lo stato configurato del servizio heartbeat.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Classe Msvm_HeartbeatComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307905"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="7acc6-103">\_Classe MSVM HeartbeatComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="7acc6-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="7acc6-104">Rappresenta lo stato configurato del servizio heartbeat.</span><span class="sxs-lookup"><span data-stu-id="7acc6-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="7acc6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7acc6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acc6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7acc6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="7acc6-107">Members</span><span class="sxs-lookup"><span data-stu-id="7acc6-107">Members</span></span>

<span data-ttu-id="7acc6-108">La **classe \_ HeartbeatComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7acc6-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7acc6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acc6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7acc6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acc6-110">Properties</span></span>

<span data-ttu-id="7acc6-111">La **classe \_ HeartbeatComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7acc6-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7acc6-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="7acc6-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7acc6-115">The address of the resource.</span></span> <span data-ttu-id="7acc6-116">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="7acc6-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-120">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="7acc6-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="7acc6-121">Le  / proprietà **AddressOnParent** padre vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="7acc6-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="7acc6-122">Se, ad esempio, l'elemento padre è un controller PCI, questa proprietà specifica lo slot PCI del dispositivo figlio.</span><span class="sxs-lookup"><span data-stu-id="7acc6-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="7acc6-123">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="7acc6-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-127">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="7acc6-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="7acc6-128">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su "Integration Components".</span><span class="sxs-lookup"><span data-stu-id="7acc6-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="7acc6-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7acc6-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-132">Indica se la risorsa viene allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7acc6-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="7acc6-133">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="7acc6-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7acc6-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-137">Indica se la risorsa viene deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7acc6-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="7acc6-138">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7acc6-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7acc6-142">A short description of the object.</span></span> <span data-ttu-id="7acc6-143">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "heartbeat".</span><span class="sxs-lookup"><span data-stu-id="7acc6-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="7acc6-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-145">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7acc6-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-147">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="7acc6-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="7acc6-148">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="7acc6-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7acc6-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-152">Descrive la visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="7acc6-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="7acc6-153">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 3 (virtualizzata).</span><span class="sxs-lookup"><span data-stu-id="7acc6-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-154">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7acc6-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-157">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7acc6-157">A description of the object.</span></span> <span data-ttu-id="7acc6-158">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft heartbeat Service setting data".</span><span class="sxs-lookup"><span data-stu-id="7acc6-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7acc6-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-162">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7acc6-162">A display name for the object.</span></span> <span data-ttu-id="7acc6-163">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "heartbeat".</span><span class="sxs-lookup"><span data-stu-id="7acc6-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="7acc6-164">La modifica di questa proprietà comporterà la modifica della proprietà **ElementName** del derivato [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associato.</span><span class="sxs-lookup"><span data-stu-id="7acc6-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="7acc6-165">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7acc6-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7acc6-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7acc6-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-169">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7acc6-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="7acc6-170">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7acc6-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7acc6-171">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7acc6-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7acc6-172">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7acc6-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7acc6-173">**ErrorThreshold**</span><span class="sxs-lookup"><span data-stu-id="7acc6-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-174">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7acc6-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-176">Configurazione di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7acc6-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7acc6-177">Questa proprietà è sempre impostata su 2 (abilitato).</span><span class="sxs-lookup"><span data-stu-id="7acc6-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="7acc6-178">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7acc6-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-179">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="7acc6-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-180">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7acc6-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-182">Espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7acc6-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="7acc6-183">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7acc6-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-187">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7acc6-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-188">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7acc6-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7acc6-189">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="7acc6-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-190">**Interval**</span><span class="sxs-lookup"><span data-stu-id="7acc6-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-191">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7acc6-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-193">Intervallo, in millisecondi, tra i tentativi di ping.</span><span class="sxs-lookup"><span data-stu-id="7acc6-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="7acc6-194">Questo è sempre impostato su 2000.</span><span class="sxs-lookup"><span data-stu-id="7acc6-194">This is always set to 2000.</span></span>

<span data-ttu-id="7acc6-195">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7acc6-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-196">**Latency**</span><span class="sxs-lookup"><span data-stu-id="7acc6-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7acc6-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-199">La latenza massima prevista, in millisecondi, tra un ping di richiesta e una risposta prima che una determinata richiesta venga considerata eliminata.</span><span class="sxs-lookup"><span data-stu-id="7acc6-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="7acc6-200">Questa proprietà è sempre impostata su 1000.</span><span class="sxs-lookup"><span data-stu-id="7acc6-200">This property is always set to 1000.</span></span>

<span data-ttu-id="7acc6-201">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7acc6-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-202">**Limite**</span><span class="sxs-lookup"><span data-stu-id="7acc6-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7acc6-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-205">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="7acc6-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="7acc6-206">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="7acc6-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="7acc6-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7acc6-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-210">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7acc6-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="7acc6-211">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="7acc6-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-215">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e la proprietà **ResourceType** ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7acc6-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="7acc6-216">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su "Microsoft heartbeat Component".</span><span class="sxs-lookup"><span data-stu-id="7acc6-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7acc6-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-220">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7acc6-220">The parent of the resource.</span></span> <span data-ttu-id="7acc6-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="7acc6-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-225">ID del pool di risorse da cui viene allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7acc6-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="7acc6-226">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7acc6-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-227">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="7acc6-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7acc6-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-230">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="7acc6-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="7acc6-231">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="7acc6-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="7acc6-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-235">Sottotipo specifico di implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="7acc6-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="7acc6-236">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7acc6-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="7acc6-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7acc6-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-240">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="7acc6-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="7acc6-241">Questa proprietà viene ereditata dalla classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7acc6-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="7acc6-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-243">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7acc6-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-245">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="7acc6-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="7acc6-246">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="7acc6-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-247">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="7acc6-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7acc6-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-250">Specifica le unità utilizzate dalla proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="7acc6-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="7acc6-251">Ad esempio, se ResourceType = Processor, il valore della proprietà **VirtualQuantityUnits** può essere impostato su "count", che indica che il valore della proprietà **VirtualQuantity** è espresso come conteggio.</span><span class="sxs-lookup"><span data-stu-id="7acc6-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="7acc6-252">Se ResourceType = Memory, il valore della proprietà **VirtualQuantityUnits** può essere impostato su "bytes \* 10 ^ 3", a indicare che il valore della proprietà **VirtualQuantity** è espresso in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="7acc6-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="7acc6-253">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su "count".</span><span class="sxs-lookup"><span data-stu-id="7acc6-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="7acc6-254">**Weight**</span><span class="sxs-lookup"><span data-stu-id="7acc6-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7acc6-255">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7acc6-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7acc6-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7acc6-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7acc6-257">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="7acc6-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="7acc6-258">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="7acc6-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7acc6-259">Commenti</span><span class="sxs-lookup"><span data-stu-id="7acc6-259">Remarks</span></span>

<span data-ttu-id="7acc6-260">L'accesso alla **classe \_ HeartbeatComponentSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7acc6-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7acc6-261">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7acc6-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7acc6-262">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7acc6-262">Requirements</span></span>



| <span data-ttu-id="7acc6-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="7acc6-263">Requirement</span></span> | <span data-ttu-id="7acc6-264">Valore</span><span class="sxs-lookup"><span data-stu-id="7acc6-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7acc6-265">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7acc6-265">Minimum supported client</span></span><br/> | <span data-ttu-id="7acc6-266">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7acc6-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7acc6-267">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7acc6-267">Minimum supported server</span></span><br/> | <span data-ttu-id="7acc6-268">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7acc6-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7acc6-269">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7acc6-269">Namespace</span></span><br/>                | <span data-ttu-id="7acc6-270">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7acc6-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7acc6-271">MOF</span><span class="sxs-lookup"><span data-stu-id="7acc6-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7acc6-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7acc6-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7acc6-273">DLL</span><span class="sxs-lookup"><span data-stu-id="7acc6-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7acc6-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7acc6-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7acc6-275">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7acc6-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acc6-276">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7acc6-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="7acc6-277">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7acc6-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="7acc6-278">**\_HeartbeatComponentSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="7acc6-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

