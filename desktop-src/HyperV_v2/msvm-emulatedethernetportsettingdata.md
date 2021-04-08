---
description: Rappresenta lo stato configurato di una scheda Ethernet emulata.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Classe Msvm_EmulatedEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880522"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="1e01d-103">\_Classe MSVM EmulatedEthernetPortSettingData</span><span class="sxs-lookup"><span data-stu-id="1e01d-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="1e01d-104">Rappresenta lo stato configurato di una scheda Ethernet emulata.</span><span class="sxs-lookup"><span data-stu-id="1e01d-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="1e01d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1e01d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e01d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e01d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="1e01d-107">Members</span><span class="sxs-lookup"><span data-stu-id="1e01d-107">Members</span></span>

<span data-ttu-id="1e01d-108">La **classe \_ EmulatedEthernetPortSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1e01d-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1e01d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e01d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e01d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e01d-110">Properties</span></span>

<span data-ttu-id="1e01d-111">La **classe \_ EmulatedEthernetPortSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e01d-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e01d-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="1e01d-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e01d-115">The address of the resource.</span></span> <span data-ttu-id="1e01d-116">Ad esempio, l'indirizzo MAC di una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1e01d-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="1e01d-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="1e01d-118">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1e01d-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="1e01d-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-122">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="1e01d-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="1e01d-123">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="1e01d-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="1e01d-124">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="1e01d-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-128">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="1e01d-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="1e01d-129">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su "Ports".</span><span class="sxs-lookup"><span data-stu-id="1e01d-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="1e01d-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e01d-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-133">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e01d-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="1e01d-134">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="1e01d-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e01d-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-138">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e01d-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="1e01d-139">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-140">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1e01d-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-143">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e01d-143">A short description of the object.</span></span> <span data-ttu-id="1e01d-144">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="1e01d-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-145">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="1e01d-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e01d-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-148">Indica se la scheda Ethernet viene monitorata da un cluster.</span><span class="sxs-lookup"><span data-stu-id="1e01d-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="1e01d-149">Per impostazione predefinita, questa proprietà è true se non è configurata.</span><span class="sxs-lookup"><span data-stu-id="1e01d-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="1e01d-150">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1e01d-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="1e01d-151">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="1e01d-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-152">**Connection**</span><span class="sxs-lookup"><span data-stu-id="1e01d-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-153">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1e01d-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-155">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e01d-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="1e01d-156">Ad esempio, una rete denominata o una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-156">For example, a named network or switch port.</span></span> <span data-ttu-id="1e01d-157">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="1e01d-158">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1e01d-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="1e01d-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e01d-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-162">Descrive la visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="1e01d-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="1e01d-163">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 3 (virtualizzata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-164">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1e01d-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-167">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1e01d-167">A description of the object.</span></span> <span data-ttu-id="1e01d-168">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Settings for the Microsoft Emulated Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="1e01d-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-169">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="1e01d-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-170">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e01d-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-172">Modalità di configurazione desiderata per l'endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="1e01d-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="1e01d-173">Questa proprietà viene utilizzata per impostare il valore della proprietà **OperationalEndpointMode** iniziale nell'istanza della classe [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) associata alla porta Ethernet di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="1e01d-174">Per i valori possibili, vedere la proprietà **OperationalEndpointMode** della classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="1e01d-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="1e01d-175">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1e01d-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-179">Nome visualizzato configurabile dall'utente per il dispositivo a cui è associata questa istanza di RASD.</span><span class="sxs-lookup"><span data-stu-id="1e01d-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="1e01d-180">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è impostata su "Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="1e01d-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="1e01d-181">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="1e01d-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="1e01d-182">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1e01d-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="1e01d-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-184">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1e01d-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-186">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e01d-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-190">All'interno dell'ambito dello spazio dei nomi di creazione di istanze, **InstanceID** indica in modo opaco e univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1e01d-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1e01d-191">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*VMID* \\ *VDID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="1e01d-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-192">**Limite**</span><span class="sxs-lookup"><span data-stu-id="1e01d-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-193">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e01d-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-195">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="1e01d-196">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="1e01d-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-197">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="1e01d-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e01d-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-200">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="1e01d-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="1e01d-201">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-202">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="1e01d-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-205">Stringa che descrive il tipo di modello di endpoint VLAN supportato da questo endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="1e01d-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="1e01d-206">Questa proprietà viene utilizzata solo quando la proprietà **DesiredVLANEndpointMode** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="1e01d-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="1e01d-207">Questa proprietà deve essere impostata su **null** se la proprietà **DesiredVLANEndpointMode** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="1e01d-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="1e01d-208">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="1e01d-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-209">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="1e01d-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-212">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e ResourceType è impostato su 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="1e01d-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="1e01d-213">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="1e01d-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-214">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1e01d-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-217">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e01d-217">The parent of the resource.</span></span> <span data-ttu-id="1e01d-218">Ad esempio, un controller per l'allocazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1e01d-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="1e01d-219">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-220">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="1e01d-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-223">Il pool da cui la risorsa è attualmente allocata o il pool da cui verrà allocata la risorsa quando si verifica l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="1e01d-224">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-225">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="1e01d-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-226">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e01d-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-228">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="1e01d-229">Nei sistemi che supportano l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione per impedire che venga accettata un'allocazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="1e01d-230">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="1e01d-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1e01d-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-234">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e01d-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="1e01d-235">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e01d-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="1e01d-236">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su "Microsoft Emulated Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="1e01d-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1e01d-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e01d-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-240">Tipo di risorsa a cui si applica questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="1e01d-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="1e01d-241">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 10 (scheda Ethernet).</span><span class="sxs-lookup"><span data-stu-id="1e01d-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-242">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="1e01d-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-243">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e01d-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-245">Indica se utilizzare un indirizzo MAC statico.</span><span class="sxs-lookup"><span data-stu-id="1e01d-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="1e01d-246">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1e01d-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="1e01d-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-248">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e01d-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-250">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="1e01d-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="1e01d-251">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="1e01d-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-252">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="1e01d-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1e01d-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-255">Specifica l'unità di misura per l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1e01d-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="1e01d-256">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1e01d-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="1e01d-257">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="1e01d-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="1e01d-258">**Weight**</span><span class="sxs-lookup"><span data-stu-id="1e01d-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e01d-259">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e01d-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e01d-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e01d-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e01d-261">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="1e01d-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="1e01d-262">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="1e01d-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e01d-263">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e01d-263">Remarks</span></span>

<span data-ttu-id="1e01d-264">L'accesso alla **classe \_ EmulatedEthernetPortSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="1e01d-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1e01d-265">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1e01d-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="1e01d-266">Esempio</span><span class="sxs-lookup"><span data-stu-id="1e01d-266">Examples</span></span>

<span data-ttu-id="1e01d-267">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1e01d-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e01d-268">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e01d-268">Requirements</span></span>



| <span data-ttu-id="1e01d-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e01d-269">Requirement</span></span> | <span data-ttu-id="1e01d-270">Valore</span><span class="sxs-lookup"><span data-stu-id="1e01d-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e01d-271">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e01d-271">Minimum supported client</span></span><br/> | <span data-ttu-id="1e01d-272">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1e01d-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e01d-273">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e01d-273">Minimum supported server</span></span><br/> | <span data-ttu-id="1e01d-274">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1e01d-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e01d-275">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e01d-275">Namespace</span></span><br/>                | <span data-ttu-id="1e01d-276">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1e01d-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1e01d-277">MOF</span><span class="sxs-lookup"><span data-stu-id="1e01d-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e01d-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e01d-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e01d-279">DLL</span><span class="sxs-lookup"><span data-stu-id="1e01d-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e01d-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e01d-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e01d-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e01d-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e01d-282">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1e01d-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="1e01d-283">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1e01d-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

