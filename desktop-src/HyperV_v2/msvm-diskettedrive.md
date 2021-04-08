---
description: Rappresenta un'unità floppy all'interno della macchina virtuale.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757655"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="b610e-103">\_Classe MSVM DisketteDrive</span><span class="sxs-lookup"><span data-stu-id="b610e-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="b610e-104">Rappresenta un'unità floppy all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b610e-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="b610e-105">Un'unità floppy può essere popolata con un file che rappresenta un supporto floppy o l'unità può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="b610e-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="b610e-106">Il supporto fisico non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-106">Physical media is not supported.</span></span> <span data-ttu-id="b610e-107">Esiste esattamente un'unità floppy per ogni controller floppy e non è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="b610e-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="b610e-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b610e-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b610e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b610e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="b610e-110">Members</span><span class="sxs-lookup"><span data-stu-id="b610e-110">Members</span></span>

<span data-ttu-id="b610e-111">La **classe \_ DisketteDrive di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b610e-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b610e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b610e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b610e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b610e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b610e-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b610e-114">Methods</span></span>

<span data-ttu-id="b610e-115">La **classe \_ DisketteDrive di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b610e-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="b610e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b610e-116">Method</span></span>                                                              | <span data-ttu-id="b610e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b610e-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b610e-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b610e-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="b610e-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b610e-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="b610e-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="b610e-121">Blocca o rilascia i supporti.</span><span class="sxs-lookup"><span data-stu-id="b610e-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="b610e-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b610e-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="b610e-123">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b610e-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b610e-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="b610e-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b610e-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b610e-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="b610e-127">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="b610e-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="b610e-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b610e-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="b610e-129">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="b610e-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="b610e-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="b610e-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="b610e-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b610e-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="b610e-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="b610e-133">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b610e-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b610e-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="b610e-135">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b610e-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b610e-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b610e-136">Properties</span></span>

<span data-ttu-id="b610e-137">La **classe \_ DisketteDrive di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b610e-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b610e-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b610e-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-139">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-141">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="b610e-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b610e-143">Valore</span><span class="sxs-lookup"><span data-stu-id="b610e-143">Value</span></span>                                                                        | <span data-ttu-id="b610e-144">Significato</span><span class="sxs-lookup"><span data-stu-id="b610e-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="b610e-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="b610e-146">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="b610e-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b610e-147">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="b610e-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-150">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-150">The primary availability and status of the device.</span></span> <span data-ttu-id="b610e-151">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b610e-152">Valore</span><span class="sxs-lookup"><span data-stu-id="b610e-152">Value</span></span>                                                                        | <span data-ttu-id="b610e-153">Significato</span><span class="sxs-lookup"><span data-stu-id="b610e-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="b610e-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="b610e-155">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="b610e-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b610e-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b610e-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-157">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-159">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="b610e-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="b610e-160">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b610e-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="b610e-161">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="b610e-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="b610e-162">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="b610e-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="b610e-163">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b610e-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b610e-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-165">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-167">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="b610e-167">The capabilities of the media access device.</span></span> <span data-ttu-id="b610e-168">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b610e-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="b610e-169">Valore</span><span class="sxs-lookup"><span data-stu-id="b610e-169">Value</span></span>                                                                                | <span data-ttu-id="b610e-170">Significato</span><span class="sxs-lookup"><span data-stu-id="b610e-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b610e-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="b610e-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="b610e-173">La voce corrispondente in **CapabilityDescriptions** è "accesso casuale".</span><span class="sxs-lookup"><span data-stu-id="b610e-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="b610e-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="b610e-175">La voce corrispondente in **CapabilityDescriptions** è "supporta la scrittura".</span><span class="sxs-lookup"><span data-stu-id="b610e-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="b610e-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="b610e-177">La voce corrispondente in **CapabilityDescriptions** è "supporta supporti rimovibili".</span><span class="sxs-lookup"><span data-stu-id="b610e-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b610e-178">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b610e-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-179">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b610e-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-181">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nella matrice di proprietà delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="b610e-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="b610e-182">Ogni voce di questa matrice è correlata alla voce nella matrice di **funzionalità** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="b610e-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="b610e-183">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b610e-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-187">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b610e-187">A short description of the object.</span></span> <span data-ttu-id="b610e-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b610e-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-192">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="b610e-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b610e-193">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b610e-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b610e-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b610e-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-198">Stringa che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="b610e-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b610e-199">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="b610e-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b610e-200">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="b610e-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b610e-201">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="b610e-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="b610e-202">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="b610e-203">"Non compresso"</span><span class="sxs-lookup"><span data-stu-id="b610e-203">"Not Compressed"</span></span>

<span data-ttu-id="b610e-204">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="b610e-204">"Unknown"</span></span>

<span data-ttu-id="b610e-205">Compressi</span><span class="sxs-lookup"><span data-stu-id="b610e-205">"Compressed"</span></span>

<span data-ttu-id="b610e-206">"Non compresso"</span><span class="sxs-lookup"><span data-stu-id="b610e-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="b610e-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b610e-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-210">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="b610e-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b610e-211">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-212">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b610e-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-213">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-215">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="b610e-216">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-217">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b610e-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-220">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b610e-220">A description of the object.</span></span> <span data-ttu-id="b610e-221">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b610e-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-225">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="b610e-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b610e-226">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b610e-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b610e-227">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b610e-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-231">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="b610e-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="b610e-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b610e-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-235">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b610e-235">A display name for the object.</span></span> <span data-ttu-id="b610e-236">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b610e-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-240">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b610e-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b610e-241">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="b610e-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b610e-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-245">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="b610e-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b610e-246">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="b610e-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b610e-247">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b610e-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-248">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b610e-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-249">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b610e-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-251">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="b610e-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b610e-252">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b610e-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-256">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b610e-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="b610e-257">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-258">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b610e-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-261">Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="b610e-262">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b610e-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-264">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-266">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b610e-266">The current health of the element.</span></span> <span data-ttu-id="b610e-267">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b610e-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b610e-268">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="b610e-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b610e-269">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="b610e-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b610e-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-271">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b610e-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-273">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="b610e-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="b610e-274">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b610e-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b610e-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-276">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-278">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b610e-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b610e-279">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b610e-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-281">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b610e-283">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b610e-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b610e-284">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b610e-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b610e-285">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-286">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="b610e-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-287">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-289">Data e ora dell'ultima pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="b610e-290">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b610e-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b610e-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-294">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b610e-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="b610e-295">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-296">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-297">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-299">Tempo, in millisecondi, da caricare per poter leggere o scrivere un supporto.</span><span class="sxs-lookup"><span data-stu-id="b610e-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="b610e-300">Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per la lettura/scrittura (ovvero, il disco viene ruotato a velocità nominale).</span><span class="sxs-lookup"><span data-stu-id="b610e-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="b610e-301">Per le unità nastro, questo è il tempo da inserire in un supporto per segnalare che è pronto per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b610e-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="b610e-302">Si tratta in genere dell'area BOT del nastro.</span><span class="sxs-lookup"><span data-stu-id="b610e-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="b610e-303">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-304">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-305">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-307">Tempo, in millisecondi, per spostarsi dalla prima posizione sul supporto alla posizione più lontana rispetto al tempo.</span><span class="sxs-lookup"><span data-stu-id="b610e-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="b610e-308">Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo.</span><span class="sxs-lookup"><span data-stu-id="b610e-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="b610e-309">Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="b610e-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="b610e-310">(La fine di un nastro può essere il punto più distante fisicamente, ma ciò non è necessariamente vero). Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-311">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b610e-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-312">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-314">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="b610e-315">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-316">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="b610e-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-317">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-319">Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="b610e-320">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="b610e-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="b610e-321">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-322">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-323">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-325">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="b610e-325">This property has been deprecated.</span></span> <span data-ttu-id="b610e-326">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-327">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="b610e-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-328">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-330">Unità massime che è possibile utilizzare prima di pulire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="b610e-331">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-332">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="b610e-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-333">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b610e-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-335">**True** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b610e-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="b610e-336">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-337">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b610e-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-338">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-340">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="b610e-341">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-342">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="b610e-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-343">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-345">Per un dispositivo che supporta supporti rimovibili, il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="b610e-346">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="b610e-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="b610e-347">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-348">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b610e-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-351">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="b610e-351">The label by which the object is known.</span></span> <span data-ttu-id="b610e-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="b610e-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-353">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="b610e-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-354">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b610e-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-356">**True** se il dispositivo di accesso multimediale deve essere pulito. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b610e-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="b610e-357">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-358">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="b610e-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-359">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b610e-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-361">Numero massimo di supporti singoli che possono essere supportati o inseriti.</span><span class="sxs-lookup"><span data-stu-id="b610e-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="b610e-362">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b610e-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-364">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-366">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="b610e-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b610e-367">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b610e-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b610e-368">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b610e-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-372">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b610e-372">The current statuses of the object.</span></span> <span data-ttu-id="b610e-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="b610e-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-374">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b610e-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-375">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-377">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b610e-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b610e-378">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="b610e-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b610e-379">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b610e-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b610e-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-381">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b610e-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-383">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b610e-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b610e-384">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b610e-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-385">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b610e-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-386">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-388">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-388">The power management capabilities of the device.</span></span> <span data-ttu-id="b610e-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-390">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b610e-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-391">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b610e-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-393">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="b610e-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b610e-394">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-395">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b610e-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-396">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-398">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="b610e-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b610e-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-400">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b610e-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-401">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-403">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="b610e-403">Provides high level status information.</span></span> <span data-ttu-id="b610e-404">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="b610e-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="b610e-405">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="b610e-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b610e-406">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b610e-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b610e-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-408">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-410">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b610e-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="b610e-411">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="b610e-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b610e-412">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b610e-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="b610e-413">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="b610e-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="b610e-414">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b610e-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="b610e-415">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="b610e-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-416">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="b610e-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-417">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-419">Sicurezza operativa definita per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-419">The operational security defined for the device.</span></span> <span data-ttu-id="b610e-420">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="b610e-421">Valore</span><span class="sxs-lookup"><span data-stu-id="b610e-421">Value</span></span>                                                                        | <span data-ttu-id="b610e-422">Significato</span><span class="sxs-lookup"><span data-stu-id="b610e-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="b610e-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b610e-424">nessuno</span><span class="sxs-lookup"><span data-stu-id="b610e-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b610e-425">**Status**</span><span class="sxs-lookup"><span data-stu-id="b610e-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-426">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-427">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-428">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b610e-428">The current status of the object.</span></span> <span data-ttu-id="b610e-429">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-430">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b610e-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-431">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b610e-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b610e-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-433">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="b610e-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b610e-434">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="b610e-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b610e-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b610e-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-436">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-438">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b610e-438">The current state of the logical device.</span></span> <span data-ttu-id="b610e-439">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-440">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b610e-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-441">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-443">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="b610e-443">The scoping system's creation class name.</span></span> <span data-ttu-id="b610e-444">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b610e-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-446">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-448">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="b610e-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="b610e-449">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-450">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="b610e-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-451">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-452">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-453">Per un dispositivo che supporta supporti rimovibili, la data e l'ora più recenti in cui il supporto è stato montato sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="b610e-454">Per i dispositivi che accedono a supporti non rimovibili, ad esempio i dischi rigidi, questa proprietà non ha significato e non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="b610e-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="b610e-455">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-456">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b610e-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-457">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-459">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b610e-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b610e-460">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b610e-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-461">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-462">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-464">Per un dispositivo che supporta supporti rimovibili, il tempo totale (in secondi) per cui sono stati montati i supporti per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b610e-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="b610e-465">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="b610e-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="b610e-466">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-467">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b610e-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-468">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-470">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="b610e-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b610e-471">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-472">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b610e-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-473">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b610e-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-474">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-475">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b610e-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b610e-476">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b610e-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-477">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="b610e-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-478">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b610e-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-479">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-480">Velocità di trasferimento dati prolungata, in KB al secondo, che il dispositivo può leggere e scrivere su un supporto.</span><span class="sxs-lookup"><span data-stu-id="b610e-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="b610e-481">Si tratta di una velocità dati continua e non elaborata.</span><span class="sxs-lookup"><span data-stu-id="b610e-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="b610e-482">Frequenze o tariffe massime che presuppongono che la compressione non venga segnalata in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b610e-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="b610e-483">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-484">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="b610e-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-485">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b610e-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-487">Unità relative all'uso in **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="b610e-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="b610e-488">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="b610e-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b610e-489">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="b610e-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-490">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-491">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-492">Numero corrente di unità utilizzate.</span><span class="sxs-lookup"><span data-stu-id="b610e-492">The current number of units used.</span></span> <span data-ttu-id="b610e-493">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="b610e-494">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="b610e-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b610e-495">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b610e-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b610e-496">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b610e-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b610e-497">Tempo, in millisecondi, durante il quale è possibile leggere o scrivere un supporto nel relativo ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="b610e-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="b610e-498">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="b610e-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b610e-499">Commenti</span><span class="sxs-lookup"><span data-stu-id="b610e-499">Remarks</span></span>

<span data-ttu-id="b610e-500">L'accesso alla **classe \_ DisketteDrive di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b610e-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b610e-501">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b610e-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b610e-502">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b610e-502">Requirements</span></span>



| <span data-ttu-id="b610e-503">Requisito</span><span class="sxs-lookup"><span data-stu-id="b610e-503">Requirement</span></span> | <span data-ttu-id="b610e-504">Valore</span><span class="sxs-lookup"><span data-stu-id="b610e-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b610e-505">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b610e-505">Minimum supported client</span></span><br/> | <span data-ttu-id="b610e-506">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b610e-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b610e-507">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b610e-507">Minimum supported server</span></span><br/> | <span data-ttu-id="b610e-508">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b610e-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b610e-509">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b610e-509">Namespace</span></span><br/>                | <span data-ttu-id="b610e-510">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b610e-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b610e-511">MOF</span><span class="sxs-lookup"><span data-stu-id="b610e-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b610e-512"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b610e-513">DLL</span><span class="sxs-lookup"><span data-stu-id="b610e-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b610e-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b610e-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b610e-515">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b610e-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b610e-516">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="b610e-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="b610e-517">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="b610e-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="b610e-518">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b610e-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

