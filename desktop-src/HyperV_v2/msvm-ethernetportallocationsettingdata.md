---
description: Rappresenta una richiesta di allocazione per una porta di commutazione statica o dinamica oppure rappresenta la configurazione attiva di una porta di commutazione statica o dinamica attualmente allocata.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Classe Msvm_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312914"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="64bce-103">\_Classe MSVM EthernetPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="64bce-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="64bce-104">Rappresenta una richiesta di allocazione per una porta di commutazione statica o dinamica oppure rappresenta la configurazione attiva di una porta di commutazione statica o dinamica attualmente allocata.</span><span class="sxs-lookup"><span data-stu-id="64bce-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="64bce-105">Una richiesta di allocazione per una porta di commutazione dinamica è nota anche come richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="64bce-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="64bce-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="64bce-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64bce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64bce-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="64bce-108">Members</span><span class="sxs-lookup"><span data-stu-id="64bce-108">Members</span></span>

<span data-ttu-id="64bce-109">La **classe \_ EthernetPortAllocationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="64bce-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="64bce-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64bce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64bce-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64bce-111">Properties</span></span>

<span data-ttu-id="64bce-112">La **classe \_ EthernetPortAllocationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="64bce-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64bce-113">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="64bce-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-116">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-116">The address of the resource.</span></span> <span data-ttu-id="64bce-117">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="64bce-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-121">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="64bce-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="64bce-122">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="64bce-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="64bce-123">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="64bce-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-127">Unità di allocazione utilizzata dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="64bce-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="64bce-128">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="64bce-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="64bce-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-132">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="64bce-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="64bce-133">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="64bce-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="64bce-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-137">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="64bce-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="64bce-138">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="64bce-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64bce-142">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="64bce-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="64bce-143">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="64bce-143">A short description of the object.</span></span> <span data-ttu-id="64bce-144">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Settings".</span><span class="sxs-lookup"><span data-stu-id="64bce-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="64bce-145">**CompartmentGuid**</span><span class="sxs-lookup"><span data-stu-id="64bce-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64bce-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64bce-148">Questa proprietà specifica il raggruppamento di rete di destinazione per la porta.</span><span class="sxs-lookup"><span data-stu-id="64bce-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="64bce-149">È supportato solo per gli adapter interni.</span><span class="sxs-lookup"><span data-stu-id="64bce-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="64bce-150">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="64bce-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="64bce-151">**Connection**</span><span class="sxs-lookup"><span data-stu-id="64bce-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-152">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="64bce-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="64bce-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-154">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-154">The device to which this resource is connected.</span></span> <span data-ttu-id="64bce-155">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-156">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="64bce-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64bce-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-159">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="64bce-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="64bce-160">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 3 (virtualizzata).</span><span class="sxs-lookup"><span data-stu-id="64bce-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-161">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="64bce-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-164">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="64bce-164">A description of the object.</span></span> <span data-ttu-id="64bce-165">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Settings".</span><span class="sxs-lookup"><span data-stu-id="64bce-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="64bce-166">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="64bce-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64bce-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-169">Modalità di configurazione desiderata per l'endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="64bce-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="64bce-170">Questa proprietà viene utilizzata per impostare il valore della proprietà **OperationalEndpointMode** iniziale nell'istanza della classe [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) associata alla porta Ethernet di destinazione.</span><span class="sxs-lookup"><span data-stu-id="64bce-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="64bce-171">Per i valori possibili, vedere la proprietà **OperationalEndpointMode** della classe **MSVM \_ VLANEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="64bce-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="64bce-172">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="64bce-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="64bce-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-176">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="64bce-176">A display name for the object.</span></span> <span data-ttu-id="64bce-177">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64bce-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="64bce-178">Se si modifica questa proprietà, il nome dell'elemento del derivato del dispositivo logico associato verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="64bce-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="64bce-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64bce-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-182">Indica se la richiesta di allocazione è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="64bce-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="64bce-183">Quando una richiesta di allocazione è contrassegnata come disabilitata (3), l'allocazione non viene elaborata.</span><span class="sxs-lookup"><span data-stu-id="64bce-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="64bce-184">Il valore di **EnabledState** per una configurazione attiva è sempre contrassegnato come abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="64bce-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="64bce-185">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="64bce-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="64bce-186">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="64bce-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="64bce-187">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="64bce-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-188">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="64bce-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="64bce-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-190">È possibile assegnare una sola risorsa host a ogni dispositivo nel Commuter virtuale, pertanto è possibile impostare solo il primo elemento di questa matrice.</span><span class="sxs-lookup"><span data-stu-id="64bce-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="64bce-191">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="64bce-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="64bce-192">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="64bce-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64bce-196">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="64bce-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="64bce-197">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="64bce-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="64bce-198">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="64bce-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="64bce-199">**LastKnownSwitchName**</span><span class="sxs-lookup"><span data-stu-id="64bce-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-202">Ultimo nome descrittivo del Commuter con cui questa porta aveva un'affinità rigida, se presente.</span><span class="sxs-lookup"><span data-stu-id="64bce-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="64bce-203">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="64bce-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="64bce-204">**Limite**</span><span class="sxs-lookup"><span data-stu-id="64bce-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-205">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="64bce-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-207">Quantità massima di risorse host corrispondenti che possono essere utilizzate dal Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="64bce-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="64bce-208">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-209">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="64bce-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-210">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64bce-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-212">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="64bce-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="64bce-213">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-214">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="64bce-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-217">Stringa che descrive il tipo di modello di endpoint VLAN supportato da questo endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="64bce-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="64bce-218">Questa proprietà viene utilizzata solo quando la proprietà **DesiredVLANEndpointMode** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="64bce-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="64bce-219">Questa proprietà deve essere impostata su **null** se la proprietà **DesiredVLANEndpointMode** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="64bce-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="64bce-220">Questa proprietà viene ereditata da **CIM \_ EthernetPortAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="64bce-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-221">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="64bce-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-224">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="64bce-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="64bce-225">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="64bce-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-226">**Parent**</span><span class="sxs-lookup"><span data-stu-id="64bce-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-229">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-229">The parent of the resource.</span></span> <span data-ttu-id="64bce-230">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-231">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="64bce-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-234">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="64bce-235">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-236">**RequiredFeatureHints**</span><span class="sxs-lookup"><span data-stu-id="64bce-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-237">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="64bce-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="64bce-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-239">Elenco di nomi visualizzati che corrispondono a ogni voce nella matrice **RequiredFeatures** .</span><span class="sxs-lookup"><span data-stu-id="64bce-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-240">**RequiredFeatures**</span><span class="sxs-lookup"><span data-stu-id="64bce-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-241">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="64bce-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="64bce-242">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64bce-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64bce-243">Elenco di identificatori di funzionalità che rappresentano tutte le funzionalità necessarie per una porta.</span><span class="sxs-lookup"><span data-stu-id="64bce-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-244">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="64bce-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-245">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="64bce-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-247">Quantità di risorse riservate per l'utilizzo da parte del Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="64bce-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="64bce-248">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="64bce-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-252">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="64bce-253">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="64bce-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="64bce-254">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="64bce-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-256">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64bce-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-258">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="64bce-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="64bce-259">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)ed è sempre impostata su 33 (Ethernet Connection).</span><span class="sxs-lookup"><span data-stu-id="64bce-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-260">**TestReplicaPoolID**</span><span class="sxs-lookup"><span data-stu-id="64bce-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64bce-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64bce-263">Specifica il pool di risorse di rete da cui verrà allocata una connessione al sistema di replica di test quando viene creato.</span><span class="sxs-lookup"><span data-stu-id="64bce-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-264">**TestReplicaSwitchName**</span><span class="sxs-lookup"><span data-stu-id="64bce-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-265">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-266">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64bce-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64bce-267">Specifica il nome visualizzato dello switch di rete virtuale a cui verrà allocata una connessione per il sistema di replica di test quando viene creato.</span><span class="sxs-lookup"><span data-stu-id="64bce-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="64bce-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="64bce-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="64bce-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-271">Numero totale di porte nel Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="64bce-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="64bce-272">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="64bce-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64bce-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-276">Specifica l'unità di misura per la proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="64bce-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="64bce-277">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di programmazione, come definito nell'allegato C. 1 di DSP0004 V 2.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="64bce-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="64bce-278">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="64bce-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="64bce-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bce-280">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64bce-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64bce-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64bce-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bce-282">Intero che definisce il peso per ogni Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="64bce-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="64bce-283">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="64bce-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="64bce-284">Intervallo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="64bce-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64bce-285">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64bce-285">Requirements</span></span>



| <span data-ttu-id="64bce-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="64bce-286">Requirement</span></span> | <span data-ttu-id="64bce-287">Valore</span><span class="sxs-lookup"><span data-stu-id="64bce-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64bce-288">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64bce-288">Minimum supported client</span></span><br/> | <span data-ttu-id="64bce-289">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64bce-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64bce-290">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64bce-290">Minimum supported server</span></span><br/> | <span data-ttu-id="64bce-291">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64bce-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64bce-292">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64bce-292">Namespace</span></span><br/>                | <span data-ttu-id="64bce-293">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="64bce-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64bce-294">MOF</span><span class="sxs-lookup"><span data-stu-id="64bce-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64bce-295"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64bce-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64bce-296">DLL</span><span class="sxs-lookup"><span data-stu-id="64bce-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64bce-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64bce-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

