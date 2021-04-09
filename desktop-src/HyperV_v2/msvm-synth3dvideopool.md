---
description: Contiene informazioni sulle GPU (Graphics Processing Unit) sintetico 3D disponibili nel sistema host.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967151"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="32161-103">\_Classe MSVM Synth3dVideoPool</span><span class="sxs-lookup"><span data-stu-id="32161-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="32161-104">Contiene informazioni sulle GPU (Graphics Processing Unit) sintetico 3D disponibili nel sistema host.</span><span class="sxs-lookup"><span data-stu-id="32161-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="32161-105">Questa classe viene utilizzata solo con i sistemi host che supportano RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="32161-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="32161-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="32161-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32161-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32161-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="32161-108">Members</span><span class="sxs-lookup"><span data-stu-id="32161-108">Members</span></span>

<span data-ttu-id="32161-109">La **classe \_ Synth3dVideoPool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32161-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="32161-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="32161-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="32161-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32161-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="32161-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="32161-112">Methods</span></span>

<span data-ttu-id="32161-113">La **classe \_ Synth3dVideoPool di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="32161-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="32161-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="32161-114">Method</span></span>                                                                                             | <span data-ttu-id="32161-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32161-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32161-116">**CalculateVideoMemoryRequirements**</span><span class="sxs-lookup"><span data-stu-id="32161-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="32161-117">Calcola la quantità di memoria video necessaria per una macchina virtuale RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="32161-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="32161-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32161-118">Properties</span></span>

<span data-ttu-id="32161-119">La **classe \_ Synth3dVideoPool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="32161-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32161-120">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="32161-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-123">Unità di allocazione utilizzate dal pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="32161-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="32161-124">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-125">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="32161-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32161-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32161-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-128">Quantità massima (in unità di **AllocationUnits**) di prenotazioni attive che il pool di risorse può supportare.</span><span class="sxs-lookup"><span data-stu-id="32161-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="32161-129">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-130">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="32161-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-133">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="32161-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="32161-134">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="32161-134">A short description of the object.</span></span> <span data-ttu-id="32161-135">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="32161-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="32161-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-139">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="32161-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="32161-140">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="32161-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="32161-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="32161-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="32161-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32161-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="32161-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="32161-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="32161-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="32161-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="32161-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="32161-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="32161-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="32161-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="32161-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="32161-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="32161-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="32161-149">)</span><span class="sxs-lookup"><span data-stu-id="32161-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32161-150">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="32161-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-153">Specifica le unità per le proprietà **MaxConsumableResource** e **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="32161-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="32161-154">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-155">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="32161-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-156">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32161-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32161-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-158">Specifica la quantità di risorse che il pool di risorse presenta attualmente ai consumer.</span><span class="sxs-lookup"><span data-stu-id="32161-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="32161-159">Questa proprietà è diversa dalla proprietà **riservata** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **riservata** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="32161-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="32161-160">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-161">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="32161-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-164">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="32161-164">A description of the object.</span></span> <span data-ttu-id="32161-165">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="32161-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="32161-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-169">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="32161-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="32161-170">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="32161-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="32161-171">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="32161-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="32161-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32161-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="32161-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="32161-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="32161-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="32161-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="32161-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="32161-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="32161-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="32161-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="32161-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="32161-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="32161-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="32161-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="32161-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="32161-180">)</span><span class="sxs-lookup"><span data-stu-id="32161-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32161-181">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="32161-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-184">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="32161-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="32161-185">Specifica la versione più bassa di DirectX supportata dalle schede all'interno del pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="32161-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="32161-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="32161-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-189">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="32161-189">A display name for the object.</span></span> <span data-ttu-id="32161-190">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="32161-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="32161-191">Anche la proprietà [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) della classe **CIM \_ ManagedSystemElement** è definita come nome visualizzato, ma spesso è sottoclassata come chiave.</span><span class="sxs-lookup"><span data-stu-id="32161-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="32161-192">Non è ragionevole che la stessa proprietà possa fornire identità e un nome visualizzato, senza incoerenze.</span><span class="sxs-lookup"><span data-stu-id="32161-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="32161-193">Dove [**Name**](msvm-keyboard.md) esiste e non è una chiave, ad esempio per le istanze di LogicalDevice, le stesse informazioni possono essere presenti nelle proprietà **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="32161-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="32161-194">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="32161-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="32161-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-198">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="32161-198">The current health of the element.</span></span> <span data-ttu-id="32161-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="32161-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="32161-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="32161-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-201">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="32161-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="32161-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-203">Data e ora di creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32161-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="32161-204">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32161-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-208">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="32161-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="32161-209">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="32161-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="32161-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="32161-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="32161-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-212">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="32161-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32161-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-214">Specifica se il video 3D è supportato dal sistema host.</span><span class="sxs-lookup"><span data-stu-id="32161-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="32161-215">Contiene un valore diverso da zero se il video 3D è supportato oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="32161-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="32161-216">Per supportare video 3D, l'host RemoteFX deve disporre di funzionalità di trasferimento indirizzi di secondo livello (stecca) e avere almeno una GPU fisica che supporti RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="32161-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="32161-217">**IsGPUCapable**</span><span class="sxs-lookup"><span data-stu-id="32161-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-218">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="32161-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32161-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-220">Specifica se l'host dispone di GPU che supportano RemoteFX e se le versioni DirectX soddisfano il requisito minimo.</span><span class="sxs-lookup"><span data-stu-id="32161-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="32161-221">**IsSLATCapable**</span><span class="sxs-lookup"><span data-stu-id="32161-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-222">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="32161-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32161-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-224">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="32161-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="32161-225">Specifica se l'host dispone di una CPU in grado di supportare la conversione degli indirizzi di secondo livello.</span><span class="sxs-lookup"><span data-stu-id="32161-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="32161-226">Deprecato in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="32161-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="32161-227">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="32161-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-228">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32161-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32161-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-230">Specifica la quantità massima di risorse utilizzabili che il pool di risorse può presentare ai consumer.</span><span class="sxs-lookup"><span data-stu-id="32161-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="32161-231">Questa proprietà è diversa dalla proprietà **Capacity** in quanto descrive la visualizzazione dei consumer della risorsa, mentre la proprietà **Capacity** descrive la visualizzazione producer della risorsa.</span><span class="sxs-lookup"><span data-stu-id="32161-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="32161-232">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-233">**Nome**</span><span class="sxs-lookup"><span data-stu-id="32161-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-236">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="32161-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="32161-237">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="32161-237">The label by which the object is known.</span></span> <span data-ttu-id="32161-238">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="32161-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="32161-239">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="32161-240">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="32161-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-241">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-243">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="32161-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="32161-244">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="32161-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="32161-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="32161-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="32161-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32161-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="32161-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="32161-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="32161-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="32161-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="32161-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="32161-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="32161-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="32161-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="32161-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="32161-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="32161-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="32161-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="32161-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="32161-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="32161-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="32161-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="32161-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="32161-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="32161-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="32161-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="32161-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="32161-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="32161-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="32161-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="32161-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="32161-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="32161-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="32161-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="32161-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="32161-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="32161-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="32161-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="32161-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="32161-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="32161-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="32161-265">)</span><span class="sxs-lookup"><span data-stu-id="32161-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32161-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="32161-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-267">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="32161-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-269">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="32161-269">The current status of the element.</span></span> <span data-ttu-id="32161-270">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="32161-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="32161-271">Hyper-V userà sempre il primo elemento di questa matrice.</span><span class="sxs-lookup"><span data-stu-id="32161-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="32161-272">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="32161-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-275">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorpool.md) è impostato su 0 ("other").</span><span class="sxs-lookup"><span data-stu-id="32161-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="32161-276">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="32161-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="32161-277">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="32161-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-280">A questo valore viene fatto riferimento dalle istanze [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che sono state allocate da questo pool.</span><span class="sxs-lookup"><span data-stu-id="32161-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="32161-281">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è sempre impostata su "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="32161-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="32161-282">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="32161-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-285">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="32161-285">Provides high level status information.</span></span> <span data-ttu-id="32161-286">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="32161-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="32161-287">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="32161-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="32161-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="32161-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="32161-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="32161-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32161-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="32161-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="32161-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="32161-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="32161-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="32161-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="32161-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="32161-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="32161-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="32161-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="32161-295">)</span><span class="sxs-lookup"><span data-stu-id="32161-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32161-296">**Originale**</span><span class="sxs-lookup"><span data-stu-id="32161-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-297">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="32161-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32161-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-299">**True** se il pool di risorse è la base da cui vengono disegnate e restituite risorse nell'attività di gestione delle risorse. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="32161-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="32161-300">Essendo primordiale significa che questo pool di risorse non può essere creato o eliminato dagli utenti di questo modello.</span><span class="sxs-lookup"><span data-stu-id="32161-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="32161-301">Tuttavia, altre azioni, modellate o meno, possono influire sulle caratteristiche o sulle dimensioni dei pool di risorse primordiali.</span><span class="sxs-lookup"><span data-stu-id="32161-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="32161-302">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-303">**RequiredMinimumDirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="32161-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32161-306">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="32161-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="32161-307">Specifica la versione minima di DirectX richiesta dalle schede all'interno del pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="32161-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="32161-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="32161-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-309">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="32161-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="32161-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-311">Le prenotazioni correnti, in unità di **AllocationUnits**, vengono distribuite in tutte le allocazioni attive da questo pool.</span><span class="sxs-lookup"><span data-stu-id="32161-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="32161-312">In una configurazione gerarchica, rappresenta la somma di tutte le prenotazioni correnti del pool di risorse discendenti.</span><span class="sxs-lookup"><span data-stu-id="32161-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="32161-313">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="32161-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-317">Stringa che descrive un sottotipo specifico dell'implementazione per questo pool.</span><span class="sxs-lookup"><span data-stu-id="32161-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="32161-318">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="32161-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="32161-319">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32161-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32161-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="32161-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-321">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="32161-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="32161-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-323">Tipo di risorsa che questo pool di risorse può allocare.</span><span class="sxs-lookup"><span data-stu-id="32161-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="32161-324">Questa proprietà viene ereditata da [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))ed è sempre impostata su 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="32161-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="32161-325">**Status**</span><span class="sxs-lookup"><span data-stu-id="32161-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32161-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32161-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="32161-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="32161-329">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="32161-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32161-330">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="32161-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="32161-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32161-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32161-332">Stringhe che descrivono i vari valori della matrice [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="32161-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="32161-333">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="32161-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="32161-334">Hyper-V userà sempre il primo elemento di questa matrice.</span><span class="sxs-lookup"><span data-stu-id="32161-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32161-335">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32161-335">Requirements</span></span>



| <span data-ttu-id="32161-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="32161-336">Requirement</span></span> | <span data-ttu-id="32161-337">Valore</span><span class="sxs-lookup"><span data-stu-id="32161-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32161-338">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32161-338">Minimum supported client</span></span><br/> | <span data-ttu-id="32161-339">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="32161-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="32161-340">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32161-340">Minimum supported server</span></span><br/> | <span data-ttu-id="32161-341">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="32161-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32161-342">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32161-342">Namespace</span></span><br/>                | <span data-ttu-id="32161-343">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="32161-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="32161-344">MOF</span><span class="sxs-lookup"><span data-stu-id="32161-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32161-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32161-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32161-346">DLL</span><span class="sxs-lookup"><span data-stu-id="32161-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32161-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32161-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32161-348">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32161-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32161-349">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="32161-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

