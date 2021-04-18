---
description: Rappresenta lo stato configurato di una scheda Ethernet sintetica.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Classe Msvm_SyntheticEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306036"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="b5432-103">\_Classe MSVM SyntheticEthernetPortSettingData</span><span class="sxs-lookup"><span data-stu-id="b5432-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="b5432-104">Rappresenta lo stato configurato di una scheda Ethernet sintetica.</span><span class="sxs-lookup"><span data-stu-id="b5432-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="b5432-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b5432-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5432-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5432-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="b5432-107">Members</span><span class="sxs-lookup"><span data-stu-id="b5432-107">Members</span></span>

<span data-ttu-id="b5432-108">La **classe \_ SyntheticEthernetPortSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b5432-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b5432-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5432-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5432-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5432-110">Properties</span></span>

<span data-ttu-id="b5432-111">La **classe \_ SyntheticEthernetPortSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5432-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5432-112">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="b5432-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-115">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5432-115">The address of the resource.</span></span> <span data-ttu-id="b5432-116">Ad esempio, l'indirizzo MAC di una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b5432-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="b5432-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="b5432-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-121">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="b5432-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b5432-122">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="b5432-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b5432-123">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="b5432-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-127">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="b5432-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b5432-128">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-129">**AllowPacketDirect**</span><span class="sxs-lookup"><span data-stu-id="b5432-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b5432-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5432-132">Indica se la proiezione PacketDirect è abilitata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5432-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="b5432-133">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b5432-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b5432-134">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="b5432-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-137">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b5432-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="b5432-138">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-139">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="b5432-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-142">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b5432-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="b5432-143">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-144">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b5432-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-147">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5432-147">A short description of the object.</span></span> <span data-ttu-id="b5432-148">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5432-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-149">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="b5432-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-152">Indica se la scheda Ethernet viene monitorata da un cluster.</span><span class="sxs-lookup"><span data-stu-id="b5432-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="b5432-153">Per impostazione predefinita, questa proprietà è true se non è configurata.</span><span class="sxs-lookup"><span data-stu-id="b5432-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="b5432-154">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b5432-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="b5432-155">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="b5432-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-156">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b5432-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-157">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b5432-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5432-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-159">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5432-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="b5432-160">Ad esempio, una rete denominata o una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-160">For example, a named network or switch port.</span></span> <span data-ttu-id="b5432-161">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-162">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="b5432-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5432-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-165">La visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="b5432-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="b5432-166">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 3 (virtualizzata).</span><span class="sxs-lookup"><span data-stu-id="b5432-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-167">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b5432-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-170">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b5432-170">A description of the object.</span></span> <span data-ttu-id="b5432-171">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5432-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-172">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="b5432-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5432-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-175">Modalità di configurazione desiderata per l'endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="b5432-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="b5432-176">Questa proprietà viene utilizzata per impostare il valore della proprietà **OperationalEndpointMode** iniziale nell'istanza della classe [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) associata alla porta Ethernet di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="b5432-177">Per i valori possibili, vedere la proprietà **OperationalEndpointMode** della classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="b5432-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="b5432-178">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="b5432-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-179">**DeviceNamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="b5432-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-182">Indica se questa scheda Ethernet supporta la denominazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b5432-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="b5432-183">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b5432-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="b5432-184">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b5432-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b5432-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b5432-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-188">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5432-188">A short description of the object.</span></span> <span data-ttu-id="b5432-189">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5432-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-190">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="b5432-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-191">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b5432-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5432-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-193">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b5432-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5432-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5432-197">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b5432-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b5432-198">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b5432-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b5432-199">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b5432-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-200">**Limite**</span><span class="sxs-lookup"><span data-stu-id="b5432-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-201">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5432-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-203">Limite superiore o quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="b5432-204">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-205">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="b5432-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-206">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5432-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-208">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="b5432-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="b5432-209">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-210">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="b5432-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-213">Stringa che descrive il tipo di modello di endpoint VLAN supportato da questo endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="b5432-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="b5432-214">Questa proprietà viene utilizzata solo quando la proprietà **DesiredVLANEndpointMode** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b5432-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="b5432-215">Questa proprietà deve essere impostata su **null** se la proprietà **DesiredVLANEndpointMode** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="b5432-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="b5432-216">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="b5432-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="b5432-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-220">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su "other" (0).</span><span class="sxs-lookup"><span data-stu-id="b5432-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="b5432-221">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b5432-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b5432-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-225">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5432-225">The parent of the resource.</span></span> <span data-ttu-id="b5432-226">Ad esempio, un controller per l'allocazione corrente.</span><span class="sxs-lookup"><span data-stu-id="b5432-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="b5432-227">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="b5432-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-231">Il pool da cui la risorsa è attualmente allocata o il pool da cui verrà allocata la risorsa quando si verifica l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="b5432-232">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-233">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="b5432-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-234">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5432-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-236">Quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="b5432-237">Nei sistemi che supportano l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione per impedire che venga accettata un'allocazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="b5432-238">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b5432-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-242">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5432-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="b5432-243">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5432-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="b5432-244">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b5432-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-246">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5432-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-248">Tipo di risorsa a cui si applica questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="b5432-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="b5432-249">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 10 (scheda Ethernet).</span><span class="sxs-lookup"><span data-stu-id="b5432-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-250">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="b5432-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-251">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b5432-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-253">Specifica se l'indirizzo MAC è statico.</span><span class="sxs-lookup"><span data-stu-id="b5432-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="b5432-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b5432-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-255">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5432-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-257">Quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="b5432-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="b5432-258">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-259">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="b5432-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b5432-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-262">Specifica l'unità di misura per la proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="b5432-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="b5432-263">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b5432-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="b5432-264">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-265">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="b5432-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-266">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b5432-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b5432-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5432-268">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="b5432-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="b5432-269">Matrice di stringhe di identificatori di questa risorsa presentata al sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5432-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="b5432-270">Gli indici e i valori per indice vengono definiti in base alle singole risorse, ovvero per ogni valore della proprietà **ResourceType** enumerata.</span><span class="sxs-lookup"><span data-stu-id="b5432-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="b5432-271">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b5432-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5432-272">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5432-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5432-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5432-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5432-274">Priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5432-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="b5432-275">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b5432-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5432-276">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5432-276">Remarks</span></span>

<span data-ttu-id="b5432-277">L'accesso alla **classe \_ SyntheticEthernetPortSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b5432-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b5432-278">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b5432-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b5432-279">Esempio</span><span class="sxs-lookup"><span data-stu-id="b5432-279">Examples</span></span>

<span data-ttu-id="b5432-280">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b5432-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5432-281">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5432-281">Requirements</span></span>



| <span data-ttu-id="b5432-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5432-282">Requirement</span></span> | <span data-ttu-id="b5432-283">Valore</span><span class="sxs-lookup"><span data-stu-id="b5432-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5432-284">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5432-284">Minimum supported client</span></span><br/> | <span data-ttu-id="b5432-285">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b5432-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5432-286">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5432-286">Minimum supported server</span></span><br/> | <span data-ttu-id="b5432-287">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5432-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5432-288">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5432-288">Namespace</span></span><br/>                | <span data-ttu-id="b5432-289">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5432-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5432-290">MOF</span><span class="sxs-lookup"><span data-stu-id="b5432-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5432-291"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5432-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5432-292">DLL</span><span class="sxs-lookup"><span data-stu-id="b5432-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5432-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5432-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5432-294">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5432-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5432-295">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b5432-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="b5432-296">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b5432-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

