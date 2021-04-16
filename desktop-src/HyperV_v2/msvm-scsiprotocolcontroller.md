---
description: Rappresenta un controller SCSI sintetico.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Classe Msvm_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530385"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="6fcf1-103">\_Classe MSVM SCSIProtocolController</span><span class="sxs-lookup"><span data-stu-id="6fcf1-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="6fcf1-104">Rappresenta un controller SCSI sintetico.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="6fcf1-105">Un controller SCSI sintetico può supportare fino a 256 unità.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="6fcf1-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fcf1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fcf1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_SCSIProtocolController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="6fcf1-108">Members</span><span class="sxs-lookup"><span data-stu-id="6fcf1-108">Members</span></span>

<span data-ttu-id="6fcf1-109">La **classe \_ SCSIProtocolController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6fcf1-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="6fcf1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6fcf1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6fcf1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fcf1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6fcf1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="6fcf1-112">Methods</span></span>

<span data-ttu-id="6fcf1-113">La **classe \_ SCSIProtocolController di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="6fcf1-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="6fcf1-114">Method</span></span>                                                                       | <span data-ttu-id="6fcf1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fcf1-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="6fcf1-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="6fcf1-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6fcf1-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="6fcf1-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6fcf1-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="6fcf1-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6fcf1-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="6fcf1-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="6fcf1-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="6fcf1-125">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="6fcf1-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="6fcf1-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6fcf1-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="6fcf1-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6fcf1-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="6fcf1-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6fcf1-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fcf1-132">Properties</span></span>

<span data-ttu-id="6fcf1-133">La **classe \_ SCSIProtocolController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fcf1-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-135">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-137">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="6fcf1-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6fcf1-139">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-139">Value</span></span>                                                                            | <span data-ttu-id="6fcf1-140">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6fcf1-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="6fcf1-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="6fcf1-143">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fcf1-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-144">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-147">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-147">The primary availability and status of the device.</span></span> <span data-ttu-id="6fcf1-148">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6fcf1-149">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-149">Value</span></span>                                                                        | <span data-ttu-id="6fcf1-150">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6fcf1-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="6fcf1-152">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fcf1-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-153">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-154">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-156">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="6fcf1-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="6fcf1-157">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-158">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-161">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-161">A short description of the object.</span></span> <span data-ttu-id="6fcf1-162">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-166">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6fcf1-167">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6fcf1-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6fcf1-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6fcf1-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6fcf1-176">)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6fcf1-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-180">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6fcf1-181">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-182">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-185">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="6fcf1-185">A description of the object.</span></span> <span data-ttu-id="6fcf1-186">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-190">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6fcf1-191">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6fcf1-192">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6fcf1-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6fcf1-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6fcf1-201">)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6fcf1-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-205">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="6fcf1-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-209">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-209">A display name for the object.</span></span> <span data-ttu-id="6fcf1-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-214">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6fcf1-215">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6fcf1-216">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-216">Value</span></span>                                                                        | <span data-ttu-id="6fcf1-217">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="6fcf1-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6fcf1-219">Abilitato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-223">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6fcf1-224">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6fcf1-225">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6fcf1-226">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-226">Value</span></span>                                                                        | <span data-ttu-id="6fcf1-227">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6fcf1-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="6fcf1-229">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fcf1-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-233">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="6fcf1-234">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-238">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="6fcf1-239">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-241">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-243">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-243">The current health of the element.</span></span> <span data-ttu-id="6fcf1-244">Questa operazione esprime l'integrità dell'elemento, ma non necessariamente quello dei sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6fcf1-245">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6fcf1-246">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-248">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-250">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="6fcf1-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="6fcf1-251">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-253">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-255">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6fcf1-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-260">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-261">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6fcf1-262">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-266">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="6fcf1-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-271">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-271">This property has been deprecated.</span></span> <span data-ttu-id="6fcf1-272">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-273">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-274">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-276">Numero massimo di unità che possono essere controllate o accessibili tramite questo controller di protocollo.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="6fcf1-277">Questa proprietà viene ereditata da [**CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-278">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-281">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-281">The label by which the object is known.</span></span> <span data-ttu-id="6fcf1-282">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-284">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-286">Identifica il modo in cui viene selezionato il nome del controller del protocollo SCSI.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="6fcf1-287">Questa proprietà viene ereditata da [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="6fcf1-288">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-288">Value</span></span>                                                                        | <span data-ttu-id="6fcf1-289">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="6fcf1-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6fcf1-291">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="6fcf1-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-292">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-293">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-295">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6fcf1-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6fcf1-296">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6fcf1-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6fcf1-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6fcf1-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6fcf1-317">)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6fcf1-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-319">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-321">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-321">The current status of the object.</span></span> <span data-ttu-id="6fcf1-322">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="6fcf1-323">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-323">Value</span></span>                                                                            | <span data-ttu-id="6fcf1-324">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="6fcf1-325"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="6fcf1-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="6fcf1-327">OK</span><span class="sxs-lookup"><span data-stu-id="6fcf1-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-328">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-331">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6fcf1-332">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6fcf1-333">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-335">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-337">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="6fcf1-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-339">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-342">Stringa che descrive il modo in cui viene identificato il controller di protocollo quando **NameFormat** è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="6fcf1-343">Questa proprietà viene ereditata da [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-345">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-347">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-347">The power management capabilities of the device.</span></span> <span data-ttu-id="6fcf1-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-350">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-352">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="6fcf1-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-355">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-357">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="6fcf1-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-360">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-362">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-362">Provides high level status information.</span></span> <span data-ttu-id="6fcf1-363">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6fcf1-364">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6fcf1-365">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6fcf1-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6fcf1-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6fcf1-372">)</span><span class="sxs-lookup"><span data-stu-id="6fcf1-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6fcf1-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-374">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-376">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="6fcf1-377">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6fcf1-378">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6fcf1-379">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6fcf1-380">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-380">Value</span></span>                                                                         | <span data-ttu-id="6fcf1-381">Significato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6fcf1-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6fcf1-383">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fcf1-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6fcf1-384">**Status**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-387">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-387">The current status of the object.</span></span> <span data-ttu-id="6fcf1-388">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-389">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-390">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-392">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6fcf1-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6fcf1-393">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="6fcf1-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-395">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-397">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-397">The current state of the logical device.</span></span> <span data-ttu-id="6fcf1-398">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-402">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-402">The scoping system's creation class name.</span></span> <span data-ttu-id="6fcf1-403">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-407">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="6fcf1-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-409">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-410">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-412">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6fcf1-413">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-414">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-415">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-417">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="6fcf1-418">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf1-419">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fcf1-420">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fcf1-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6fcf1-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fcf1-422">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6fcf1-423">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fcf1-424">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fcf1-424">Remarks</span></span>

<span data-ttu-id="6fcf1-425">L'accesso alla **classe \_ SCSIProtocolController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="6fcf1-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6fcf1-426">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6fcf1-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcf1-427">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fcf1-427">Requirements</span></span>



| <span data-ttu-id="6fcf1-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcf1-428">Requirement</span></span> | <span data-ttu-id="6fcf1-429">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf1-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcf1-430">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-430">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcf1-431">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6fcf1-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6fcf1-432">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcf1-432">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcf1-433">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6fcf1-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fcf1-434">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fcf1-434">Namespace</span></span><br/>                | <span data-ttu-id="6fcf1-435">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6fcf1-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6fcf1-436">MOF</span><span class="sxs-lookup"><span data-stu-id="6fcf1-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fcf1-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fcf1-438">DLL</span><span class="sxs-lookup"><span data-stu-id="6fcf1-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fcf1-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf1-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6fcf1-440">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fcf1-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcf1-441">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="6fcf1-442">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="6fcf1-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="6fcf1-443">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6fcf1-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

