---
description: Rappresenta lo stato del controller S3 emulato presente in ogni configurazione di macchina virtuale.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Classe Msvm_S3DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132098"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="f24ab-103">\_Classe MSVM S3DisplayController</span><span class="sxs-lookup"><span data-stu-id="f24ab-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="f24ab-104">Rappresenta lo stato del controller S3 emulato presente in ogni configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f24ab-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="f24ab-105">In una macchina virtuale può essere attivo un solo controller di visualizzazione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="f24ab-106">Questa classe si applica solo alle macchine virtuali di prima generazione.</span><span class="sxs-lookup"><span data-stu-id="f24ab-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="f24ab-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f24ab-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f24ab-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="f24ab-109">Members</span><span class="sxs-lookup"><span data-stu-id="f24ab-109">Members</span></span>

<span data-ttu-id="f24ab-110">La **classe \_ S3DisplayController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f24ab-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="f24ab-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f24ab-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f24ab-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f24ab-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f24ab-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f24ab-113">Methods</span></span>

<span data-ttu-id="f24ab-114">La **classe \_ S3DisplayController di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f24ab-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="f24ab-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="f24ab-115">Method</span></span>                                                                    | <span data-ttu-id="f24ab-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f24ab-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="f24ab-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f24ab-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="f24ab-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f24ab-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f24ab-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="f24ab-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f24ab-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f24ab-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="f24ab-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="f24ab-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f24ab-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="f24ab-124">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="f24ab-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f24ab-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="f24ab-126">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="f24ab-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="f24ab-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f24ab-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="f24ab-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f24ab-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f24ab-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="f24ab-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f24ab-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="f24ab-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f24ab-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f24ab-133">Properties</span></span>

<span data-ttu-id="f24ab-134">La **classe \_ S3DisplayController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f24ab-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f24ab-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-136">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-138">Funzionalità grafiche e 3D del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f24ab-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="f24ab-139">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f24ab-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-143">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f24ab-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="f24ab-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-145">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f24ab-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-146">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-148">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f24ab-148">The primary availability and status of the device.</span></span> <span data-ttu-id="f24ab-149">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f24ab-150">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-150">Value</span></span>                                                                        | <span data-ttu-id="f24ab-151">Significato</span><span class="sxs-lookup"><span data-stu-id="f24ab-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f24ab-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f24ab-153">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f24ab-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f24ab-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f24ab-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-155">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-157">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f24ab-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f24ab-158">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f24ab-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-160">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f24ab-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-162">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità di accelerazione video indicate nella matrice **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f24ab-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="f24ab-163">Ogni voce di questa matrice è correlata alla voce nella matrice **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="f24ab-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="f24ab-164">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f24ab-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-168">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f24ab-168">A short description of the object.</span></span> <span data-ttu-id="f24ab-169">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f24ab-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-171">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-173">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="f24ab-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f24ab-174">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f24ab-175">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f24ab-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f24ab-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="f24ab-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="f24ab-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="f24ab-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f24ab-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f24ab-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f24ab-183">)</span><span class="sxs-lookup"><span data-stu-id="f24ab-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f24ab-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f24ab-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-187">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f24ab-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f24ab-188">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ S3DisplayController".</span><span class="sxs-lookup"><span data-stu-id="f24ab-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-189">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f24ab-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-192">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f24ab-192">A description of the object.</span></span> <span data-ttu-id="f24ab-193">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f24ab-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-195">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-197">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f24ab-198">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f24ab-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f24ab-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="f24ab-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="f24ab-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="f24ab-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="f24ab-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="f24ab-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f24ab-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f24ab-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f24ab-208">)</span><span class="sxs-lookup"><span data-stu-id="f24ab-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f24ab-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f24ab-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-212">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f24ab-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f24ab-213">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f24ab-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-217">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f24ab-217">A display name for the object.</span></span> <span data-ttu-id="f24ab-218">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f24ab-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-220">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-222">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f24ab-223">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f24ab-224">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-224">Value</span></span>                                                                        | <span data-ttu-id="f24ab-225">Significato</span><span class="sxs-lookup"><span data-stu-id="f24ab-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f24ab-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f24ab-227">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f24ab-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f24ab-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f24ab-229">Disabled</span><span class="sxs-lookup"><span data-stu-id="f24ab-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f24ab-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-233">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f24ab-234">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="f24ab-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="f24ab-235">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled) o 3 (Disabled).</span><span class="sxs-lookup"><span data-stu-id="f24ab-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="f24ab-236">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-236">Value</span></span>                                                                        | <span data-ttu-id="f24ab-237">Significato</span><span class="sxs-lookup"><span data-stu-id="f24ab-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f24ab-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f24ab-239">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f24ab-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f24ab-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f24ab-241">Disabled</span><span class="sxs-lookup"><span data-stu-id="f24ab-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f24ab-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f24ab-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-243">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f24ab-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-245">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f24ab-246">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f24ab-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-250">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f24ab-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f24ab-251">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-255">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-255">The current health of the element.</span></span> <span data-ttu-id="f24ab-256">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f24ab-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f24ab-257">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="f24ab-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f24ab-258">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="f24ab-259">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-259">Value</span></span>                                                                        | <span data-ttu-id="f24ab-260">Significato</span><span class="sxs-lookup"><span data-stu-id="f24ab-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="f24ab-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="f24ab-262">OK</span><span class="sxs-lookup"><span data-stu-id="f24ab-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f24ab-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f24ab-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-264">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f24ab-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-266">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="f24ab-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f24ab-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f24ab-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-269">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f24ab-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-271">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f24ab-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f24ab-272">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f24ab-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-276">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f24ab-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-277">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f24ab-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f24ab-278">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f24ab-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-280">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f24ab-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-282">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f24ab-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="f24ab-283">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-284">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="f24ab-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f24ab-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-287">Quantità massima di memoria, in byte, supportata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="f24ab-288">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-289">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="f24ab-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-290">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f24ab-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-292">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="f24ab-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="f24ab-293">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="f24ab-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="f24ab-294">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="f24ab-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="f24ab-295">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="f24ab-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-296">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f24ab-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-297">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f24ab-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-299">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-299">This property has been deprecated.</span></span> <span data-ttu-id="f24ab-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-301">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f24ab-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-304">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f24ab-304">The label by which the object is known.</span></span> <span data-ttu-id="f24ab-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-306">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="f24ab-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-307">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f24ab-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-309">Il numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="f24ab-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="f24ab-310">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-311">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f24ab-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-312">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-314">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f24ab-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f24ab-315">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f24ab-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f24ab-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f24ab-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="f24ab-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="f24ab-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="f24ab-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="f24ab-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="f24ab-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="f24ab-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="f24ab-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="f24ab-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="f24ab-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="f24ab-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="f24ab-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="f24ab-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="f24ab-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="f24ab-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="f24ab-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f24ab-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f24ab-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f24ab-336">)</span><span class="sxs-lookup"><span data-stu-id="f24ab-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f24ab-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f24ab-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-338">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-340">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f24ab-340">The current statuses of the object.</span></span> <span data-ttu-id="f24ab-341">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="f24ab-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-342">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-345">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f24ab-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f24ab-346">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f24ab-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f24ab-347">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f24ab-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-349">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f24ab-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-351">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f24ab-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f24ab-352">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-353">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="f24ab-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-356">Stringa che descrive il tipo di architettura video quando la proprietà **VideoArchitecture** è 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="f24ab-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="f24ab-357">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-358">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="f24ab-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-359">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-361">Tipo di memoria video quando la proprietà **VideoMemoryType** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f24ab-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="f24ab-362">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f24ab-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-364">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-366">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f24ab-366">The power management capabilities of the device.</span></span> <span data-ttu-id="f24ab-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-368">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f24ab-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-369">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f24ab-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-371">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="f24ab-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f24ab-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-373">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f24ab-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-374">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f24ab-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-376">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="f24ab-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f24ab-377">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-378">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f24ab-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-379">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-381">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="f24ab-381">Provides high level status information.</span></span> <span data-ttu-id="f24ab-382">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f24ab-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f24ab-383">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f24ab-384">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f24ab-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f24ab-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f24ab-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="f24ab-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="f24ab-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f24ab-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f24ab-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f24ab-391">)</span><span class="sxs-lookup"><span data-stu-id="f24ab-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f24ab-392">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="f24ab-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-393">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-395">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="f24ab-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="f24ab-396">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="f24ab-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-397">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="f24ab-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-398">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-400">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="f24ab-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="f24ab-401">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="f24ab-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-403">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-405">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="f24ab-406">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f24ab-407">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="f24ab-408">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f24ab-409">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-409">Value</span></span>                                                                         | <span data-ttu-id="f24ab-410">Significato</span><span class="sxs-lookup"><span data-stu-id="f24ab-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f24ab-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f24ab-412">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f24ab-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f24ab-413">**Status**</span><span class="sxs-lookup"><span data-stu-id="f24ab-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-414">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-416">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f24ab-416">The current status of the object.</span></span> <span data-ttu-id="f24ab-417">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-418">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f24ab-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-419">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f24ab-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-421">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f24ab-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f24ab-422">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="f24ab-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f24ab-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-424">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-426">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f24ab-426">The current state of the logical device.</span></span> <span data-ttu-id="f24ab-427">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-428">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f24ab-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-429">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-431">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f24ab-431">The scoping system's creation class name.</span></span> <span data-ttu-id="f24ab-432">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f24ab-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-436">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="f24ab-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="f24ab-437">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f24ab-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="f24ab-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-439">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f24ab-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-441">Ora dell'ultima accensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f24ab-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="f24ab-442">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="f24ab-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-443">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f24ab-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-444">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f24ab-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-446">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f24ab-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f24ab-447">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-448">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f24ab-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-449">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f24ab-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-451">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="f24ab-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f24ab-452">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-453">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f24ab-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-456">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f24ab-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f24ab-457">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f24ab-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-458">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="f24ab-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-459">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-461">Specifica l'architettura video del controller di visualizzazione usato per generare il segnale video.</span><span class="sxs-lookup"><span data-stu-id="f24ab-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="f24ab-462">In genere, un processore video dedicato genera il segnale video in conformità con l'architettura specificata.</span><span class="sxs-lookup"><span data-stu-id="f24ab-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="f24ab-463">Si tratta di un indicatore della capacità di risoluzione massima del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f24ab-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="f24ab-464">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f24ab-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f24ab-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="f24ab-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="f24ab-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="f24ab-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="f24ab-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="f24ab-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="f24ab-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="f24ab-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-474"><span id="8514A"></span><span id="8514a"></span>**8514a** (9)</span><span class="sxs-lookup"><span data-stu-id="f24ab-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="f24ab-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer frame lineare** (11)</span><span class="sxs-lookup"><span data-stu-id="f24ab-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="f24ab-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f24ab-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f24ab-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f24ab-480">)</span><span class="sxs-lookup"><span data-stu-id="f24ab-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f24ab-481">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="f24ab-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-482">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f24ab-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-484">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="f24ab-484">The type of video memory.</span></span> <span data-ttu-id="f24ab-485">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f24ab-486">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="f24ab-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f24ab-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f24ab-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f24ab-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f24ab-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f24ab-489">Stringa che descrive il processore/controller video.</span><span class="sxs-lookup"><span data-stu-id="f24ab-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="f24ab-490">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f24ab-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f24ab-491">Commenti</span><span class="sxs-lookup"><span data-stu-id="f24ab-491">Remarks</span></span>

<span data-ttu-id="f24ab-492">L'accesso alla **classe \_ S3DisplayController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f24ab-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f24ab-493">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f24ab-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f24ab-494">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f24ab-494">Requirements</span></span>



| <span data-ttu-id="f24ab-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="f24ab-495">Requirement</span></span> | <span data-ttu-id="f24ab-496">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24ab-497">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24ab-497">Minimum supported client</span></span><br/> | <span data-ttu-id="f24ab-498">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f24ab-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f24ab-499">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24ab-499">Minimum supported server</span></span><br/> | <span data-ttu-id="f24ab-500">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f24ab-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f24ab-501">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f24ab-501">Namespace</span></span><br/>                | <span data-ttu-id="f24ab-502">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f24ab-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f24ab-503">MOF</span><span class="sxs-lookup"><span data-stu-id="f24ab-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f24ab-504"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f24ab-505">DLL</span><span class="sxs-lookup"><span data-stu-id="f24ab-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f24ab-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f24ab-507">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f24ab-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24ab-508">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="f24ab-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="f24ab-509">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f24ab-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f24ab-510">Classi video</span><span class="sxs-lookup"><span data-stu-id="f24ab-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

