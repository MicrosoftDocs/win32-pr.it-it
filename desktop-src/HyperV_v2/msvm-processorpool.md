---
description: Aggrega le risorse del processore che possono essere allocate a una macchina virtuale.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312902"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="1a330-103">\_Classe MSVM ProcessorPool</span><span class="sxs-lookup"><span data-stu-id="1a330-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="1a330-104">Aggrega le risorse del processore che possono essere allocate a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1a330-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="1a330-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1a330-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a330-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a330-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="1a330-107">Members</span><span class="sxs-lookup"><span data-stu-id="1a330-107">Members</span></span>

<span data-ttu-id="1a330-108">La **classe \_ ProcessorPool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1a330-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="1a330-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="1a330-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1a330-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1a330-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1a330-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="1a330-111">Methods</span></span>

<span data-ttu-id="1a330-112">La **classe \_ ProcessorPool di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1a330-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="1a330-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="1a330-113">Method</span></span>                                                                          | <span data-ttu-id="1a330-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a330-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="1a330-115">**CalculatePossibleReserve**</span><span class="sxs-lookup"><span data-stu-id="1a330-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="1a330-116">Utilizzato per trovare la riserva effettiva del processore.</span><span class="sxs-lookup"><span data-stu-id="1a330-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1a330-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1a330-117">Properties</span></span>

<span data-ttu-id="1a330-118">La **classe \_ ProcessorPool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1a330-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a330-119">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="1a330-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-122">Unità di allocazione utilizzate dal pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a330-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="1a330-123">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su "megabyte".</span><span class="sxs-lookup"><span data-stu-id="1a330-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="1a330-124">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="1a330-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a330-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-127">Quantità massima (in unità di **AllocationUnits**) di prenotazioni attive che il pool di risorse può supportare.</span><span class="sxs-lookup"><span data-stu-id="1a330-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="1a330-128">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-129">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1a330-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-132">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a330-132">A short description of the object.</span></span> <span data-ttu-id="1a330-133">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-134">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1a330-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-137">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="1a330-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1a330-138">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="1a330-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1a330-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1a330-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1a330-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="1a330-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="1a330-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="1a330-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="1a330-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1a330-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1a330-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1a330-147">)</span><span class="sxs-lookup"><span data-stu-id="1a330-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a330-148">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="1a330-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-151">Specifica le unità per le proprietà **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="1a330-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="1a330-152">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-153">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="1a330-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-154">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a330-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-156">Specifica la quantità di risorse che il pool di risorse presenta attualmente ai consumer.</span><span class="sxs-lookup"><span data-stu-id="1a330-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="1a330-157">Questa proprietà è diversa dalla proprietà **riservata** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **riservata** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a330-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="1a330-158">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-159">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1a330-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-162">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1a330-162">A description of the object.</span></span> <span data-ttu-id="1a330-163">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1a330-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-167">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="1a330-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1a330-168">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="1a330-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1a330-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1a330-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="1a330-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="1a330-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="1a330-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="1a330-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="1a330-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="1a330-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1a330-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1a330-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1a330-178">)</span><span class="sxs-lookup"><span data-stu-id="1a330-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a330-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1a330-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-182">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a330-182">A display name for the object.</span></span> <span data-ttu-id="1a330-183">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1a330-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-187">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1a330-187">The current health of the element.</span></span> <span data-ttu-id="1a330-188">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1a330-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-190">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a330-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-192">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a330-192">The date and time when the object was installed.</span></span> <span data-ttu-id="1a330-193">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="1a330-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="1a330-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1a330-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a330-198">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="1a330-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1a330-199">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1a330-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1a330-200">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-201">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="1a330-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-202">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a330-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-204">Specifica la quantità massima di risorse utilizzabili che il pool di risorse può presentare ai consumer.</span><span class="sxs-lookup"><span data-stu-id="1a330-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="1a330-205">Questa proprietà è diversa dalla proprietà **Capacity** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **Capacity** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a330-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="1a330-206">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-207">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1a330-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-210">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="1a330-210">The label by which the object is known.</span></span> <span data-ttu-id="1a330-211">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-212">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1a330-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-215">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="1a330-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1a330-216">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="1a330-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1a330-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1a330-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1a330-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="1a330-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="1a330-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="1a330-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="1a330-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="1a330-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="1a330-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="1a330-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="1a330-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="1a330-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="1a330-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="1a330-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="1a330-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="1a330-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="1a330-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="1a330-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="1a330-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1a330-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1a330-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1a330-237">)</span><span class="sxs-lookup"><span data-stu-id="1a330-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a330-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1a330-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-239">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1a330-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-241">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a330-241">The current statuses of the object.</span></span> <span data-ttu-id="1a330-242">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-243">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="1a330-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-246">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e **ResourceType** è impostato su 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="1a330-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="1a330-247">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="1a330-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1a330-248">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="1a330-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-251">A questo valore viene fatto riferimento dalle istanze [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che sono state allocate da questo pool.</span><span class="sxs-lookup"><span data-stu-id="1a330-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="1a330-252">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è sempre impostata su "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="1a330-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="1a330-253">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1a330-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-254">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-256">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="1a330-256">Provides high level status information.</span></span> <span data-ttu-id="1a330-257">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="1a330-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1a330-258">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="1a330-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1a330-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1a330-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1a330-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1a330-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="1a330-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="1a330-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1a330-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1a330-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1a330-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1a330-266">)</span><span class="sxs-lookup"><span data-stu-id="1a330-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a330-267">**Originale**</span><span class="sxs-lookup"><span data-stu-id="1a330-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-268">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1a330-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-270">**True** se il pool di risorse è la base da cui vengono disegnate e restituite risorse nell'attività di gestione delle risorse. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1a330-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="1a330-271">Essendo primordiale significa che questo pool di risorse non può essere creato o eliminato dagli utenti di questo modello.</span><span class="sxs-lookup"><span data-stu-id="1a330-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="1a330-272">Tuttavia, altre azioni, modellate o meno, possono influire sulle caratteristiche o sulle dimensioni dei pool di risorse primordiali.</span><span class="sxs-lookup"><span data-stu-id="1a330-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="1a330-273">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1a330-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-275">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a330-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-277">Le prenotazioni correnti, in unità di **AllocationUnits**, vengono distribuite in tutte le allocazioni attive da questo pool.</span><span class="sxs-lookup"><span data-stu-id="1a330-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="1a330-278">In una configurazione gerarchica, rappresenta la somma di tutte le prenotazioni correnti del pool di risorse discendenti.</span><span class="sxs-lookup"><span data-stu-id="1a330-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="1a330-279">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1a330-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-283">Stringa che descrive un sottotipo specifico dell'implementazione per il pool.</span><span class="sxs-lookup"><span data-stu-id="1a330-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="1a330-284">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a330-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="1a330-285">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a330-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1a330-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1a330-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-287">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a330-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-289">Il tipo di risorsa che questo pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="1a330-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="1a330-290">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="1a330-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="1a330-291">**Status**</span><span class="sxs-lookup"><span data-stu-id="1a330-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-292">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a330-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a330-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-294">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a330-294">The current status of the object.</span></span> <span data-ttu-id="1a330-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="1a330-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a330-296">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1a330-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a330-297">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1a330-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a330-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a330-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a330-299">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1a330-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1a330-300">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1a330-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a330-301">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a330-301">Remarks</span></span>

<span data-ttu-id="1a330-302">L'accesso alla **classe \_ ProcessorPool di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="1a330-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1a330-303">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1a330-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a330-304">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a330-304">Requirements</span></span>



| <span data-ttu-id="1a330-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a330-305">Requirement</span></span> | <span data-ttu-id="1a330-306">Valore</span><span class="sxs-lookup"><span data-stu-id="1a330-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a330-307">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a330-307">Minimum supported client</span></span><br/> | <span data-ttu-id="1a330-308">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1a330-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1a330-309">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a330-309">Minimum supported server</span></span><br/> | <span data-ttu-id="1a330-310">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1a330-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a330-311">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1a330-311">Namespace</span></span><br/>                | <span data-ttu-id="1a330-312">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a330-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1a330-313">MOF</span><span class="sxs-lookup"><span data-stu-id="1a330-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a330-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a330-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a330-315">DLL</span><span class="sxs-lookup"><span data-stu-id="1a330-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a330-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a330-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a330-317">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a330-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a330-318">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="1a330-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="1a330-319">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a330-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a330-320">Classi del processore</span><span class="sxs-lookup"><span data-stu-id="1a330-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

