---
description: Rappresenta la memoria attualmente allocata a una macchina virtuale.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Classe Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885154"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="e9f3d-103">\_Classe di memoria MSVM</span><span class="sxs-lookup"><span data-stu-id="e9f3d-103">Msvm\_Memory class</span></span>

<span data-ttu-id="e9f3d-104">Rappresenta la memoria attualmente allocata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="e9f3d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f3d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f3d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="e9f3d-107">Members</span><span class="sxs-lookup"><span data-stu-id="e9f3d-107">Members</span></span>

<span data-ttu-id="e9f3d-108">La classe di **\_ memoria MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9f3d-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="e9f3d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9f3d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9f3d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9f3d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9f3d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9f3d-111">Methods</span></span>

<span data-ttu-id="e9f3d-112">La classe di **\_ memoria MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="e9f3d-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e9f3d-113">Method</span></span>                                                       | <span data-ttu-id="e9f3d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f3d-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e9f3d-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="e9f3d-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e9f3d-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="e9f3d-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e9f3d-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="e9f3d-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e9f3d-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="e9f3d-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e9f3d-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="e9f3d-124">Reimposta la memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="e9f3d-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="e9f3d-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e9f3d-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="e9f3d-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e9f3d-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="e9f3d-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e9f3d-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9f3d-131">Properties</span></span>

<span data-ttu-id="e9f3d-132">La classe di **\_ memoria MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-133">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-136">Descrive le proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="e9f3d-137">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è impostata su 3 (lettura/scrittura supportata) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-139">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-143">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-145">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-146">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-149">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-151">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-153">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e9f3d-154">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-156">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-158">Dimensione, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e9f3d-159">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e9f3d-160">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="e9f3d-161">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 1048576.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-162">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-165">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-165">A short description of the object.</span></span> <span data-ttu-id="e9f3d-166">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-170">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e9f3d-171">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e9f3d-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e9f3d-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e9f3d-180">)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9f3d-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-182">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-184">Numero massimo di blocchi, di dimensioni **blockSize**, che sono disponibili per l'utilizzo quando si esegue il layering degli extent di archiviazione utilizzando l'associazione BasedOn.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="e9f3d-185">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-187">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-189">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-193">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e9f3d-194">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-195">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-198">Tipo di organizzazione dati utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-198">The type of data organization used.</span></span> <span data-ttu-id="e9f3d-199">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 2.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-200">**Ridondanza dataridondanza**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-201">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-203">Numero di copie complete dei dati attualmente gestiti.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="e9f3d-204">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-206">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-208">Valore corrente per la prenotazione Delta.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-208">The current value for delta reservation.</span></span> <span data-ttu-id="e9f3d-209">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-210">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-213">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-213">A description of the object.</span></span> <span data-ttu-id="e9f3d-214">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-216">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-218">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e9f3d-219">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e9f3d-220">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e9f3d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e9f3d-229">)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9f3d-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-233">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e9f3d-234">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-238">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-238">A display name for the object.</span></span> <span data-ttu-id="e9f3d-239">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-241">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-243">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e9f3d-244">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-246">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-248">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e9f3d-249">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e9f3d-250">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e9f3d-251">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f3d-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e9f3d-252">Significato</span><span class="sxs-lookup"><span data-stu-id="e9f3d-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e9f3d-253"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e9f3d-254">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e9f3d-255"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e9f3d-256"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e9f3d-257">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e9f3d-258"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e9f3d-259">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="e9f3d-260"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="e9f3d-261">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e9f3d-262"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e9f3d-263">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e9f3d-264"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e9f3d-265">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="e9f3d-266"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="e9f3d-267">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="e9f3d-268"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="e9f3d-269">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e9f3d-270"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e9f3d-271">L'elemento è abilitato, ma è in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="e9f3d-272">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="e9f3d-273">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="e9f3d-274"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="e9f3d-275">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="e9f3d-276">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="e9f3d-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-278">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-280">Indirizzo finale del blocco di memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="e9f3d-281">Poiché la proprietà **IndirizzoIniziale** è sempre 0, questo valore riflette sempre la quantità totale di memoria nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-285">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-287">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-289">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-291">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-293">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-295">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-297">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-299">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-301">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-307">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-309">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-313">Stringa che descrive il tipo di rilevamento e correzione degli errori supportato da questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="e9f3d-314">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-316">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-318">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-320">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-322">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory) ma non usata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-324">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-326">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-328">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-330">Gli extent di archiviazione hanno informazioni di stato aggiuntive oltre a quelle acquisite in **OperationalStatus** e altre proprietà ereditate da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="e9f3d-331">Queste informazioni aggiuntive (ad esempio, "Protection Disabled", value = 9) vengono acquisite nella proprietà **VolumeStatus** .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="e9f3d-332">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 2 (nessuna/non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-334">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-336">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-336">The current health of the element.</span></span> <span data-ttu-id="e9f3d-337">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e9f3d-338">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e9f3d-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-341">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-343">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-345">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-347">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e9f3d-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-352">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-353">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e9f3d-354">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-356">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-358">**True** se gli extent di archiviazione sottostanti fanno parte di un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="e9f3d-359">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-361">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-363">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-365">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-368">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-371">Qualificatori: **maxlen** (1024), **override** ("Name")</span><span class="sxs-lookup"><span data-stu-id="e9f3d-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-372">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-372">The label by which the object is known.</span></span> <span data-ttu-id="e9f3d-373">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="e9f3d-374">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="e9f3d-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-378">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-380">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-382">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-384">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-386">**True** se non esiste alcun singolo punto di errore.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="e9f3d-387">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-389">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-391">Valore calcolato che rappresenta la quantità totale di memoria divisa dal **blockSize**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="e9f3d-392">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-394">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-396">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e9f3d-397">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e9f3d-398">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e9f3d-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e9f3d-418">)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9f3d-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-420">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-422">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-422">The current statuses of the object.</span></span> <span data-ttu-id="e9f3d-423">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-425">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-427">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e9f3d-428">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e9f3d-429">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-431">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-433">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-435">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-437">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-441">Spazio dei nomi della proprietà **Name** quando la proprietà **NameFormat** include il valore 1 (other ").</span><span class="sxs-lookup"><span data-stu-id="e9f3d-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="e9f3d-442">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-444">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-446">Spazio dei nomi della proprietà **Name** quando la proprietà **NameNamespace** include il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="e9f3d-447">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-449">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-451">Il numero di pacchetti fisici che attualmente possono avere esito negativo senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="e9f3d-452">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-454">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-456">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-458">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-460">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-462">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-464">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-466">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-468">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-468">Provides high level status information.</span></span> <span data-ttu-id="e9f3d-469">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e9f3d-470">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e9f3d-471">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e9f3d-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e9f3d-478">)</span><span class="sxs-lookup"><span data-stu-id="e9f3d-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9f3d-479">**Originale**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-480">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-482">**True** se il sistema che lo contiene non è in grado di creare o eliminare questo elemento operativo.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="e9f3d-483">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-484">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-485">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-487">Stringa che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-487">A string that describes the media and its use.</span></span> <span data-ttu-id="e9f3d-488">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su "System Memory".</span><span class="sxs-lookup"><span data-stu-id="e9f3d-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-490">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-491">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-492">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="e9f3d-493">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e9f3d-494">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e9f3d-495">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e9f3d-496">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e9f3d-497">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-499">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-501">**True** se l'accesso all'archiviazione viene eseguito in modo sequenziale da un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="e9f3d-502">Una partizione nastro è un esempio di un extent di archiviazione a cui si accede in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="e9f3d-503">I volumi di archiviazione, le partizioni disco e i dischi logici rappresentano extent ad accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="e9f3d-504">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è sempre impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-505">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-506">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-508">Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="e9f3d-509">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-510">**Status**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-513">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-515">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-516">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-517">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e9f3d-518">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-520">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-521">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-522">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-524">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-525">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-526">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-526">The scoping system's creation class name.</span></span> <span data-ttu-id="e9f3d-527">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-529">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-531">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-533">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-535">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e9f3d-536">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-538">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-539">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-540">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e9f3d-541">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su "null".</span><span class="sxs-lookup"><span data-stu-id="e9f3d-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-543">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-544">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-545">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-547">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-549">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e9f3d-550">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-551">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f3d-552">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9f3d-553">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f3d-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9f3d-554">Indica se la memoria è volatile.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="e9f3d-555">Questa proprietà viene ereditata [**dalla \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f3d-556">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f3d-556">Remarks</span></span>

<span data-ttu-id="e9f3d-557">L'accesso alla classe di **\_ memoria MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e9f3d-558">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e9f3d-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f3d-559">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f3d-559">Requirements</span></span>



| <span data-ttu-id="e9f3d-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f3d-560">Requirement</span></span> | <span data-ttu-id="e9f3d-561">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f3d-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f3d-562">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f3d-562">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f3d-563">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9f3d-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9f3d-564">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f3d-564">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f3d-565">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9f3d-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9f3d-566">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9f3d-566">Namespace</span></span><br/>                | <span data-ttu-id="e9f3d-567">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e9f3d-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9f3d-568">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f3d-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f3d-569"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f3d-570">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f3d-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f3d-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9f3d-572">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f3d-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f3d-573">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="e9f3d-574">**\_Memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="e9f3d-575">Classi di memoria</span><span class="sxs-lookup"><span data-stu-id="e9f3d-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

