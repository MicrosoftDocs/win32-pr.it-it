---
description: Rappresenta lo stato del controller di visualizzazione sintetico presente in ogni configurazione di macchina virtuale.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Classe Msvm_SyntheticDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880202"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="0b169-103">\_Classe MSVM SyntheticDisplayController</span><span class="sxs-lookup"><span data-stu-id="0b169-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="0b169-104">Rappresenta lo stato del controller di visualizzazione sintetico presente in ogni configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b169-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="0b169-105">In una macchina virtuale può essere attivo un solo controller di visualizzazione in qualsiasi momento e il controller sintetico può essere attivato solo quando il sistema operativo guest ha caricato i servizi di accelerazione video richiesti.</span><span class="sxs-lookup"><span data-stu-id="0b169-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="0b169-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0b169-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b169-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b169-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="0b169-108">Members</span><span class="sxs-lookup"><span data-stu-id="0b169-108">Members</span></span>

<span data-ttu-id="0b169-109">La **classe \_ SyntheticDisplayController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b169-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="0b169-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b169-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b169-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b169-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b169-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b169-112">Methods</span></span>

<span data-ttu-id="0b169-113">La **classe \_ SyntheticDisplayController di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0b169-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="0b169-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0b169-114">Method</span></span>                                                                           | <span data-ttu-id="0b169-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b169-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0b169-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0b169-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="0b169-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b169-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0b169-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="0b169-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b169-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0b169-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="0b169-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0b169-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b169-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="0b169-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0b169-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0b169-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="0b169-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="0b169-125">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b169-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="0b169-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0b169-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="0b169-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b169-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0b169-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="0b169-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b169-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0b169-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="0b169-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0b169-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0b169-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b169-132">Properties</span></span>

<span data-ttu-id="0b169-133">La **classe \_ SyntheticDisplayController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b169-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b169-134">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b169-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-135">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-137">La grafica e le funzionalità 3D del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0b169-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="0b169-138">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su 2 (Graphics Accelerator).</span><span class="sxs-lookup"><span data-stu-id="0b169-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0b169-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-140">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0b169-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-143">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="0b169-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0b169-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0b169-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0b169-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0b169-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-152">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b169-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-153">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0b169-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-155">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità di accelerazione video indicate nella matrice di proprietà **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0b169-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="0b169-156">Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="0b169-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="0b169-157">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su "Graphics Accelerator".</span><span class="sxs-lookup"><span data-stu-id="0b169-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-158">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0b169-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-161">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b169-161">A short description of the object.</span></span> <span data-ttu-id="0b169-162">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "display controller".</span><span class="sxs-lookup"><span data-stu-id="0b169-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0b169-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-164">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-166">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="0b169-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0b169-167">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b169-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b169-168">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b169-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b169-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="0b169-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="0b169-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="0b169-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="0b169-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b169-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b169-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b169-176">)</span><span class="sxs-lookup"><span data-stu-id="0b169-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b169-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b169-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-180">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0b169-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0b169-181">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ SyntheticDisplayController".</span><span class="sxs-lookup"><span data-stu-id="0b169-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-182">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0b169-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-185">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0b169-185">A description of the object.</span></span> <span data-ttu-id="0b169-186">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Synthetic display controller".</span><span class="sxs-lookup"><span data-stu-id="0b169-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0b169-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-190">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="0b169-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0b169-191">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b169-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b169-192">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b169-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="0b169-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="0b169-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="0b169-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="0b169-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="0b169-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="0b169-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b169-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b169-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b169-201">)</span><span class="sxs-lookup"><span data-stu-id="0b169-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b169-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0b169-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-205">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="0b169-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0b169-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-209">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b169-209">A display name for the object.</span></span> <span data-ttu-id="0b169-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "display controller" per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b169-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0b169-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-214">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b169-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0b169-215">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="0b169-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b169-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-219">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b169-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0b169-220">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="0b169-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0b169-221">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled) o 3 (Disabled).</span><span class="sxs-lookup"><span data-stu-id="0b169-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-222">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0b169-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-223">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0b169-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-225">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0b169-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-229">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0b169-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-231">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-233">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b169-233">The current health of the element.</span></span> <span data-ttu-id="0b169-234">Questo attributo esprime l'integrità dell'elemento, ma non necessariamente quello dei sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="0b169-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="0b169-235">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="0b169-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0b169-236">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="0b169-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b169-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-238">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0b169-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-240">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b169-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-242">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b169-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-244">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b169-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0b169-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b169-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b169-249">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0b169-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0b169-250">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0b169-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0b169-251">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0b169-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-253">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b169-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-255">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-256">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="0b169-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-257">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b169-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-259">Quantità massima di memoria, in byte, supportata.</span><span class="sxs-lookup"><span data-stu-id="0b169-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="0b169-260">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su 4.194.304 (0x400000).</span><span class="sxs-lookup"><span data-stu-id="0b169-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-261">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="0b169-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b169-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-264">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="0b169-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="0b169-265">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="0b169-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="0b169-266">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="0b169-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="0b169-267">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="0b169-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0b169-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b169-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-271">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-272">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0b169-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-275">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="0b169-275">The label by which the object is known.</span></span> <span data-ttu-id="0b169-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="0b169-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-277">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="0b169-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-278">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b169-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-280">Il numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="0b169-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="0b169-281">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su 1024.</span><span class="sxs-lookup"><span data-stu-id="0b169-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0b169-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-285">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0b169-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0b169-286">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b169-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b169-287">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b169-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b169-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="0b169-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="0b169-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="0b169-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="0b169-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="0b169-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="0b169-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="0b169-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="0b169-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="0b169-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="0b169-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="0b169-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="0b169-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="0b169-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="0b169-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="0b169-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="0b169-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b169-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b169-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b169-307">)</span><span class="sxs-lookup"><span data-stu-id="0b169-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b169-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0b169-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-309">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-311">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b169-311">The current statuses of the object.</span></span> <span data-ttu-id="0b169-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="0b169-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b169-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-316">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0b169-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0b169-317">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="0b169-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0b169-318">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0b169-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-320">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0b169-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-323">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="0b169-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-326">Stringa che descrive il tipo di architettura video quando la proprietà **VideoArchitecture** è 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="0b169-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="0b169-327">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b169-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-328">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="0b169-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-331">Tipo di memoria video quando la proprietà **VideoMemoryType** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0b169-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="0b169-332">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b169-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-334">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-336">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-337">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0b169-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-338">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0b169-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0b169-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b169-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-345">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0b169-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-346">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-348">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="0b169-348">Provides high level status information.</span></span> <span data-ttu-id="0b169-349">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0b169-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0b169-350">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b169-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b169-351">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b169-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b169-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b169-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0b169-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="0b169-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="0b169-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b169-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b169-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b169-358">)</span><span class="sxs-lookup"><span data-stu-id="0b169-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b169-359">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="0b169-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-362">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="0b169-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="0b169-363">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è sempre impostata su "video".</span><span class="sxs-lookup"><span data-stu-id="0b169-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-364">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="0b169-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-365">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-367">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="0b169-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="0b169-368">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è sempre impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0b169-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0b169-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-370">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-372">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b169-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="0b169-373">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="0b169-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0b169-374">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0b169-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0b169-375">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="0b169-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="0b169-376">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0b169-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0b169-377">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è impostata su 2 (Enabled), 3 (Disabled) o 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="0b169-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="0b169-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-381">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-382">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b169-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-383">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0b169-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b169-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-385">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0b169-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0b169-386">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="0b169-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0b169-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-388">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-390">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b169-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-392">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-394">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0b169-394">The scoping system's creation class name.</span></span> <span data-ttu-id="0b169-395">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="0b169-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0b169-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0b169-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-399">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="0b169-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="0b169-400">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="0b169-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="0b169-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-402">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b169-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-404">Ora dell'ultima accensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b169-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="0b169-405">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="0b169-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-406">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b169-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-407">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b169-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-409">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b169-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0b169-410">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b169-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-411">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0b169-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-412">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b169-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-414">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b169-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-415">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0b169-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-416">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-418">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b169-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0b169-419">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b169-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b169-420">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="0b169-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-421">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-423">Specifica l'architettura video del controller di visualizzazione usato per generare il segnale video.</span><span class="sxs-lookup"><span data-stu-id="0b169-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="0b169-424">In genere, un processore video dedicato genera il segnale video in conformità con l'architettura specificata.</span><span class="sxs-lookup"><span data-stu-id="0b169-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="0b169-425">Si tratta di un indicatore della capacità di risoluzione massima del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0b169-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="0b169-426">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b169-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0b169-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b169-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0b169-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="0b169-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="0b169-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="0b169-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="0b169-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="0b169-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="0b169-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="0b169-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-436"><span id="8514A"></span><span id="8514a"></span>**8514a** (9)</span><span class="sxs-lookup"><span data-stu-id="0b169-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="0b169-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer frame lineare** (11)</span><span class="sxs-lookup"><span data-stu-id="0b169-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="0b169-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b169-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b169-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b169-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b169-442">)</span><span class="sxs-lookup"><span data-stu-id="0b169-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b169-443">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="0b169-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-444">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b169-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-446">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="0b169-446">The type of video memory.</span></span> <span data-ttu-id="0b169-447">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su 2 (VRAM).</span><span class="sxs-lookup"><span data-stu-id="0b169-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="0b169-448">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="0b169-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b169-449">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b169-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b169-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b169-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b169-451">Stringa che descrive il processore/controller video.</span><span class="sxs-lookup"><span data-stu-id="0b169-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="0b169-452">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))ed è sempre impostata su "elaborazione video sintetica".</span><span class="sxs-lookup"><span data-stu-id="0b169-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b169-453">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b169-453">Remarks</span></span>

<span data-ttu-id="0b169-454">L'accesso alla **classe \_ SyntheticDisplayController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0b169-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0b169-455">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0b169-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b169-456">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b169-456">Requirements</span></span>



| <span data-ttu-id="0b169-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b169-457">Requirement</span></span> | <span data-ttu-id="0b169-458">Valore</span><span class="sxs-lookup"><span data-stu-id="0b169-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b169-459">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b169-459">Minimum supported client</span></span><br/> | <span data-ttu-id="0b169-460">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b169-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b169-461">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b169-461">Minimum supported server</span></span><br/> | <span data-ttu-id="0b169-462">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b169-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b169-463">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b169-463">Namespace</span></span><br/>                | <span data-ttu-id="0b169-464">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b169-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b169-465">MOF</span><span class="sxs-lookup"><span data-stu-id="0b169-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b169-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b169-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b169-467">DLL</span><span class="sxs-lookup"><span data-stu-id="0b169-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b169-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b169-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b169-469">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b169-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b169-470">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="0b169-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="0b169-471">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b169-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b169-472">Classi video</span><span class="sxs-lookup"><span data-stu-id="0b169-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

