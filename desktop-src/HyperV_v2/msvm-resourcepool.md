---
description: Descrive un tipo di risorsa virtuale disponibile per l'utilizzo nelle macchine virtuali.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Classe Msvm_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232078"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="b880d-103">\_Classe MSVM ResourcePool</span><span class="sxs-lookup"><span data-stu-id="b880d-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="b880d-104">Descrive un tipo di risorsa virtuale disponibile per l'utilizzo nelle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b880d-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="b880d-105">Il pool di risorse aggrega le risorse fisiche e viene usato per allocare le risorse alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b880d-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="b880d-106">In Hyper-V tutti i pool di risorse sono primordiali ed è presente esattamente un pool per ogni tipo specifico di risorsa che può essere allocato a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b880d-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="b880d-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b880d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b880d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b880d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="b880d-109">Members</span><span class="sxs-lookup"><span data-stu-id="b880d-109">Members</span></span>

<span data-ttu-id="b880d-110">La **classe \_ ResourcePool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b880d-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="b880d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b880d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b880d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b880d-112">Properties</span></span>

<span data-ttu-id="b880d-113">La **classe \_ ResourcePool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b880d-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b880d-114">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="b880d-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-117">Unità di allocazione utilizzate dal pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="b880d-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="b880d-118">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su "megabyte".</span><span class="sxs-lookup"><span data-stu-id="b880d-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="b880d-119">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="b880d-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-120">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b880d-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-122">Quantità massima (in unità di **AllocationUnits**) di prenotazioni attive che il pool di risorse può supportare.</span><span class="sxs-lookup"><span data-stu-id="b880d-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="b880d-123">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b880d-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b880d-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-127">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b880d-127">A short description of the object.</span></span> <span data-ttu-id="b880d-128">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b880d-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-132">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="b880d-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b880d-133">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b880d-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b880d-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b880d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b880d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b880d-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="b880d-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="b880d-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="b880d-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b880d-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b880d-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b880d-142">)</span><span class="sxs-lookup"><span data-stu-id="b880d-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b880d-143">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="b880d-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-146">Specifica le unità per le proprietà **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="b880d-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="b880d-147">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="b880d-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-148">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b880d-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-150">Specifica la quantità di risorse che il pool di risorse presenta attualmente ai consumer.</span><span class="sxs-lookup"><span data-stu-id="b880d-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="b880d-151">Questa proprietà è diversa dalla proprietà **riservata** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **riservata** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b880d-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b880d-152">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b880d-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-155">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b880d-155">A description of the object.</span></span> <span data-ttu-id="b880d-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b880d-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-160">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="b880d-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b880d-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b880d-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b880d-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b880d-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="b880d-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="b880d-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="b880d-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b880d-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="b880d-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="b880d-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b880d-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b880d-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b880d-171">)</span><span class="sxs-lookup"><span data-stu-id="b880d-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b880d-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b880d-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-175">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b880d-175">A display name for the object.</span></span> <span data-ttu-id="b880d-176">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b880d-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-180">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b880d-180">The current health of the element.</span></span> <span data-ttu-id="b880d-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b880d-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-183">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b880d-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-185">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b880d-185">The date and time when the object was installed.</span></span> <span data-ttu-id="b880d-186">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="b880d-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="b880d-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b880d-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b880d-191">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b880d-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b880d-192">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b880d-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b880d-193">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-194">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="b880d-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-195">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b880d-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-197">Specifica la quantità massima di risorse utilizzabili che il pool di risorse può presentare ai consumer.</span><span class="sxs-lookup"><span data-stu-id="b880d-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="b880d-198">Questa proprietà è diversa dalla proprietà **Capacity** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **Capacity** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b880d-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b880d-199">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b880d-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-202">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b880d-202">The label by which the object is known.</span></span> <span data-ttu-id="b880d-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-204">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b880d-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-205">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-207">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b880d-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b880d-208">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b880d-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b880d-209">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b880d-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b880d-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b880d-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="b880d-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="b880d-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="b880d-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="b880d-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="b880d-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="b880d-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="b880d-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="b880d-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="b880d-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="b880d-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="b880d-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="b880d-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="b880d-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="b880d-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="b880d-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b880d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b880d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b880d-229">)</span><span class="sxs-lookup"><span data-stu-id="b880d-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b880d-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b880d-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-231">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b880d-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b880d-233">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="b880d-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="b880d-234">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b880d-234">The current statuses of the object.</span></span> <span data-ttu-id="b880d-235">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="b880d-236">Se non sono state rilevate condizioni correlate a QoS, lo stato primario (OperationalStatus \[ 0 \] ) viene impostato su OK (2).</span><span class="sxs-lookup"><span data-stu-id="b880d-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="b880d-237">In caso contrario, lo stato primario viene impostato su ridotto (3) e uno o più valori di stato secondari sono compilati nella matrice, a partire dall'indice 1, che segnala condizioni più specifiche, in base a questa tabella.</span><span class="sxs-lookup"><span data-stu-id="b880d-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="b880d-238">Valore</span><span class="sxs-lookup"><span data-stu-id="b880d-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="b880d-239">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b880d-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b880d-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Velocità effettiva insufficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="b880d-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="b880d-241">Almeno uno dei dischi virtuali allocati dal pool sta attualmente segnalando uno stato di velocità effettiva insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b880d-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="b880d-242">Il provider WMI Hyper-V genera un evento [**MSVM \_ StorageAlert**](msvm-storagealert.md) ogni volta che viene modificato il OperationalStatus della classe **MSVM \_ ResourcePool** .</span><span class="sxs-lookup"><span data-stu-id="b880d-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b880d-243">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="b880d-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b880d-244">**Danneggiato** (3)</span><span class="sxs-lookup"><span data-stu-id="b880d-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="b880d-245">**Errore irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="b880d-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b880d-246">**Nessun contatto** (12)</span><span class="sxs-lookup"><span data-stu-id="b880d-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="b880d-247">**Comunicazione persa** (13)</span><span class="sxs-lookup"><span data-stu-id="b880d-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="b880d-248">**Mancata corrispondenza del protocollo** (32775)</span><span class="sxs-lookup"><span data-stu-id="b880d-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="b880d-249">**Velocità effettiva insufficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="b880d-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b880d-250">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="b880d-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-253">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorpool.md) è impostato su 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="b880d-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="b880d-254">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b880d-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b880d-255">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="b880d-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-258">A questo valore viene fatto riferimento dalle istanze [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che sono state allocate da questo pool.</span><span class="sxs-lookup"><span data-stu-id="b880d-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="b880d-259">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è sempre impostata su "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="b880d-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="b880d-260">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b880d-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-261">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-263">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="b880d-263">Provides high level status information.</span></span> <span data-ttu-id="b880d-264">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b880d-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b880d-265">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b880d-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b880d-266">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b880d-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b880d-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="b880d-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="b880d-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="b880d-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b880d-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b880d-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b880d-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b880d-273">)</span><span class="sxs-lookup"><span data-stu-id="b880d-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b880d-274">**Originale**</span><span class="sxs-lookup"><span data-stu-id="b880d-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-275">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b880d-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-277">**True** se il pool di risorse è la base da cui vengono disegnate e restituite risorse nell'attività di gestione delle risorse. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b880d-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="b880d-278">Essendo primordiale significa che questo pool di risorse non può essere creato o eliminato dagli utenti di questo modello.</span><span class="sxs-lookup"><span data-stu-id="b880d-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="b880d-279">Tuttavia, altre azioni, modellate o meno, possono influire sulle caratteristiche o sulle dimensioni dei pool di risorse primordiali.</span><span class="sxs-lookup"><span data-stu-id="b880d-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="b880d-280">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b880d-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b880d-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-282">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b880d-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-284">Le prenotazioni correnti, in unità di **AllocationUnits**, vengono distribuite in tutte le allocazioni attive da questo pool.</span><span class="sxs-lookup"><span data-stu-id="b880d-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="b880d-285">In una configurazione gerarchica, rappresenta la somma di tutte le prenotazioni correnti del pool di risorse discendenti.</span><span class="sxs-lookup"><span data-stu-id="b880d-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="b880d-286">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b880d-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="b880d-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-290">Stringa che descrive un sottotipo specifico dell'implementazione per il pool.</span><span class="sxs-lookup"><span data-stu-id="b880d-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="b880d-291">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b880d-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="b880d-292">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b880d-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b880d-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b880d-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-294">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b880d-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-296">Il tipo di risorsa che questo pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="b880d-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="b880d-297">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="b880d-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="b880d-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="b880d-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b880d-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b880d-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-301">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b880d-301">The current status of the object.</span></span> <span data-ttu-id="b880d-302">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b880d-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b880d-303">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b880d-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b880d-304">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b880d-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b880d-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b880d-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b880d-306">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b880d-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b880d-307">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b880d-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b880d-308">Commenti</span><span class="sxs-lookup"><span data-stu-id="b880d-308">Remarks</span></span>

<span data-ttu-id="b880d-309">L'accesso alla **classe \_ ResourcePool di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b880d-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b880d-310">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b880d-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b880d-311">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b880d-311">Requirements</span></span>



| <span data-ttu-id="b880d-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="b880d-312">Requirement</span></span> | <span data-ttu-id="b880d-313">Valore</span><span class="sxs-lookup"><span data-stu-id="b880d-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b880d-314">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b880d-314">Minimum supported client</span></span><br/> | <span data-ttu-id="b880d-315">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b880d-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b880d-316">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b880d-316">Minimum supported server</span></span><br/> | <span data-ttu-id="b880d-317">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b880d-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b880d-318">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b880d-318">Namespace</span></span><br/>                | <span data-ttu-id="b880d-319">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b880d-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b880d-320">MOF</span><span class="sxs-lookup"><span data-stu-id="b880d-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b880d-321"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b880d-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b880d-322">DLL</span><span class="sxs-lookup"><span data-stu-id="b880d-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b880d-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b880d-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b880d-324">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b880d-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b880d-325">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="b880d-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="b880d-326">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b880d-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b880d-327">**MSVM \_ ResourcePool (V1)**</span><span class="sxs-lookup"><span data-stu-id="b880d-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="b880d-328">**\_StorageAlert MSVM**</span><span class="sxs-lookup"><span data-stu-id="b880d-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="b880d-329">Classi di gestione delle risorse</span><span class="sxs-lookup"><span data-stu-id="b880d-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

