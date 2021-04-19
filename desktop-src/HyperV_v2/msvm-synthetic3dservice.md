---
description: Viene descritto il servizio GPU 3D sintetico.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308906"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="b7f97-103">\_Classe MSVM Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="b7f97-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="b7f97-104">Viene descritto il servizio GPU 3D sintetico.</span><span class="sxs-lookup"><span data-stu-id="b7f97-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="b7f97-105">Questa classe non è disponibile per le macchine virtuali di seconda generazione.</span><span class="sxs-lookup"><span data-stu-id="b7f97-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="b7f97-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b7f97-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7f97-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="b7f97-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7f97-108">Members</span></span>

<span data-ttu-id="b7f97-109">La **classe \_ Synthetic3DService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7f97-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="b7f97-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7f97-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7f97-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7f97-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7f97-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7f97-112">Methods</span></span>

<span data-ttu-id="b7f97-113">La **classe \_ Synthetic3DService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b7f97-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="b7f97-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="b7f97-114">Method</span></span>                                                                                     | <span data-ttu-id="b7f97-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7f97-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="b7f97-116">**DisableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="b7f97-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="b7f97-117">Disabilita una GPU fisica per la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7f97-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="b7f97-118">**EnableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="b7f97-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="b7f97-119">Abilita una GPU fisica per la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7f97-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="b7f97-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="b7f97-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="b7f97-121">Modifica i dati dell'impostazione per il servizio sintetico 3D.</span><span class="sxs-lookup"><span data-stu-id="b7f97-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="b7f97-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b7f97-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="b7f97-123">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7f97-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="b7f97-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="b7f97-124">**StartService**</span></span>                                                                           | <span data-ttu-id="b7f97-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7f97-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="b7f97-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="b7f97-126">**StopService**</span></span>                                                                            | <span data-ttu-id="b7f97-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b7f97-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="b7f97-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7f97-128">Properties</span></span>

<span data-ttu-id="b7f97-129">La **classe \_ Synthetic3DService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b7f97-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7f97-130">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b7f97-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-131">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-133">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="b7f97-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b7f97-134">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-135">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b7f97-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-138">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7f97-138">A short description of the object.</span></span> <span data-ttu-id="b7f97-139">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b7f97-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-143">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="b7f97-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b7f97-144">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b7f97-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b7f97-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b7f97-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b7f97-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f97-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f97-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f97-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="b7f97-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b7f97-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b7f97-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b7f97-153">)</span><span class="sxs-lookup"><span data-stu-id="b7f97-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7f97-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b7f97-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-157">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b7f97-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b7f97-158">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-159">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b7f97-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-162">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b7f97-162">A description of the object.</span></span> <span data-ttu-id="b7f97-163">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b7f97-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-167">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="b7f97-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b7f97-168">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b7f97-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b7f97-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b7f97-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="b7f97-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f97-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f97-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f97-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="b7f97-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="b7f97-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b7f97-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b7f97-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b7f97-178">)</span><span class="sxs-lookup"><span data-stu-id="b7f97-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7f97-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b7f97-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-182">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7f97-182">A display name for the object.</span></span> <span data-ttu-id="b7f97-183">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-184">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b7f97-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-187">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b7f97-188">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b7f97-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-192">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b7f97-193">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="b7f97-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b7f97-194">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b7f97-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-198">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-198">The current health of the element.</span></span> <span data-ttu-id="b7f97-199">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b7f97-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b7f97-200">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="b7f97-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b7f97-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7f97-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-203">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f97-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-205">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7f97-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b7f97-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7f97-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-210">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b7f97-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-211">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b7f97-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b7f97-212">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b7f97-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-213">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b7f97-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-216">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b7f97-216">The label by which the object is known.</span></span> <span data-ttu-id="b7f97-217">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-218">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b7f97-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-221">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b7f97-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b7f97-222">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b7f97-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b7f97-223">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b7f97-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b7f97-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f97-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f97-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f97-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="b7f97-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="b7f97-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="b7f97-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="b7f97-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="b7f97-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="b7f97-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="b7f97-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="b7f97-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="b7f97-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="b7f97-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="b7f97-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="b7f97-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="b7f97-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b7f97-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b7f97-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b7f97-243">)</span><span class="sxs-lookup"><span data-stu-id="b7f97-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7f97-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b7f97-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-245">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-247">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7f97-247">The current statuses of the object.</span></span> <span data-ttu-id="b7f97-248">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-249">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b7f97-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-252">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b7f97-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b7f97-253">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="b7f97-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b7f97-254">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b7f97-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-258">Valore che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="b7f97-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="b7f97-259">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-260">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="b7f97-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-263">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="b7f97-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="b7f97-264">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="b7f97-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="b7f97-265">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b7f97-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-269">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="b7f97-269">Provides high level status information.</span></span> <span data-ttu-id="b7f97-270">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b7f97-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b7f97-271">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b7f97-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b7f97-272">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b7f97-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b7f97-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f97-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f97-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f97-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b7f97-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="b7f97-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b7f97-279">)</span><span class="sxs-lookup"><span data-stu-id="b7f97-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b7f97-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b7f97-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-281">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-283">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="b7f97-284">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="b7f97-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b7f97-285">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b7f97-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="b7f97-286">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="b7f97-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="b7f97-287">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b7f97-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="b7f97-288">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="b7f97-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-289">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="b7f97-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-290">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b7f97-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-292">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b7f97-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="b7f97-293">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-294">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="b7f97-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-295">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-297">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="b7f97-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="b7f97-298">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-299">**Status**</span><span class="sxs-lookup"><span data-stu-id="b7f97-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-302">Stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-302">The status of the element.</span></span> <span data-ttu-id="b7f97-303">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-304">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b7f97-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-305">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b7f97-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-307">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b7f97-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b7f97-308">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b7f97-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-309">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b7f97-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-312">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b7f97-312">The scoping system's creation class name.</span></span> <span data-ttu-id="b7f97-313">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b7f97-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b7f97-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-317">Nome del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="b7f97-317">The name of the hosting computer system.</span></span> <span data-ttu-id="b7f97-318">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="b7f97-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-319">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b7f97-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-320">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f97-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-322">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7f97-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b7f97-323">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7f97-324">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b7f97-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f97-325">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f97-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f97-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7f97-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f97-327">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b7f97-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b7f97-328">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7f97-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7f97-329">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7f97-329">Requirements</span></span>



| <span data-ttu-id="b7f97-330">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f97-330">Requirement</span></span> | <span data-ttu-id="b7f97-331">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f97-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f97-332">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f97-332">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f97-333">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b7f97-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b7f97-334">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f97-334">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f97-335">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b7f97-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7f97-336">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7f97-336">Namespace</span></span><br/>                | <span data-ttu-id="b7f97-337">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b7f97-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b7f97-338">MOF</span><span class="sxs-lookup"><span data-stu-id="b7f97-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7f97-339"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7f97-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7f97-340">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f97-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f97-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7f97-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

