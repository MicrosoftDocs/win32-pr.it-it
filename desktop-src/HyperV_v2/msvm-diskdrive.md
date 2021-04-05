---
description: Rappresenta un'unità disco rigido all'interno di una macchina virtuale.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884602"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="eb1db-103">\_Classe MSVM DiskDrive</span><span class="sxs-lookup"><span data-stu-id="eb1db-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="eb1db-104">Rappresenta un'unità disco rigido all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="eb1db-105">Questa unità disco rigido può essere un dispositivo pass-through (se un disco rigido fisico è stato collegato alla macchina virtuale) o un dispositivo sintetico popolato con supporti disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="eb1db-106">Poiché i dischi rigidi virtuali e fisici possono essere aggiunti e rimossi dalla macchina virtuale, sono presenti due pool di risorse associati a questa classe, uno per i dischi rigidi pass-through e l'altro per i dischi rigidi virtuali.</span><span class="sxs-lookup"><span data-stu-id="eb1db-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="eb1db-107">I dischi rigidi possono essere aggiunti o rimossi solo dal controller SCSI virtuale quando la macchina virtuale è online.</span><span class="sxs-lookup"><span data-stu-id="eb1db-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="eb1db-108">I dischi possono essere aggiunti o rimossi solo dal controller IDE virtuale quando la macchina virtuale è offline.</span><span class="sxs-lookup"><span data-stu-id="eb1db-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="eb1db-109">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eb1db-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1db-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb1db-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="eb1db-111">Members</span><span class="sxs-lookup"><span data-stu-id="eb1db-111">Members</span></span>

<span data-ttu-id="eb1db-112">La **classe \_ DiskDrive di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eb1db-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="eb1db-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="eb1db-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="eb1db-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb1db-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eb1db-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="eb1db-115">Methods</span></span>

<span data-ttu-id="eb1db-116">La **classe \_ DiskDrive di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="eb1db-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="eb1db-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="eb1db-117">Method</span></span>                                                          | <span data-ttu-id="eb1db-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb1db-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="eb1db-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="eb1db-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="eb1db-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="eb1db-121">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="eb1db-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="eb1db-122">Blocca o rilascia i supporti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="eb1db-123">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="eb1db-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="eb1db-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="eb1db-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="eb1db-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="eb1db-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="eb1db-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="eb1db-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="eb1db-128">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="eb1db-129">**Reset**</span><span class="sxs-lookup"><span data-stu-id="eb1db-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="eb1db-130">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="eb1db-131">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="eb1db-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="eb1db-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="eb1db-133">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="eb1db-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="eb1db-134">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="eb1db-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="eb1db-136">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eb1db-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eb1db-137">Properties</span></span>

<span data-ttu-id="eb1db-138">La **classe \_ DiskDrive di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb1db-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb1db-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="eb1db-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-140">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="eb1db-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-143">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="eb1db-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="eb1db-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="eb1db-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="eb1db-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb1db-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="eb1db-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-153">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-155">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-155">The capabilities of the media access device.</span></span> <span data-ttu-id="eb1db-156">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="eb1db-157">Valore</span><span class="sxs-lookup"><span data-stu-id="eb1db-157">Value</span></span>                                                                        | <span data-ttu-id="eb1db-158">Significato</span><span class="sxs-lookup"><span data-stu-id="eb1db-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb1db-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="eb1db-160">La voce corrispondente in **CapabilityDescriptions** è "accesso casuale".</span><span class="sxs-lookup"><span data-stu-id="eb1db-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="eb1db-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="eb1db-162">La voce corrispondente in **CapabilityDescriptions** è "supporta la scrittura".</span><span class="sxs-lookup"><span data-stu-id="eb1db-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eb1db-163">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="eb1db-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-164">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="eb1db-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-166">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nella matrice di proprietà delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="eb1db-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="eb1db-167">Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **capabilities** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="eb1db-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="eb1db-168">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-169">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="eb1db-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-172">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-172">A short description of the object.</span></span> <span data-ttu-id="eb1db-173">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-174">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="eb1db-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-175">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-177">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="eb1db-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="eb1db-178">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eb1db-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eb1db-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eb1db-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="eb1db-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="eb1db-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="eb1db-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="eb1db-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="eb1db-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eb1db-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eb1db-187">)</span><span class="sxs-lookup"><span data-stu-id="eb1db-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb1db-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="eb1db-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-191">Stringa che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="eb1db-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="eb1db-192">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="eb1db-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="eb1db-193">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="eb1db-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="eb1db-194">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="eb1db-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="eb1db-195">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su "non compresso".</span><span class="sxs-lookup"><span data-stu-id="eb1db-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb1db-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-197">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-199">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="eb1db-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eb1db-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-201">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="eb1db-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-202">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-204">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="eb1db-205">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 512.</span><span class="sxs-lookup"><span data-stu-id="eb1db-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-206">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="eb1db-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-209">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="eb1db-209">A description of the object.</span></span> <span data-ttu-id="eb1db-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="eb1db-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-214">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="eb1db-215">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eb1db-216">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eb1db-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="eb1db-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="eb1db-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="eb1db-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="eb1db-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="eb1db-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="eb1db-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="eb1db-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eb1db-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eb1db-225">)</span><span class="sxs-lookup"><span data-stu-id="eb1db-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb1db-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb1db-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-229">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="eb1db-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="eb1db-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-231">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="eb1db-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-232">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb1db-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-234">Il numero di unità fisiche nel computer host.</span><span class="sxs-lookup"><span data-stu-id="eb1db-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eb1db-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-238">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-238">A display name for the object.</span></span> <span data-ttu-id="eb1db-239">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="eb1db-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-241">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-243">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="eb1db-244">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb1db-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-246">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-248">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="eb1db-249">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="eb1db-250">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb1db-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="eb1db-251">Valore</span><span class="sxs-lookup"><span data-stu-id="eb1db-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="eb1db-252">Significato</span><span class="sxs-lookup"><span data-stu-id="eb1db-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="eb1db-253"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="eb1db-254">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="eb1db-255"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="eb1db-256"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="eb1db-257">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="eb1db-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="eb1db-258"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="eb1db-259">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="eb1db-260"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="eb1db-261">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="eb1db-262"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="eb1db-263">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="eb1db-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="eb1db-264"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="eb1db-265">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="eb1db-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="eb1db-266"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="eb1db-267">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="eb1db-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="eb1db-268"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="eb1db-269">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="eb1db-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="eb1db-270"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="eb1db-271">L'elemento è abilitato, ma è in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="eb1db-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="eb1db-272">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="eb1db-273">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="eb1db-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="eb1db-274"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="eb1db-275">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="eb1db-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="eb1db-276">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="eb1db-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="eb1db-277">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="eb1db-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-278">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb1db-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-280">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="eb1db-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-285">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="eb1db-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-288">Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="eb1db-289">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su "None".</span><span class="sxs-lookup"><span data-stu-id="eb1db-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-291">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-293">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-293">The current health of the element.</span></span> <span data-ttu-id="eb1db-294">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="eb1db-295">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="eb1db-296">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="eb1db-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="eb1db-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-298">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="eb1db-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eb1db-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-302">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-304">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb1db-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="eb1db-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb1db-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-309">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="eb1db-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-310">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="eb1db-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="eb1db-311">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-312">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="eb1db-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-313">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-315">Data e ora dell'ultima pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="eb1db-316">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eb1db-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb1db-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-321">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-322">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-324">Tempo, in millisecondi, da caricare per poter leggere o scrivere un supporto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="eb1db-325">Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per la lettura/scrittura (ovvero, il disco viene ruotato a velocità nominale).</span><span class="sxs-lookup"><span data-stu-id="eb1db-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="eb1db-326">Per le unità nastro, questo è il tempo da inserire in un supporto per segnalare che è pronto per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb1db-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="eb1db-327">Si tratta in genere dell'area BOT del nastro.</span><span class="sxs-lookup"><span data-stu-id="eb1db-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="eb1db-328">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-329">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-330">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-332">Tempo, in millisecondi, per spostarsi dalla prima posizione sul supporto alla posizione più lontana rispetto al tempo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="eb1db-333">Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="eb1db-334">Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="eb1db-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="eb1db-335">(La fine di un nastro può essere il punto più distante fisicamente, ma ciò non è necessariamente vero). Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-336">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="eb1db-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-337">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-339">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="eb1db-340">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 512 per le unità disco rigido virtuali, variabile per le unità pass-through.</span><span class="sxs-lookup"><span data-stu-id="eb1db-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-341">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="eb1db-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-344">Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="eb1db-345">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="eb1db-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="eb1db-346">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 2 miliardi per le unità disco rigido virtuali, variabile per le unità pass-through.</span><span class="sxs-lookup"><span data-stu-id="eb1db-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-347">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-348">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-351">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="eb1db-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-352">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-354">Unità massime che è possibile utilizzare prima di pulire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="eb1db-355">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="eb1db-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-356">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="eb1db-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-357">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb1db-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-359">**True** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="eb1db-360">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-361">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="eb1db-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-362">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-364">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="eb1db-365">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 512.</span><span class="sxs-lookup"><span data-stu-id="eb1db-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-366">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="eb1db-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-367">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-369">Per un dispositivo che supporta supporti rimovibili, il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="eb1db-370">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="eb1db-371">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eb1db-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-375">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-375">The label by which the object is known.</span></span> <span data-ttu-id="eb1db-376">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-377">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="eb1db-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-378">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb1db-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-380">**True** se il dispositivo di accesso multimediale deve essere pulito. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="eb1db-381">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-382">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="eb1db-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-383">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb1db-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-385">Numero massimo di supporti singoli che possono essere supportati o inseriti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="eb1db-386">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="eb1db-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-387">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="eb1db-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-388">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-390">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="eb1db-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="eb1db-391">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eb1db-392">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eb1db-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eb1db-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="eb1db-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="eb1db-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="eb1db-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="eb1db-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="eb1db-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="eb1db-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="eb1db-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="eb1db-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="eb1db-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="eb1db-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="eb1db-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="eb1db-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="eb1db-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="eb1db-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="eb1db-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="eb1db-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="eb1db-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eb1db-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eb1db-412">)</span><span class="sxs-lookup"><span data-stu-id="eb1db-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb1db-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="eb1db-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-414">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-416">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-416">The current statuses of the object.</span></span> <span data-ttu-id="eb1db-417">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-418">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-419">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-421">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="eb1db-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="eb1db-422">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="eb1db-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="eb1db-423">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="eb1db-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-425">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="eb1db-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-427">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-428">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="eb1db-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-429">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-432">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="eb1db-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-433">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="eb1db-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-435">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="eb1db-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-437">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-438">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-439">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-440">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="eb1db-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-441">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-443">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="eb1db-443">Provides high level status information.</span></span> <span data-ttu-id="eb1db-444">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="eb1db-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="eb1db-445">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eb1db-446">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eb1db-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="eb1db-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="eb1db-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="eb1db-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="eb1db-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="eb1db-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="eb1db-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eb1db-453">)</span><span class="sxs-lookup"><span data-stu-id="eb1db-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb1db-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-455">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-457">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="eb1db-458">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="eb1db-459">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="eb1db-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="eb1db-460">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="eb1db-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="eb1db-461">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="eb1db-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="eb1db-462">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-463">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="eb1db-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-464">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-466">Sicurezza operativa definita per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-466">The operational security defined for the device.</span></span> <span data-ttu-id="eb1db-467">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 3 (nessuno).</span><span class="sxs-lookup"><span data-stu-id="eb1db-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-468">**Status**</span><span class="sxs-lookup"><span data-stu-id="eb1db-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-471">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-472">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="eb1db-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-473">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="eb1db-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-474">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-475">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="eb1db-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="eb1db-476">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="eb1db-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="eb1db-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-478">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-479">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-480">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-481">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb1db-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-482">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-483">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-484">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="eb1db-484">The scoping system's creation class name.</span></span> <span data-ttu-id="eb1db-485">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="eb1db-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-489">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="eb1db-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="eb1db-490">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="eb1db-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-491">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="eb1db-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-492">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-494">Per un dispositivo che supporta supporti rimovibili, la data e l'ora più recenti in cui il supporto è stato montato sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="eb1db-495">Per i dispositivi che accedono a supporti non rimovibili, ad esempio i dischi rigidi, questa proprietà non ha significato e non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="eb1db-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="eb1db-496">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-497">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="eb1db-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-498">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-500">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="eb1db-501">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su "null".</span><span class="sxs-lookup"><span data-stu-id="eb1db-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-502">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-503">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-505">Per un dispositivo che supporta supporti rimovibili, il tempo totale (in secondi) per cui sono stati montati i supporti per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb1db-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="eb1db-506">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="eb1db-507">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-508">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="eb1db-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-509">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-510">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-511">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-512">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="eb1db-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-513">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb1db-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-515">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="eb1db-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="eb1db-516">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb1db-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-517">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="eb1db-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-518">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb1db-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-520">Velocità di trasferimento dati prolungata, in KB al secondo, che il dispositivo è in grado di leggere e scrivere su un supporto.</span><span class="sxs-lookup"><span data-stu-id="eb1db-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="eb1db-521">Si tratta di una velocità dati continua e non elaborata.</span><span class="sxs-lookup"><span data-stu-id="eb1db-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="eb1db-522">Frequenze o tariffe massime che presuppongono che la compressione non venga segnalata in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb1db-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="eb1db-523">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-524">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="eb1db-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-525">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="eb1db-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-526">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-527">Unità relative all'uso in **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="eb1db-528">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="eb1db-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-529">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="eb1db-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-530">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-531">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-532">Numero corrente di unità utilizzate.</span><span class="sxs-lookup"><span data-stu-id="eb1db-532">The current number of units used.</span></span> <span data-ttu-id="eb1db-533">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb1db-534">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="eb1db-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb1db-535">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb1db-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb1db-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eb1db-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb1db-537">Tempo, in millisecondi, durante il quale è possibile leggere o scrivere un supporto nello scaricamento.</span><span class="sxs-lookup"><span data-stu-id="eb1db-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="eb1db-538">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="eb1db-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb1db-539">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb1db-539">Remarks</span></span>

<span data-ttu-id="eb1db-540">L'accesso alla **classe \_ DiskDrive di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="eb1db-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eb1db-541">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eb1db-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1db-542">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb1db-542">Requirements</span></span>



| <span data-ttu-id="eb1db-543">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb1db-543">Requirement</span></span> | <span data-ttu-id="eb1db-544">Valore</span><span class="sxs-lookup"><span data-stu-id="eb1db-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1db-545">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb1db-545">Minimum supported client</span></span><br/> | <span data-ttu-id="eb1db-546">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb1db-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eb1db-547">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb1db-547">Minimum supported server</span></span><br/> | <span data-ttu-id="eb1db-548">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb1db-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb1db-549">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb1db-549">Namespace</span></span><br/>                | <span data-ttu-id="eb1db-550">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb1db-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eb1db-551">MOF</span><span class="sxs-lookup"><span data-stu-id="eb1db-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb1db-552"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb1db-553">DLL</span><span class="sxs-lookup"><span data-stu-id="eb1db-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb1db-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb1db-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb1db-555">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb1db-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1db-556">**\_DiskDrive CIM**</span><span class="sxs-lookup"><span data-stu-id="eb1db-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="eb1db-557">**\_DiskDrive CIM**</span><span class="sxs-lookup"><span data-stu-id="eb1db-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="eb1db-558">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="eb1db-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

