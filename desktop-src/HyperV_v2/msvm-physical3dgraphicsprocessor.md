---
description: Viene descritta la GPU (Graphics Processing Unit) fisica 3D.
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Classe Msvm_Physical3dGraphicsProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759644"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="66f3e-103">\_Classe MSVM Physical3dGraphicsProcessor</span><span class="sxs-lookup"><span data-stu-id="66f3e-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="66f3e-104">Viene descritta la GPU (Graphics Processing Unit) fisica 3D.</span><span class="sxs-lookup"><span data-stu-id="66f3e-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="66f3e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="66f3e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f3e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66f3e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="66f3e-107">Members</span><span class="sxs-lookup"><span data-stu-id="66f3e-107">Members</span></span>

<span data-ttu-id="66f3e-108">La **classe \_ Physical3dGraphicsProcessor di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="66f3e-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="66f3e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="66f3e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="66f3e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66f3e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="66f3e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="66f3e-111">Methods</span></span>

<span data-ttu-id="66f3e-112">La **classe \_ Physical3dGraphicsProcessor di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="66f3e-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="66f3e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="66f3e-113">Method</span></span>                 | <span data-ttu-id="66f3e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66f3e-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="66f3e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="66f3e-115">**EnableDevice**</span></span>       | <span data-ttu-id="66f3e-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="66f3e-117">**OnlineDevice**</span></span>       | <span data-ttu-id="66f3e-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="66f3e-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="66f3e-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="66f3e-121">**RequestStateChange**</span></span> | <span data-ttu-id="66f3e-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-123">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="66f3e-123">**Reset**</span></span>              | <span data-ttu-id="66f3e-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="66f3e-125">**RestoreProperties**</span></span>  | <span data-ttu-id="66f3e-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="66f3e-127">**SaveProperties**</span></span>     | <span data-ttu-id="66f3e-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="66f3e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-129">**SetPowerState**</span></span>      | <span data-ttu-id="66f3e-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="66f3e-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66f3e-131">Properties</span></span>

<span data-ttu-id="66f3e-132">La **classe \_ Physical3dGraphicsProcessor di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="66f3e-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66f3e-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="66f3e-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-136">Specifica l'identificatore dell'indice dell'adapter allocato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f3e-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="66f3e-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-140">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f3e-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="66f3e-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-142">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="66f3e-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-145">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f3e-145">The primary availability and status of the device.</span></span> <span data-ttu-id="66f3e-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="66f3e-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="66f3e-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="66f3e-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="66f3e-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="66f3e-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-153">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-155">Specifica la quantità di memoria video, in byte, disponibile per la GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-156">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="66f3e-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-159">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-159">A short description of the object.</span></span> <span data-ttu-id="66f3e-160">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="66f3e-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-162">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-164">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="66f3e-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="66f3e-165">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="66f3e-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="66f3e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="66f3e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="66f3e-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="66f3e-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="66f3e-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="66f3e-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="66f3e-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="66f3e-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="66f3e-174">)</span><span class="sxs-lookup"><span data-stu-id="66f3e-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66f3e-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="66f3e-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-176">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="66f3e-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-178">**true** se compatibile per la virtualizzazione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="66f3e-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="66f3e-179">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="66f3e-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="66f3e-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="66f3e-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-183">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="66f3e-183">The scoping system's creation class name.</span></span> <span data-ttu-id="66f3e-184">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="66f3e-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="66f3e-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-186">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-188">Specifica la quantità di memoria di sistema, in byte, dedicata alla GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="66f3e-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-190">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-192">Specifica la quantità di memoria video, in byte, dedicata alla GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-193">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="66f3e-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-196">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="66f3e-196">A description of the object.</span></span> <span data-ttu-id="66f3e-197">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="66f3e-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-201">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="66f3e-202">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="66f3e-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="66f3e-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="66f3e-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="66f3e-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="66f3e-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="66f3e-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="66f3e-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="66f3e-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="66f3e-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="66f3e-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="66f3e-212">)</span><span class="sxs-lookup"><span data-stu-id="66f3e-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66f3e-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="66f3e-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-216">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="66f3e-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="66f3e-217">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="66f3e-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="66f3e-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-221">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-222">Specifica il versione di DirectX supportato dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="66f3e-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-224">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66f3e-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-226">Specifica la data di compilazione del driver.</span><span class="sxs-lookup"><span data-stu-id="66f3e-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="66f3e-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-228">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66f3e-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-230">Specifica la data e l'ora di installazione del driver.</span><span class="sxs-lookup"><span data-stu-id="66f3e-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="66f3e-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-234">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-235">Specifica la versione del modello di driver.</span><span class="sxs-lookup"><span data-stu-id="66f3e-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="66f3e-236">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="66f3e-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="66f3e-237">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="66f3e-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-240">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-241">Specifica il nome del provider del driver.</span><span class="sxs-lookup"><span data-stu-id="66f3e-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="66f3e-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-245">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-246">Specifica la versione del driver.</span><span class="sxs-lookup"><span data-stu-id="66f3e-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="66f3e-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-250">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-250">A display name for the object.</span></span> <span data-ttu-id="66f3e-251">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="66f3e-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-255">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="66f3e-256">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="66f3e-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="66f3e-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-258">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="66f3e-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-260">Specifica se l'adapter è stato abilitato per l'utilizzo con RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="66f3e-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-262">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-264">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="66f3e-265">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="66f3e-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="66f3e-266">Valore</span><span class="sxs-lookup"><span data-stu-id="66f3e-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="66f3e-267">Significato</span><span class="sxs-lookup"><span data-stu-id="66f3e-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="66f3e-268"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="66f3e-269">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="66f3e-270"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="66f3e-271"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="66f3e-272">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="66f3e-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="66f3e-273"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="66f3e-274">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="66f3e-275"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="66f3e-276">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="66f3e-277"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="66f3e-278">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="66f3e-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="66f3e-279"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="66f3e-280">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="66f3e-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="66f3e-281"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="66f3e-282">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="66f3e-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="66f3e-283"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="66f3e-284">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="66f3e-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="66f3e-285"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="66f3e-286">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="66f3e-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="66f3e-287">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="66f3e-288">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="66f3e-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="66f3e-289"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="66f3e-290">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="66f3e-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="66f3e-291">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="66f3e-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="66f3e-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="66f3e-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-293">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="66f3e-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-295">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="66f3e-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="66f3e-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-300">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="66f3e-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="66f3e-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="66f3e-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-305">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-306">Contiene l'identificatore della GPU per l'adapter.</span><span class="sxs-lookup"><span data-stu-id="66f3e-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-308">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-310">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-310">The current health of the element.</span></span> <span data-ttu-id="66f3e-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="66f3e-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-313">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="66f3e-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-315">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="66f3e-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="66f3e-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="66f3e-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-318">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66f3e-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-320">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-320">The date and time when the object was installed.</span></span> <span data-ttu-id="66f3e-321">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="66f3e-322">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="66f3e-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-326">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="66f3e-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-327">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="66f3e-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="66f3e-328">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="66f3e-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-330">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66f3e-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-332">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="66f3e-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="66f3e-333">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="66f3e-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-335">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-337">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-337">This property has been deprecated.</span></span> <span data-ttu-id="66f3e-338">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-339">**Nome**</span><span class="sxs-lookup"><span data-stu-id="66f3e-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-342">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-342">The label by which the object is known.</span></span> <span data-ttu-id="66f3e-343">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="66f3e-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-345">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-347">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="66f3e-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="66f3e-348">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="66f3e-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="66f3e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="66f3e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="66f3e-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="66f3e-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="66f3e-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="66f3e-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="66f3e-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="66f3e-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="66f3e-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="66f3e-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="66f3e-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="66f3e-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="66f3e-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="66f3e-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="66f3e-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="66f3e-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="66f3e-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="66f3e-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="66f3e-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="66f3e-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="66f3e-369">)</span><span class="sxs-lookup"><span data-stu-id="66f3e-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66f3e-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="66f3e-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-371">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-373">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-373">The current statuses of the object.</span></span> <span data-ttu-id="66f3e-374">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-378">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="66f3e-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="66f3e-379">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="66f3e-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="66f3e-380">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="66f3e-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="66f3e-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-382">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="66f3e-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-384">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="66f3e-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="66f3e-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="66f3e-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-389">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="66f3e-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-390">Specifica il pixel shader versione supportato dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="66f3e-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-392">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-394">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f3e-394">The power management capabilities of the device.</span></span> <span data-ttu-id="66f3e-395">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="66f3e-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-397">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="66f3e-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-399">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="66f3e-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="66f3e-400">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="66f3e-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-402">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-404">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="66f3e-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="66f3e-405">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="66f3e-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-407">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-409">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="66f3e-409">Provides high level status information.</span></span> <span data-ttu-id="66f3e-410">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="66f3e-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="66f3e-411">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="66f3e-412">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="66f3e-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="66f3e-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="66f3e-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="66f3e-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="66f3e-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="66f3e-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="66f3e-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="66f3e-419">)</span><span class="sxs-lookup"><span data-stu-id="66f3e-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66f3e-420">**Rating**</span><span class="sxs-lookup"><span data-stu-id="66f3e-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-421">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-423">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="66f3e-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-424">Specifica la classificazione RemoteFX GPU per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f3e-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="66f3e-425">Questa proprietà non è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="66f3e-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-427">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-429">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="66f3e-430">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="66f3e-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="66f3e-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-432">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-434">Specifica la quantità di memoria di sistema condivisa, in byte, disponibile per la GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-435">**Status**</span><span class="sxs-lookup"><span data-stu-id="66f3e-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-438">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66f3e-438">The current status of the object.</span></span> <span data-ttu-id="66f3e-439">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="66f3e-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-441">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="66f3e-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-443">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="66f3e-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="66f3e-444">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="66f3e-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="66f3e-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-446">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-448">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="66f3e-448">The current state of the logical device.</span></span> <span data-ttu-id="66f3e-449">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="66f3e-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-451">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-453">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="66f3e-453">The scoping system's creation class name.</span></span> <span data-ttu-id="66f3e-454">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="66f3e-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="66f3e-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-456">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="66f3e-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-458">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="66f3e-458">The scoping system's name.</span></span> <span data-ttu-id="66f3e-459">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="66f3e-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="66f3e-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-461">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66f3e-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-462">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-463">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="66f3e-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="66f3e-464">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="66f3e-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="66f3e-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-466">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-468">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="66f3e-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="66f3e-469">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="66f3e-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="66f3e-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-471">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66f3e-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-473">Specifica la quantità totale di memoria video, in byte, presente nella GPU.</span><span class="sxs-lookup"><span data-stu-id="66f3e-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="66f3e-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="66f3e-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66f3e-475">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66f3e-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66f3e-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66f3e-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66f3e-477">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="66f3e-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="66f3e-478">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="66f3e-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66f3e-479">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66f3e-479">Requirements</span></span>



| <span data-ttu-id="66f3e-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f3e-480">Requirement</span></span> | <span data-ttu-id="66f3e-481">Valore</span><span class="sxs-lookup"><span data-stu-id="66f3e-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f3e-482">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66f3e-482">Minimum supported client</span></span><br/> | <span data-ttu-id="66f3e-483">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66f3e-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="66f3e-484">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66f3e-484">Minimum supported server</span></span><br/> | <span data-ttu-id="66f3e-485">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66f3e-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66f3e-486">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="66f3e-486">Namespace</span></span><br/>                | <span data-ttu-id="66f3e-487">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="66f3e-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66f3e-488">MOF</span><span class="sxs-lookup"><span data-stu-id="66f3e-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66f3e-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66f3e-490">DLL</span><span class="sxs-lookup"><span data-stu-id="66f3e-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66f3e-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66f3e-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

