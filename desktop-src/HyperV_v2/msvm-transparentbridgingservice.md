---
description: Funge da segnaposto per il servizio all'interno dell'opzione che apprende gli indirizzi MAC e funge da Bridge tra le \_ classi MSVM VirtualEthernetSwitch e MSVM \_ DynamicForwardingEntry.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Classe Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966937"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="08b5b-103">\_Classe MSVM TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="08b5b-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="08b5b-104">Funge da segnaposto per il servizio all'interno dell'opzione che apprende gli indirizzi MAC e funge da Bridge tra le classi [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) e [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) .</span><span class="sxs-lookup"><span data-stu-id="08b5b-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="08b5b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="08b5b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b5b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08b5b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="08b5b-107">Members</span><span class="sxs-lookup"><span data-stu-id="08b5b-107">Members</span></span>

<span data-ttu-id="08b5b-108">La **classe \_ TransparentBridgingService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="08b5b-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="08b5b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="08b5b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="08b5b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08b5b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08b5b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="08b5b-111">Methods</span></span>

<span data-ttu-id="08b5b-112">La **classe \_ TransparentBridgingService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="08b5b-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="08b5b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="08b5b-113">Method</span></span>                                                                           | <span data-ttu-id="08b5b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08b5b-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="08b5b-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="08b5b-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="08b5b-116">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="08b5b-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="08b5b-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="08b5b-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="08b5b-118">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="08b5b-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="08b5b-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="08b5b-120">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="08b5b-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08b5b-121">Properties</span></span>

<span data-ttu-id="08b5b-122">La **classe \_ TransparentBridgingService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="08b5b-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08b5b-123">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="08b5b-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08b5b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-126">Periodo di timeout, in secondi, per l'invecchiamento degli indirizzi MAC appresi in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="08b5b-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="08b5b-127">Questa proprietà viene ereditata da [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="08b5b-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-128">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="08b5b-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-131">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="08b5b-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="08b5b-132">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-133">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="08b5b-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-136">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08b5b-136">A short description of the object.</span></span> <span data-ttu-id="08b5b-137">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre "Virtual Switch Transparent bridging Service".</span><span class="sxs-lookup"><span data-stu-id="08b5b-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-138">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="08b5b-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-141">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="08b5b-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="08b5b-142">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08b5b-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08b5b-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="08b5b-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="08b5b-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="08b5b-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="08b5b-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="08b5b-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="08b5b-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08b5b-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08b5b-151">)</span><span class="sxs-lookup"><span data-stu-id="08b5b-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b5b-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08b5b-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-155">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08b5b-155">A short description of the object.</span></span> <span data-ttu-id="08b5b-156">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="08b5b-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-160">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="08b5b-160">A description of the object.</span></span> <span data-ttu-id="08b5b-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Virtual Switch Transparent bridging Service".</span><span class="sxs-lookup"><span data-stu-id="08b5b-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="08b5b-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-165">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="08b5b-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="08b5b-166">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08b5b-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08b5b-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="08b5b-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="08b5b-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="08b5b-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="08b5b-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="08b5b-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="08b5b-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="08b5b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08b5b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08b5b-176">)</span><span class="sxs-lookup"><span data-stu-id="08b5b-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b5b-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="08b5b-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-180">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08b5b-180">A display name for the object.</span></span> <span data-ttu-id="08b5b-181">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="08b5b-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="08b5b-182">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-183">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="08b5b-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-186">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="08b5b-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="08b5b-187">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="08b5b-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-189">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-191">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="08b5b-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="08b5b-192">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-193">**FID**</span><span class="sxs-lookup"><span data-stu-id="08b5b-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-194">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08b5b-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-196">Identificatore del database di filtro usato dalle opzioni che supportano la VLAN e che hanno più di un database di filtraggio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="08b5b-197">Questa proprietà viene ereditata da [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="08b5b-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="08b5b-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-201">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="08b5b-201">The current health of the element.</span></span> <span data-ttu-id="08b5b-202">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="08b5b-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="08b5b-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08b5b-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-205">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08b5b-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-207">Specifica l'ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08b5b-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="08b5b-208">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="08b5b-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="08b5b-209">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08b5b-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-213">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="08b5b-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-214">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="08b5b-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="08b5b-215">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-216">**Parole chiave**</span><span class="sxs-lookup"><span data-stu-id="08b5b-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-217">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="08b5b-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-219">Non usare.</span><span class="sxs-lookup"><span data-stu-id="08b5b-219">Do not use.</span></span> <span data-ttu-id="08b5b-220">Matrice di stringhe in formato libero che fornisce parole descrittive e frasi che possono essere utilizzate nelle query.</span><span class="sxs-lookup"><span data-stu-id="08b5b-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="08b5b-221">Questa proprietà non è implementata perché non è standardizzata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="08b5b-222">Se questa proprietà fosse un costrutto di query necessario, sarebbe necessaria una maggiore parte della gerarchia di ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="08b5b-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="08b5b-223">Questa proprietà viene ereditata da [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-224">**Nome**</span><span class="sxs-lookup"><span data-stu-id="08b5b-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-227">Nome che identifica in modo univoco il servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="08b5b-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="08b5b-228">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="08b5b-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-230">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-232">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="08b5b-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="08b5b-233">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08b5b-234">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08b5b-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="08b5b-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="08b5b-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="08b5b-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="08b5b-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="08b5b-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="08b5b-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="08b5b-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="08b5b-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="08b5b-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="08b5b-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="08b5b-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="08b5b-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="08b5b-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="08b5b-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="08b5b-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="08b5b-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="08b5b-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="08b5b-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08b5b-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08b5b-254">)</span><span class="sxs-lookup"><span data-stu-id="08b5b-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b5b-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="08b5b-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-256">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-258">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="08b5b-258">The current status of the element.</span></span> <span data-ttu-id="08b5b-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="08b5b-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-263">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="08b5b-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="08b5b-264">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-265">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="08b5b-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-266">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-268">Tipo di protocollo da trasmettere quando il valore di **ProtocolType** è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="08b5b-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="08b5b-269">Questa proprietà viene ereditata da [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="08b5b-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="08b5b-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-273">Stringa che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="08b5b-274">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-275">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="08b5b-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-278">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="08b5b-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="08b5b-279">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-280">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="08b5b-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-281">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-283">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="08b5b-283">Provides high level status information.</span></span> <span data-ttu-id="08b5b-284">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="08b5b-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="08b5b-285">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08b5b-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08b5b-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="08b5b-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="08b5b-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="08b5b-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="08b5b-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="08b5b-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08b5b-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08b5b-293">)</span><span class="sxs-lookup"><span data-stu-id="08b5b-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08b5b-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="08b5b-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-295">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-297">Tipo di protocollo da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="08b5b-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="08b5b-298">Questa proprietà viene ereditata da [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="08b5b-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="08b5b-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-300">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-302">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="08b5b-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="08b5b-303">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="08b5b-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-307">Non usare.</span><span class="sxs-lookup"><span data-stu-id="08b5b-307">Do not use.</span></span> <span data-ttu-id="08b5b-308">URL che fornisce il protocollo, il percorso di rete e altre informazioni specifiche del servizio necessarie per accedere al servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="08b5b-309">Usare invece la classe **ServiceAccessURI** , che posiziona correttamente la semantica dell'accesso al servizio e chiarisce il formato delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="08b5b-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="08b5b-310">Questa proprietà viene ereditata da [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-311">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="08b5b-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-312">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="08b5b-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-314">Indica se il servizio è stato avviato (**true**) o arrestato (**false**).</span><span class="sxs-lookup"><span data-stu-id="08b5b-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="08b5b-315">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-316">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="08b5b-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-319">Indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo e così via oppure viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="08b5b-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="08b5b-320">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-321">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="08b5b-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-322">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="08b5b-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-324">Non usare.</span><span class="sxs-lookup"><span data-stu-id="08b5b-324">Do not use.</span></span> <span data-ttu-id="08b5b-325">Matrice di stringhe in formato libero che specifica le precondizioni specifiche che devono essere soddisfatte per il corretto avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="08b5b-326">Questa proprietà non è utile perché non è standardizzata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="08b5b-327">Se questa proprietà fosse un costrutto necessario, sarebbe necessaria una maggiore parte della gerarchia di ereditarietà (sul servizio).</span><span class="sxs-lookup"><span data-stu-id="08b5b-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="08b5b-328">Questa proprietà viene ereditata da [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="08b5b-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-330">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="08b5b-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-332">Non usare.</span><span class="sxs-lookup"><span data-stu-id="08b5b-332">Do not use.</span></span> <span data-ttu-id="08b5b-333">Matrice di stringhe in formato libero che specifica i parametri specifici che devono essere forniti al metodo **StartService** per il corretto avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="08b5b-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="08b5b-334">Se questo metodo è stato perfezionato, i relativi parametri comunicheranno in modo più formale queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="08b5b-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="08b5b-335">Questa proprietà viene ereditata da [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="08b5b-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-339">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08b5b-339">The current status of the object.</span></span> <span data-ttu-id="08b5b-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="08b5b-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-342">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="08b5b-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-344">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="08b5b-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="08b5b-345">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08b5b-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08b5b-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-349">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="08b5b-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="08b5b-350">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="08b5b-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08b5b-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-354">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="08b5b-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="08b5b-355">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="08b5b-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="08b5b-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-357">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08b5b-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-359">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="08b5b-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="08b5b-360">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="08b5b-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08b5b-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="08b5b-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08b5b-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08b5b-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08b5b-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08b5b-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08b5b-364">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="08b5b-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="08b5b-365">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08b5b-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08b5b-366">Commenti</span><span class="sxs-lookup"><span data-stu-id="08b5b-366">Remarks</span></span>

<span data-ttu-id="08b5b-367">L'accesso alla **classe \_ TransparentBridgingService di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="08b5b-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="08b5b-368">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="08b5b-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="08b5b-369">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08b5b-369">Requirements</span></span>



| <span data-ttu-id="08b5b-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b5b-370">Requirement</span></span> | <span data-ttu-id="08b5b-371">Valore</span><span class="sxs-lookup"><span data-stu-id="08b5b-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b5b-372">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08b5b-372">Minimum supported client</span></span><br/> | <span data-ttu-id="08b5b-373">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="08b5b-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08b5b-374">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08b5b-374">Minimum supported server</span></span><br/> | <span data-ttu-id="08b5b-375">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="08b5b-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08b5b-376">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08b5b-376">Namespace</span></span><br/>                | <span data-ttu-id="08b5b-377">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="08b5b-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08b5b-378">MOF</span><span class="sxs-lookup"><span data-stu-id="08b5b-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08b5b-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08b5b-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08b5b-380">DLL</span><span class="sxs-lookup"><span data-stu-id="08b5b-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b5b-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08b5b-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08b5b-382">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08b5b-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b5b-383">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="08b5b-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="08b5b-384">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="08b5b-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

