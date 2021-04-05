---
description: Fornisce la gestione attiva dei pool di risorse.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885134"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="84f8c-103">\_Classe MSVM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="84f8c-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="84f8c-104">Fornisce la gestione attiva dei pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="84f8c-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="84f8c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="84f8c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f8c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84f8c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="84f8c-107">Members</span><span class="sxs-lookup"><span data-stu-id="84f8c-107">Members</span></span>

<span data-ttu-id="84f8c-108">La **classe \_ ResourcePoolConfigurationService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84f8c-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="84f8c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="84f8c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="84f8c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84f8c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84f8c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="84f8c-111">Methods</span></span>

<span data-ttu-id="84f8c-112">La **classe \_ ResourcePoolConfigurationService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="84f8c-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="84f8c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="84f8c-113">Method</span></span>                                                                                   | <span data-ttu-id="84f8c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84f8c-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84f8c-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="84f8c-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="84f8c-116">Crea un pool di risorse figlio.</span><span class="sxs-lookup"><span data-stu-id="84f8c-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="84f8c-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="84f8c-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="84f8c-118">Elimina un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="84f8c-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="84f8c-119">**ModifyPoolResources**</span><span class="sxs-lookup"><span data-stu-id="84f8c-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="84f8c-120">Modifica le impostazioni delle risorse del pool padre per le risorse assegnate a un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="84f8c-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="84f8c-121">**ModifyPoolSettings**</span><span class="sxs-lookup"><span data-stu-id="84f8c-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="84f8c-122">Modifica le impostazioni di un pool figlio che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="84f8c-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="84f8c-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f8c-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="84f8c-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="84f8c-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="84f8c-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="84f8c-125">**StartService**</span></span>                                                                         | <span data-ttu-id="84f8c-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="84f8c-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="84f8c-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="84f8c-127">**StopService**</span></span>                                                                          | <span data-ttu-id="84f8c-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="84f8c-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="84f8c-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84f8c-129">Properties</span></span>

<span data-ttu-id="84f8c-130">La **classe \_ ResourcePoolConfigurationService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84f8c-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f8c-131">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="84f8c-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-132">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-134">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="84f8c-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="84f8c-135">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-136">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="84f8c-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-139">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f8c-139">A short description of the object.</span></span> <span data-ttu-id="84f8c-140">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-141">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="84f8c-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-144">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="84f8c-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="84f8c-145">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f8c-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f8c-146">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f8c-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f8c-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="84f8c-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="84f8c-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="84f8c-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="84f8c-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84f8c-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="84f8c-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f8c-154">)</span><span class="sxs-lookup"><span data-stu-id="84f8c-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f8c-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84f8c-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-158">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f8c-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-159">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="84f8c-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="84f8c-160">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="84f8c-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-161">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="84f8c-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-164">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="84f8c-164">A description of the object.</span></span> <span data-ttu-id="84f8c-165">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="84f8c-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-169">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="84f8c-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="84f8c-170">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f8c-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f8c-171">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f8c-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="84f8c-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="84f8c-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="84f8c-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="84f8c-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="84f8c-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="84f8c-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84f8c-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="84f8c-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f8c-180">)</span><span class="sxs-lookup"><span data-stu-id="84f8c-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f8c-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84f8c-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-184">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f8c-184">A display name for the object.</span></span> <span data-ttu-id="84f8c-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="84f8c-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-189">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="84f8c-190">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="84f8c-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="84f8c-191">Valore</span><span class="sxs-lookup"><span data-stu-id="84f8c-191">Value</span></span>                                                                        | <span data-ttu-id="84f8c-192">Significato</span><span class="sxs-lookup"><span data-stu-id="84f8c-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="84f8c-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84f8c-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="84f8c-194">Abilitato</span><span class="sxs-lookup"><span data-stu-id="84f8c-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f8c-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="84f8c-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-198">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="84f8c-199">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="84f8c-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="84f8c-200">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="84f8c-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="84f8c-201">Valore</span><span class="sxs-lookup"><span data-stu-id="84f8c-201">Value</span></span>                                                                        | <span data-ttu-id="84f8c-202">Significato</span><span class="sxs-lookup"><span data-stu-id="84f8c-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="84f8c-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84f8c-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="84f8c-204">Abilitato</span><span class="sxs-lookup"><span data-stu-id="84f8c-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f8c-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="84f8c-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-206">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-208">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-208">The current health of the element.</span></span> <span data-ttu-id="84f8c-209">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="84f8c-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="84f8c-210">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="84f8c-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="84f8c-211">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84f8c-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-213">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f8c-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-215">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84f8c-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="84f8c-216">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84f8c-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-220">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="84f8c-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-221">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="84f8c-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="84f8c-222">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-223">**Nome**</span><span class="sxs-lookup"><span data-stu-id="84f8c-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-226">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f8c-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-227">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="84f8c-227">The label by which the object is known.</span></span> <span data-ttu-id="84f8c-228">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="84f8c-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-230">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-232">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="84f8c-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="84f8c-233">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f8c-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f8c-234">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f8c-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f8c-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="84f8c-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="84f8c-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="84f8c-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="84f8c-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="84f8c-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="84f8c-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="84f8c-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="84f8c-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="84f8c-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="84f8c-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="84f8c-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="84f8c-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="84f8c-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="84f8c-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="84f8c-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="84f8c-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84f8c-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="84f8c-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f8c-254">)</span><span class="sxs-lookup"><span data-stu-id="84f8c-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f8c-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="84f8c-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-256">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-258">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84f8c-258">The current statuses of the object.</span></span> <span data-ttu-id="84f8c-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="84f8c-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-263">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="84f8c-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="84f8c-264">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="84f8c-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="84f8c-265">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="84f8c-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-269">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f8c-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-270">Tutte le informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="84f8c-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="84f8c-271">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-272">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="84f8c-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-275">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="84f8c-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-276">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="84f8c-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="84f8c-277">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="84f8c-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="84f8c-278">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-279">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="84f8c-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-280">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-282">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="84f8c-282">Provides high level status information.</span></span> <span data-ttu-id="84f8c-283">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="84f8c-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="84f8c-284">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="84f8c-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f8c-285">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f8c-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f8c-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="84f8c-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="84f8c-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="84f8c-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84f8c-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="84f8c-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f8c-292">)</span><span class="sxs-lookup"><span data-stu-id="84f8c-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f8c-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="84f8c-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-294">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-296">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="84f8c-297">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="84f8c-298">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="84f8c-299">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="84f8c-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="84f8c-300">In tal caso, viene utilizzato il valore 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="84f8c-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="84f8c-301">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="84f8c-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="84f8c-302">Valore</span><span class="sxs-lookup"><span data-stu-id="84f8c-302">Value</span></span>                                                                         | <span data-ttu-id="84f8c-303">Significato</span><span class="sxs-lookup"><span data-stu-id="84f8c-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="84f8c-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="84f8c-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="84f8c-305">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="84f8c-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f8c-306">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="84f8c-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-307">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84f8c-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-309">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84f8c-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="84f8c-310">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="84f8c-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-311">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="84f8c-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-314">Qualificatori: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="84f8c-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-315">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="84f8c-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="84f8c-316">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-317">**Status**</span><span class="sxs-lookup"><span data-stu-id="84f8c-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-320">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="84f8c-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-321">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="84f8c-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-322">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="84f8c-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-324">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="84f8c-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="84f8c-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="84f8c-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-326">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84f8c-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-329">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f8c-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-330">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="84f8c-330">The scoping system's creation class name.</span></span> <span data-ttu-id="84f8c-331">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="84f8c-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="84f8c-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84f8c-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-335">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="84f8c-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-336">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="84f8c-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="84f8c-337">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="84f8c-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-338">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f8c-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-339">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84f8c-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-341">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="84f8c-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="84f8c-342">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84f8c-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f8c-343">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="84f8c-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f8c-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84f8c-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f8c-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84f8c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f8c-346">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="84f8c-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="84f8c-347">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="84f8c-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84f8c-348">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84f8c-348">Requirements</span></span>



| <span data-ttu-id="84f8c-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f8c-349">Requirement</span></span> | <span data-ttu-id="84f8c-350">Valore</span><span class="sxs-lookup"><span data-stu-id="84f8c-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f8c-351">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f8c-351">Minimum supported client</span></span><br/> | <span data-ttu-id="84f8c-352">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="84f8c-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="84f8c-353">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f8c-353">Minimum supported server</span></span><br/> | <span data-ttu-id="84f8c-354">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="84f8c-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84f8c-355">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84f8c-355">Namespace</span></span><br/>                | <span data-ttu-id="84f8c-356">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84f8c-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84f8c-357">MOF</span><span class="sxs-lookup"><span data-stu-id="84f8c-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f8c-358"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f8c-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f8c-359">DLL</span><span class="sxs-lookup"><span data-stu-id="84f8c-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f8c-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f8c-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

