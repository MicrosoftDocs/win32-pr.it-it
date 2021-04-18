---
description: Gestisce tutte le connessioni terminali remote a un determinato host.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308737"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="23f27-103">\_Classe MSVM TerminalService</span><span class="sxs-lookup"><span data-stu-id="23f27-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="23f27-104">Gestisce tutte le connessioni terminali remote a un determinato host.</span><span class="sxs-lookup"><span data-stu-id="23f27-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="23f27-105">Per avviare tutte le connessioni terminali, il servizio utilizza una porta configurabile.</span><span class="sxs-lookup"><span data-stu-id="23f27-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="23f27-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23f27-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f27-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23f27-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
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
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="23f27-108">Members</span><span class="sxs-lookup"><span data-stu-id="23f27-108">Members</span></span>

<span data-ttu-id="23f27-109">La **classe \_ TerminalService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23f27-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="23f27-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="23f27-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="23f27-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23f27-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23f27-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="23f27-112">Methods</span></span>

<span data-ttu-id="23f27-113">La **classe \_ TerminalService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="23f27-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="23f27-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="23f27-114">Method</span></span>                                                                                        | <span data-ttu-id="23f27-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23f27-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23f27-116">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="23f27-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="23f27-117">Recupera l'elenco DACL corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23f27-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="23f27-118">**GrantInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="23f27-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="23f27-119">Concede l'accesso alla sessione interattiva della macchina virtuale all'elenco specificato di trustee.</span><span class="sxs-lookup"><span data-stu-id="23f27-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="23f27-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="23f27-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="23f27-121">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="23f27-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="23f27-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="23f27-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="23f27-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="23f27-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="23f27-124">**RevokeInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="23f27-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="23f27-125">Revoca l'accesso alla sessione interattiva della macchina virtuale dall'elenco specificato di trustee.</span><span class="sxs-lookup"><span data-stu-id="23f27-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="23f27-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="23f27-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="23f27-127">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="23f27-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="23f27-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="23f27-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="23f27-129">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="23f27-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="23f27-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23f27-130">Properties</span></span>

<span data-ttu-id="23f27-131">La **classe \_ TerminalService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23f27-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23f27-132">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="23f27-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-133">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23f27-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-135">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="23f27-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="23f27-136">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-137">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="23f27-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-140">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23f27-140">A short description of the object.</span></span> <span data-ttu-id="23f27-141">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-142">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="23f27-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-145">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="23f27-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="23f27-146">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="23f27-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23f27-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23f27-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23f27-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="23f27-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="23f27-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="23f27-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="23f27-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="23f27-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23f27-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23f27-155">)</span><span class="sxs-lookup"><span data-stu-id="23f27-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23f27-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23f27-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-159">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="23f27-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="23f27-160">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-161">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="23f27-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-164">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="23f27-164">A description of the object.</span></span> <span data-ttu-id="23f27-165">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="23f27-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-169">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="23f27-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="23f27-170">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="23f27-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23f27-171">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23f27-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="23f27-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="23f27-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="23f27-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="23f27-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="23f27-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="23f27-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="23f27-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23f27-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23f27-180">)</span><span class="sxs-lookup"><span data-stu-id="23f27-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23f27-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23f27-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-184">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23f27-184">A display name for the object.</span></span> <span data-ttu-id="23f27-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="23f27-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-189">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="23f27-190">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="23f27-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-194">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="23f27-195">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="23f27-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="23f27-196">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="23f27-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-200">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-200">The current health of the element.</span></span> <span data-ttu-id="23f27-201">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="23f27-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="23f27-202">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="23f27-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="23f27-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="23f27-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-205">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23f27-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-207">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23f27-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="23f27-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23f27-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23f27-212">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="23f27-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23f27-213">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="23f27-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23f27-214">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="23f27-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23f27-215">**Nome**</span><span class="sxs-lookup"><span data-stu-id="23f27-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-218">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="23f27-218">The label by which the object is known.</span></span> <span data-ttu-id="23f27-219">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-220">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="23f27-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-223">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="23f27-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="23f27-224">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="23f27-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23f27-225">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23f27-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23f27-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="23f27-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="23f27-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="23f27-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="23f27-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="23f27-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="23f27-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="23f27-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="23f27-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="23f27-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="23f27-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="23f27-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="23f27-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="23f27-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="23f27-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="23f27-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="23f27-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="23f27-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23f27-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23f27-245">)</span><span class="sxs-lookup"><span data-stu-id="23f27-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23f27-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="23f27-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-247">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23f27-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-249">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23f27-249">The current statuses of the object.</span></span> <span data-ttu-id="23f27-250">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-251">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="23f27-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-254">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="23f27-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="23f27-255">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="23f27-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="23f27-256">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="23f27-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-260">Valore che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="23f27-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="23f27-261">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-262">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="23f27-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-265">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="23f27-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="23f27-266">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="23f27-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="23f27-267">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-268">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="23f27-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-269">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-271">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="23f27-271">Provides high level status information.</span></span> <span data-ttu-id="23f27-272">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="23f27-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="23f27-273">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="23f27-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23f27-274">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="23f27-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23f27-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="23f27-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="23f27-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="23f27-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="23f27-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="23f27-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="23f27-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="23f27-281">)</span><span class="sxs-lookup"><span data-stu-id="23f27-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23f27-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="23f27-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-285">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="23f27-286">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="23f27-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="23f27-287">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="23f27-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="23f27-288">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="23f27-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="23f27-289">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="23f27-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="23f27-290">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="23f27-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="23f27-291">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="23f27-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-292">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23f27-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-294">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="23f27-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="23f27-295">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-296">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="23f27-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-299">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="23f27-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="23f27-300">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-301">**Status**</span><span class="sxs-lookup"><span data-stu-id="23f27-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-304">Stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-304">The status of the element.</span></span> <span data-ttu-id="23f27-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-306">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="23f27-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-307">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="23f27-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23f27-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-309">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="23f27-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="23f27-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="23f27-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-311">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="23f27-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-314">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="23f27-314">The scoping system's creation class name.</span></span> <span data-ttu-id="23f27-315">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="23f27-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23f27-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-319">Nome del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="23f27-319">The name of the hosting computer system.</span></span> <span data-ttu-id="23f27-320">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="23f27-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-321">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="23f27-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-322">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23f27-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-324">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="23f27-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="23f27-325">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23f27-326">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="23f27-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f27-327">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23f27-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23f27-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23f27-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23f27-329">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="23f27-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="23f27-330">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23f27-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23f27-331">Commenti</span><span class="sxs-lookup"><span data-stu-id="23f27-331">Remarks</span></span>

<span data-ttu-id="23f27-332">L'accesso alla **classe \_ TerminalService di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="23f27-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23f27-333">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="23f27-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="23f27-334">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23f27-334">Requirements</span></span>



| <span data-ttu-id="23f27-335">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f27-335">Requirement</span></span> | <span data-ttu-id="23f27-336">Valore</span><span class="sxs-lookup"><span data-stu-id="23f27-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f27-337">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23f27-337">Minimum supported client</span></span><br/> | <span data-ttu-id="23f27-338">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="23f27-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23f27-339">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23f27-339">Minimum supported server</span></span><br/> | <span data-ttu-id="23f27-340">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="23f27-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23f27-341">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23f27-341">Namespace</span></span><br/>                | <span data-ttu-id="23f27-342">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="23f27-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23f27-343">MOF</span><span class="sxs-lookup"><span data-stu-id="23f27-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23f27-344"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23f27-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23f27-345">DLL</span><span class="sxs-lookup"><span data-stu-id="23f27-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f27-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23f27-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23f27-347">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23f27-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f27-348">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="23f27-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

