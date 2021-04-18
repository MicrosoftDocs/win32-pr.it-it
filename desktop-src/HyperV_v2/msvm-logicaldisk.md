---
description: Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Classe Msvm_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312909"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="2cc5a-103">\_Classe MSVM disco logico</span><span class="sxs-lookup"><span data-stu-id="2cc5a-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="2cc5a-104">Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="2cc5a-105">I tipi di supporto supportati includono i file rigidi virtuali, i file floppy virtuali, i file ISO e i supporti per i dispositivi fisici.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="2cc5a-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cc5a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
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
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="2cc5a-108">Members</span><span class="sxs-lookup"><span data-stu-id="2cc5a-108">Members</span></span>

<span data-ttu-id="2cc5a-109">La **classe \_ disco logico di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2cc5a-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="2cc5a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="2cc5a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2cc5a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cc5a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2cc5a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2cc5a-112">Methods</span></span>

<span data-ttu-id="2cc5a-113">La **classe \_ disco logico di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="2cc5a-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2cc5a-114">Method</span></span>                                                            | <span data-ttu-id="2cc5a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc5a-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="2cc5a-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="2cc5a-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2cc5a-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="2cc5a-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2cc5a-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="2cc5a-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="2cc5a-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="2cc5a-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="2cc5a-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="2cc5a-125">Reimposta il servizio.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="2cc5a-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="2cc5a-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2cc5a-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="2cc5a-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2cc5a-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="2cc5a-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2cc5a-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cc5a-132">Properties</span></span>

<span data-ttu-id="2cc5a-133">La **classe \_ disco logico di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cc5a-134">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-137">Indica se il supporto è leggibile, scrivibile o entrambi.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="2cc5a-138">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="2cc5a-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-139">Value</span></span>                                                                        | <span data-ttu-id="2cc5a-140">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="2cc5a-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2cc5a-142">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="2cc5a-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="2cc5a-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2cc5a-144">Leggibile.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="2cc5a-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2cc5a-146">Scrivibile.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="2cc5a-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2cc5a-148">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="2cc5a-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="2cc5a-150">Scrivere una sola volta.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-152">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-154">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="2cc5a-155">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2cc5a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-156">Value</span></span>                                                                            | <span data-ttu-id="2cc5a-157">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2cc5a-158"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="2cc5a-159">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-160">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-163">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-163">The primary availability and status of the device.</span></span> <span data-ttu-id="2cc5a-164">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2cc5a-165">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-165">Value</span></span>                                                                        | <span data-ttu-id="2cc5a-166">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2cc5a-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2cc5a-168">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-169">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-170">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-172">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2cc5a-173">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="2cc5a-174">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2cc5a-175">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2cc5a-176">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-180">Dimensione, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="2cc5a-181">Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="2cc5a-182">Se la dimensione del blocco è sconosciuta o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, questo conterrà 1.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="2cc5a-183">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-187">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-187">A short description of the object.</span></span> <span data-ttu-id="2cc5a-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="2cc5a-189">"Immagine disco ISO"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-189">"ISO Disk Image"</span></span>

<span data-ttu-id="2cc5a-190">"Immagine disco rigido"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-190">"Hard Disk Image"</span></span>

<span data-ttu-id="2cc5a-191">"Immagine disco floppy"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="2cc5a-192">"Disco CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-194">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-196">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2cc5a-197">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2cc5a-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-199">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-200">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-202">Numero massimo di blocchi, di dimensioni **blockSize**, che sono disponibili per l'utilizzo quando si esegue il layering degli extent di archiviazione utilizzando l'associazione [**MSVM \_ BasedOn**](msvm-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="2cc5a-203">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-205">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-207">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2cc5a-208">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-209">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-210">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-212">Tipo di organizzazione dati utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-212">The type of data organization used.</span></span> <span data-ttu-id="2cc5a-213">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="2cc5a-214">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-214">Value</span></span>                                                                        | <span data-ttu-id="2cc5a-215">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="2cc5a-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2cc5a-217">Blocco fisso.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-218">**Ridondanza dataridondanza**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-221">Numero di copie complete dei dati attualmente mantenute.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="2cc5a-222">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-223">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-224">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-226">Percentuale che specifica la quantità di spazio che deve essere riservata in una replica per la memorizzazione nella cache delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="2cc5a-227">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-228">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-229">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-231">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-231">A description of the object.</span></span> <span data-ttu-id="2cc5a-232">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-234">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-236">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2cc5a-237">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2cc5a-238">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-242">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="2cc5a-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-246">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-246">A display name for the object.</span></span> <span data-ttu-id="2cc5a-247">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="2cc5a-248">"Immagine disco ISO"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-248">"ISO Disk Image"</span></span>

<span data-ttu-id="2cc5a-249">"Immagine disco rigido"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-249">"Hard Disk Image"</span></span>

<span data-ttu-id="2cc5a-250">"Immagine disco floppy"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="2cc5a-251">"Disco CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="2cc5a-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-255">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2cc5a-256">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-260">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2cc5a-261">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2cc5a-262">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-263">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-264">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-266">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2cc5a-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-271">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2cc5a-272">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-273">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-274">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-276">Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="2cc5a-277">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-278">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-279">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-281">Eventuali informazioni aggiuntive sullo stato oltre a quelle acquisite in **OperationalStatus** e altre proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="2cc5a-282">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-282">Value</span></span>                                                                            | <span data-ttu-id="2cc5a-283">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="2cc5a-284"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="2cc5a-285">Nessuno/non applicabile.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-287">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-289">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-289">The current health of the element.</span></span> <span data-ttu-id="2cc5a-290">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2cc5a-291">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2cc5a-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-294">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-296">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="2cc5a-297">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-299">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-301">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2cc5a-302">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-306">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-307">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2cc5a-308">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-309">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-310">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-312">Indica se gli extent di archiviazione sottostanti partecipano a un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="2cc5a-313">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-317">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="2cc5a-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-319">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-320">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-322">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-322">This property has been deprecated.</span></span> <span data-ttu-id="2cc5a-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-324">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-327">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-327">The label by which the object is known.</span></span> <span data-ttu-id="2cc5a-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-330">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-332">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="2cc5a-333">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-333">Value</span></span>                                                                         | <span data-ttu-id="2cc5a-334">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2cc5a-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="2cc5a-336">Altro</span><span class="sxs-lookup"><span data-stu-id="2cc5a-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="2cc5a-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2cc5a-338">Nome dispositivo del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2cc5a-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-339">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-340">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-342">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="2cc5a-343">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-343">Value</span></span>                                                                        | <span data-ttu-id="2cc5a-344">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2cc5a-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2cc5a-346">Altro</span><span class="sxs-lookup"><span data-stu-id="2cc5a-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="2cc5a-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="2cc5a-348">Spazio dei nomi del dispositivo del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2cc5a-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc5a-349">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-350">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-352">Indica se non esiste alcun singolo punto di errore.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="2cc5a-353">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-355">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-357">Il numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="2cc5a-358">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="2cc5a-359">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="2cc5a-360">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-361">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-364">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2cc5a-365">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2cc5a-366">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-368">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-370">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="2cc5a-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-371">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-371">The current statuses of the object.</span></span> <span data-ttu-id="2cc5a-372">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="2cc5a-373">Quando il livello di QoS richiesto per il disco virtuale non può essere soddisfatto, lo stato primario (OperationalStatus \[ 0 \] ) viene impostato su ridotto (3) e la matrice OperationalStatus contiene inoltre un valore di stato secondario che indica il motivo specifico della condizione QoS, in base a questa tabella.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="2cc5a-374">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="2cc5a-375">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc5a-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc5a-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Velocità effettiva insufficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="2cc5a-377">La velocità di IOPS minima richiesta non è attualmente disponibile per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="2cc5a-378">OperationalStatus viene utilizzato anche per segnalare altre condizioni di errore o avviso, ad esempio la mancata corrispondenza del protocollo tra VSP e VSC.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="2cc5a-379">Se esistono più condizioni, lo stato primario viene impostato come danneggiato e uno o più valori di stato secondari, in qualsiasi ordine a partire dall'indice 1, vengono inseriti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2cc5a-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2cc5a-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="2cc5a-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="2cc5a-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (11)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-384">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2cc5a-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="2cc5a-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="2cc5a-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (16)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-388">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="2cc5a-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Mancata corrispondenza del protocollo** (32775)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="2cc5a-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout della comunicazione** (32783)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-391">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="2cc5a-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Velocità effettiva insufficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="2cc5a-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**ID criterio QoS sconosciuto** (32791)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="2cc5a-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS non supportata** (32792)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-395">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="2cc5a-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**Configurazione QoS non corrispondente** (32793)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-397">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="2cc5a-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disco pieno** (32794)</span><span class="sxs-lookup"><span data-stu-id="2cc5a-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="2cc5a-399">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2cc5a-400">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-403">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2cc5a-404">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2cc5a-405">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-407">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-409">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2cc5a-410">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-411">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-414">Stringa che descrive il formato della proprietà **Name** quando **NameFormat** contiene il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="2cc5a-415">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-416">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-417">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-419">Stringa che descrive lo spazio dei nomi della proprietà **Name** quando **NameNamespace** contiene il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="2cc5a-420">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-421">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-422">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-424">Il numero di pacchetti fisici che attualmente possono avere esito negativo senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="2cc5a-425">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-426">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-427">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-429">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-429">The power management capabilities of the device.</span></span> <span data-ttu-id="2cc5a-430">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-432">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-434">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2cc5a-435">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-437">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-438">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-439">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2cc5a-440">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-441">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-442">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-444">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-444">Provides high level status information.</span></span> <span data-ttu-id="2cc5a-445">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2cc5a-446">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2cc5a-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-448">**Originale**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-449">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-451">Indica se il sistema contenitore è in grado di creare o eliminare questo elemento operativo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="2cc5a-452">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è impostata su **false** per i supporti basati su file e **true** per i supporti pass-through.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-453">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-456">Stringa che descrive i supporti e/o il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="2cc5a-457">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-459">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-461">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="2cc5a-462">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2cc5a-463">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="2cc5a-464">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="2cc5a-465">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="2cc5a-466">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-468">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-470">Indica se l'accesso alla risorsa di archiviazione viene eseguito in modo sequenziale da un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="2cc5a-471">Il supporto per nastri pass-through è un esempio di un extent di archiviazione a cui si accede in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="2cc5a-472">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-473">**Status**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-476">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-476">The current status of the object.</span></span> <span data-ttu-id="2cc5a-477">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-478">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-479">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-481">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2cc5a-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2cc5a-482">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-484">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-485">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-486">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-486">The current state of the logical device.</span></span> <span data-ttu-id="2cc5a-487">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-488">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-489">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-490">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-491">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-491">The scoping system's creation class name.</span></span> <span data-ttu-id="2cc5a-492">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-494">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-496">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="2cc5a-497">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-498">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-499">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-501">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2cc5a-502">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-503">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-504">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-506">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2cc5a-507">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2cc5a-508">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cc5a-509">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cc5a-510">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cc5a-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cc5a-511">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2cc5a-512">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cc5a-513">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cc5a-513">Remarks</span></span>

<span data-ttu-id="2cc5a-514">L'accesso alla **classe \_ disco logico di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="2cc5a-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2cc5a-515">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2cc5a-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc5a-516">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc5a-516">Requirements</span></span>



| <span data-ttu-id="2cc5a-517">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc5a-517">Requirement</span></span> | <span data-ttu-id="2cc5a-518">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc5a-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc5a-519">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-519">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc5a-520">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2cc5a-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2cc5a-521">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc5a-521">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc5a-522">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2cc5a-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cc5a-523">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2cc5a-523">Namespace</span></span><br/>                | <span data-ttu-id="2cc5a-524">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2cc5a-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2cc5a-525">MOF</span><span class="sxs-lookup"><span data-stu-id="2cc5a-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cc5a-526"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cc5a-527">DLL</span><span class="sxs-lookup"><span data-stu-id="2cc5a-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cc5a-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2cc5a-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2cc5a-529">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cc5a-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc5a-530">**\_Disco logico CIM**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="2cc5a-531">**\_Disco logico CIM**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="2cc5a-532">**\_StorageAlert MSVM**</span><span class="sxs-lookup"><span data-stu-id="2cc5a-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="2cc5a-533">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2cc5a-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

