---
description: Rappresenta il controller di visualizzazione sintetico 3D assegnato a una macchina virtuale.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Classe Msvm_Synthetic3DDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310007"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="bc316-103">\_Classe MSVM Synthetic3DDisplayController</span><span class="sxs-lookup"><span data-stu-id="bc316-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="bc316-104">Rappresenta il controller di visualizzazione sintetico 3D assegnato a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc316-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="bc316-105">Questa classe viene utilizzata solo con le macchine virtuali che utilizzano RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="bc316-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc316-106">Quando si aggiunge un controller di visualizzazione sintetico 3D a una macchina virtuale, è necessario disabilitare qualsiasi controller di visualizzazione sintetico ([**MSVM \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) collegato a tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc316-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="bc316-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bc316-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc316-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc316-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="bc316-109">Members</span><span class="sxs-lookup"><span data-stu-id="bc316-109">Members</span></span>

<span data-ttu-id="bc316-110">La **classe \_ Synthetic3DDisplayController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc316-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="bc316-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc316-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc316-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc316-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc316-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc316-113">Methods</span></span>

<span data-ttu-id="bc316-114">La **classe \_ Synthetic3DDisplayController di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bc316-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="bc316-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc316-115">Method</span></span>                 | <span data-ttu-id="bc316-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc316-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="bc316-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="bc316-117">**EnableDevice**</span></span>       | <span data-ttu-id="bc316-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="bc316-119">**OnlineDevice**</span></span>       | <span data-ttu-id="bc316-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="bc316-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="bc316-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="bc316-123">**RequestStateChange**</span></span> | <span data-ttu-id="bc316-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-125">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="bc316-125">**Reset**</span></span>              | <span data-ttu-id="bc316-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="bc316-127">**RestoreProperties**</span></span>  | <span data-ttu-id="bc316-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="bc316-129">**SaveProperties**</span></span>     | <span data-ttu-id="bc316-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc316-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bc316-131">**SetPowerState**</span></span>      | <span data-ttu-id="bc316-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc316-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc316-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc316-133">Properties</span></span>

<span data-ttu-id="bc316-134">La **classe \_ Synthetic3DDisplayController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc316-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc316-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bc316-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-136">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-138">La grafica e le funzionalità 3D del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bc316-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="bc316-139">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="bc316-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bc316-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-144">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="bc316-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc316-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="bc316-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="bc316-148">Identificatore della GPU (Graphics Processing Unit) fisica allocata a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc316-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="bc316-149">Questa proprietà si applica solo alle macchine virtuali che usano RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="bc316-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="bc316-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-153">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bc316-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="bc316-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-155">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-157">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="bc316-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="bc316-158">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bc316-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc316-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-160">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bc316-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-162">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità di accelerazione video indicate nella matrice di proprietà **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="bc316-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="bc316-163">Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **AcceleratorCapabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="bc316-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="bc316-164">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bc316-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-168">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc316-168">A short description of the object.</span></span> <span data-ttu-id="bc316-169">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="bc316-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-171">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-173">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="bc316-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bc316-174">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bc316-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc316-175">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc316-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bc316-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="bc316-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="bc316-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="bc316-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="bc316-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc316-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bc316-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc316-183">)</span><span class="sxs-lookup"><span data-stu-id="bc316-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc316-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc316-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-187">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="bc316-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bc316-188">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bc316-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-189">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bc316-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-192">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="bc316-192">A description of the object.</span></span> <span data-ttu-id="bc316-193">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bc316-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-195">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-197">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="bc316-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bc316-198">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bc316-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc316-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc316-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="bc316-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="bc316-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="bc316-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="bc316-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="bc316-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="bc316-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc316-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bc316-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc316-208">)</span><span class="sxs-lookup"><span data-stu-id="bc316-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc316-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bc316-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-212">Identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc316-212">The device identifier.</span></span> <span data-ttu-id="bc316-213">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="bc316-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="bc316-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bc316-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-217">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc316-217">A display name for the object.</span></span> <span data-ttu-id="bc316-218">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="bc316-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-220">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-222">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bc316-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="bc316-223">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="bc316-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bc316-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-227">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bc316-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="bc316-228">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="bc316-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="bc316-229">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled) o 3 (Disabled).</span><span class="sxs-lookup"><span data-stu-id="bc316-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bc316-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc316-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-233">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bc316-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-237">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bc316-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-241">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bc316-241">The current health of the element.</span></span> <span data-ttu-id="bc316-242">Questo attributo esprime l'integrità dell'elemento, ma non necessariamente quello dei sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="bc316-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="bc316-243">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="bc316-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="bc316-244">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc316-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-246">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bc316-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-248">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bc316-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bc316-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-250">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc316-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-252">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc316-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="bc316-253">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc316-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc316-257">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bc316-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bc316-258">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="bc316-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bc316-259">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bc316-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-261">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc316-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-263">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-264">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="bc316-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-265">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc316-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-267">Quantità massima di memoria, in byte, supportata.</span><span class="sxs-lookup"><span data-stu-id="bc316-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="bc316-268">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-269">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="bc316-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-270">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc316-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-272">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="bc316-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="bc316-273">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="bc316-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="bc316-274">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="bc316-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="bc316-275">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="bc316-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="bc316-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-277">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bc316-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-279">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-280">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bc316-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-283">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="bc316-283">The label by which the object is known.</span></span> <span data-ttu-id="bc316-284">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-285">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="bc316-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-286">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc316-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-288">Il numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc316-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="bc316-289">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-290">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="bc316-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-291">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-293">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bc316-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bc316-294">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bc316-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc316-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc316-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bc316-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="bc316-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="bc316-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="bc316-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="bc316-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="bc316-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="bc316-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="bc316-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="bc316-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="bc316-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="bc316-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="bc316-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="bc316-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="bc316-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="bc316-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="bc316-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="bc316-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc316-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bc316-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc316-315">)</span><span class="sxs-lookup"><span data-stu-id="bc316-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc316-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bc316-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-317">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-319">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc316-319">The current statuses of the object.</span></span> <span data-ttu-id="bc316-320">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-321">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="bc316-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-324">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="bc316-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="bc316-325">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="bc316-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="bc316-326">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bc316-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bc316-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-328">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bc316-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bc316-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-331">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bc316-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-334">Stringa che descrive il tipo di architettura video quando la proprietà **VideoArchitecture** è 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="bc316-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="bc316-335">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-336">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bc316-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-339">Tipo di memoria video quando la proprietà **VideoMemoryType** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="bc316-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="bc316-340">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-341">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bc316-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-342">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bc316-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-346">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc316-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-349">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bc316-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-350">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bc316-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-352">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="bc316-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-354">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-356">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="bc316-356">Provides high level status information.</span></span> <span data-ttu-id="bc316-357">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="bc316-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="bc316-358">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="bc316-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc316-359">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc316-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bc316-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="bc316-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="bc316-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="bc316-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc316-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bc316-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc316-366">)</span><span class="sxs-lookup"><span data-stu-id="bc316-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc316-367">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="bc316-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-370">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="bc316-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="bc316-371">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="bc316-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="bc316-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-373">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-375">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="bc316-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="bc316-376">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="bc316-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="bc316-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-378">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-380">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bc316-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="bc316-381">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="bc316-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="bc316-382">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc316-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="bc316-383">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="bc316-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="bc316-384">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bc316-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="bc316-385">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 2 (Enabled), 3 (Disabled) o 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="bc316-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-386">**Status**</span><span class="sxs-lookup"><span data-stu-id="bc316-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-389">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-390">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc316-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-391">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="bc316-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc316-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-393">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="bc316-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="bc316-394">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bc316-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bc316-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-396">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-398">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc316-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-402">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="bc316-402">The scoping system's creation class name.</span></span> <span data-ttu-id="bc316-403">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bc316-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bc316-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-407">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="bc316-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="bc316-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="bc316-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="bc316-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-410">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc316-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-412">Ora dell'ultima accensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc316-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="bc316-413">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="bc316-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-414">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="bc316-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-415">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bc316-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-417">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bc316-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="bc316-418">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-419">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bc316-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-420">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bc316-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-422">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc316-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-423">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="bc316-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-424">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-426">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bc316-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="bc316-427">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="bc316-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc316-428">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bc316-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-429">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-431">Specifica l'architettura video del controller di visualizzazione usato per generare il segnale video.</span><span class="sxs-lookup"><span data-stu-id="bc316-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="bc316-432">In genere, un processore video dedicato genera il segnale video in conformità con l'architettura specificata.</span><span class="sxs-lookup"><span data-stu-id="bc316-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="bc316-433">Si tratta di un indicatore della capacità di risoluzione massima del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bc316-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="bc316-434">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bc316-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="bc316-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc316-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="bc316-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="bc316-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="bc316-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="bc316-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="bc316-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="bc316-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="bc316-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-444"><span id="8514A"></span><span id="8514a"></span>**8514a** (9)</span><span class="sxs-lookup"><span data-stu-id="bc316-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="bc316-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer frame lineare** (11)</span><span class="sxs-lookup"><span data-stu-id="bc316-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="bc316-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc316-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc316-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bc316-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc316-450">)</span><span class="sxs-lookup"><span data-stu-id="bc316-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc316-451">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bc316-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-452">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc316-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-454">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="bc316-454">The type of video memory.</span></span> <span data-ttu-id="bc316-455">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc316-456">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="bc316-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc316-457">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc316-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc316-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc316-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc316-459">Stringa che descrive il processore/controller video.</span><span class="sxs-lookup"><span data-stu-id="bc316-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="bc316-460">Questa proprietà viene ereditata da [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bc316-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc316-461">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc316-461">Requirements</span></span>



| <span data-ttu-id="bc316-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc316-462">Requirement</span></span> | <span data-ttu-id="bc316-463">Valore</span><span class="sxs-lookup"><span data-stu-id="bc316-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc316-464">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc316-464">Minimum supported client</span></span><br/> | <span data-ttu-id="bc316-465">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc316-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bc316-466">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc316-466">Minimum supported server</span></span><br/> | <span data-ttu-id="bc316-467">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc316-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc316-468">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc316-468">Namespace</span></span><br/>                | <span data-ttu-id="bc316-469">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc316-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bc316-470">MOF</span><span class="sxs-lookup"><span data-stu-id="bc316-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc316-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc316-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc316-472">DLL</span><span class="sxs-lookup"><span data-stu-id="bc316-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc316-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc316-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc316-474">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc316-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc316-475">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="bc316-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

