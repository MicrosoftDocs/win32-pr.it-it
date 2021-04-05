---
description: Rappresenta un'unità DVD all'interno di una macchina virtuale.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884598"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="74181-103">\_Classe MSVM DVDDrive</span><span class="sxs-lookup"><span data-stu-id="74181-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="74181-104">Rappresenta un'unità DVD all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74181-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="74181-105">Questa unità DVD può essere un dispositivo pass-through (se un disco rigido fisico è stato collegato alla macchina virtuale) o sintetico e popolato con file multimediali ISO.</span><span class="sxs-lookup"><span data-stu-id="74181-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="74181-106">Poiché le unità DVD virtuali e fisiche possono essere aggiunte e rimosse dalla macchina virtuale, sono presenti due pool di risorse associati a questa classe, uno per le unità DVD pass-through e l'altro per le unità DVD virtuali.</span><span class="sxs-lookup"><span data-stu-id="74181-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="74181-107">Le unità DVD possono essere aggiunte o rimosse solo se la macchina virtuale è offline.</span><span class="sxs-lookup"><span data-stu-id="74181-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="74181-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="74181-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74181-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74181-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
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
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="74181-110">Members</span><span class="sxs-lookup"><span data-stu-id="74181-110">Members</span></span>

<span data-ttu-id="74181-111">La **classe \_ DVDDrive di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="74181-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="74181-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="74181-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="74181-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74181-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74181-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="74181-114">Methods</span></span>

<span data-ttu-id="74181-115">La **classe \_ DVDDrive di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="74181-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="74181-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="74181-116">Method</span></span>                                                         | <span data-ttu-id="74181-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74181-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="74181-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="74181-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="74181-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="74181-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="74181-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="74181-121">Blocca o rilascia i supporti.</span><span class="sxs-lookup"><span data-stu-id="74181-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="74181-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="74181-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="74181-123">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74181-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="74181-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="74181-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="74181-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="74181-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="74181-127">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="74181-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="74181-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="74181-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="74181-129">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="74181-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="74181-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="74181-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="74181-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74181-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="74181-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="74181-133">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74181-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="74181-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="74181-135">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="74181-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="74181-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74181-136">Properties</span></span>

<span data-ttu-id="74181-137">La **classe \_ DVDDrive di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="74181-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74181-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="74181-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-139">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-141">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="74181-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="74181-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="74181-143">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="74181-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-146">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-146">The primary availability and status of the device.</span></span> <span data-ttu-id="74181-147">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="74181-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="74181-148">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="74181-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-149">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-151">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="74181-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="74181-152">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="74181-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="74181-153">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="74181-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="74181-154">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="74181-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="74181-155">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74181-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="74181-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="74181-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-157">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74181-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-159">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="74181-159">The capabilities of the media access device.</span></span> <span data-ttu-id="74181-160">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="74181-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="74181-161">Valore</span><span class="sxs-lookup"><span data-stu-id="74181-161">Value</span></span>                                                                             | <span data-ttu-id="74181-162">Significato</span><span class="sxs-lookup"><span data-stu-id="74181-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74181-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="74181-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="74181-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="74181-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="74181-165">La voce corrispondente in **CapabilityDescriptions** è "accesso casuale".</span><span class="sxs-lookup"><span data-stu-id="74181-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="74181-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="74181-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="74181-167">La voce corrispondente in **CapabilityDescriptions** è "supporta supporti rimovibili".</span><span class="sxs-lookup"><span data-stu-id="74181-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74181-168">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74181-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-169">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74181-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-171">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nella matrice di proprietà delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="74181-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="74181-172">Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **capabilities** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="74181-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="74181-173">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-174">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="74181-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-177">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74181-177">A short description of the object.</span></span> <span data-ttu-id="74181-178">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74181-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-179">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="74181-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-182">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="74181-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="74181-183">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="74181-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74181-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="74181-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-188">Stringa che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="74181-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="74181-189">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="74181-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="74181-190">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="74181-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="74181-191">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="74181-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="74181-192">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="74181-193">"Non compresso"</span><span class="sxs-lookup"><span data-stu-id="74181-193">"Not Compressed"</span></span>

<span data-ttu-id="74181-194">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="74181-194">"Unknown"</span></span>

<span data-ttu-id="74181-195">Compressi</span><span class="sxs-lookup"><span data-stu-id="74181-195">"Compressed"</span></span>

<span data-ttu-id="74181-196">"Non compresso"</span><span class="sxs-lookup"><span data-stu-id="74181-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="74181-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74181-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-200">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="74181-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="74181-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="74181-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-202">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="74181-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-205">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="74181-206">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-207">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="74181-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-210">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="74181-210">A description of the object.</span></span> <span data-ttu-id="74181-211">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74181-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="74181-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-215">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="74181-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="74181-216">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="74181-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74181-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="74181-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-221">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="74181-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="74181-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="74181-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-225">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74181-225">A display name for the object.</span></span> <span data-ttu-id="74181-226">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74181-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="74181-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-228">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-230">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="74181-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="74181-231">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74181-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="74181-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="74181-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-233">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-235">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="74181-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="74181-236">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="74181-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="74181-237">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74181-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="74181-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="74181-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="74181-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74181-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-241">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="74181-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="74181-242">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="74181-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-246">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="74181-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="74181-247">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-248">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="74181-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-251">Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="74181-252">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-253">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="74181-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-254">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-256">Formati CD e DVD supportati da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="74181-257">Questa proprietà viene ereditata da [**CIM \_ DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74181-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="74181-258">Questa matrice contiene i valori seguenti per ISO.</span><span class="sxs-lookup"><span data-stu-id="74181-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="74181-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="74181-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="74181-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="74181-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="74181-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="74181-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="74181-262">Questa matrice contiene i valori seguenti per il pass-through fisico.</span><span class="sxs-lookup"><span data-stu-id="74181-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="74181-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74181-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74181-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74181-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74181-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="74181-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="74181-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="74181-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="74181-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="74181-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="74181-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD registrabile** (19)</span><span class="sxs-lookup"><span data-stu-id="74181-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="74181-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="74181-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="74181-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="74181-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="74181-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="74181-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="74181-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="74181-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="74181-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-video** (26)</span><span class="sxs-lookup"><span data-stu-id="74181-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="74181-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="74181-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="74181-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="74181-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="74181-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="74181-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="74181-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="74181-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="74181-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD registrabile** (36)</span><span class="sxs-lookup"><span data-stu-id="74181-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="74181-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="74181-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="74181-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="74181-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="74181-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="74181-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="74181-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="74181-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="74181-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="74181-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="74181-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="74181-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="74181-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="74181-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-286">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-288">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="74181-288">The current health of the element.</span></span> <span data-ttu-id="74181-289">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="74181-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="74181-290">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="74181-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="74181-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74181-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-293">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74181-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-295">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="74181-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="74181-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="74181-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74181-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="74181-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-298">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74181-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74181-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-300">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74181-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="74181-301">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74181-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74181-305">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="74181-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="74181-306">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="74181-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="74181-307">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74181-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-308">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="74181-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-309">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74181-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74181-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-311">Data e ora dell'ultima pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="74181-312">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="74181-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-314">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74181-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74181-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-316">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="74181-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="74181-317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-318">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="74181-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-319">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-321">Tempo, in millisecondi, da "Load" per poter leggere o scrivere un supporto.</span><span class="sxs-lookup"><span data-stu-id="74181-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="74181-322">Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per la lettura/scrittura (ovvero, il disco viene ruotato a velocità nominale).</span><span class="sxs-lookup"><span data-stu-id="74181-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="74181-323">Per le unità nastro, questo è il tempo da inserire in un supporto per segnalare che è pronto per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74181-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="74181-324">Si tratta in genere dell'area BOT del nastro.</span><span class="sxs-lookup"><span data-stu-id="74181-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="74181-325">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-326">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="74181-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-327">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-329">Tempo, in millisecondi, per spostarsi dalla prima posizione sul supporto alla posizione più lontana rispetto al tempo.</span><span class="sxs-lookup"><span data-stu-id="74181-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="74181-330">Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo.</span><span class="sxs-lookup"><span data-stu-id="74181-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="74181-331">Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="74181-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="74181-332">(La fine di un nastro può essere il punto più distante fisicamente, ma ciò non è necessariamente vero). Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-333">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="74181-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-334">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-336">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="74181-337">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-338">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="74181-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-339">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-341">Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="74181-342">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="74181-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="74181-343">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-344">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="74181-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-345">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-347">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="74181-347">This property has been deprecated.</span></span> <span data-ttu-id="74181-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-349">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="74181-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-350">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-352">Unità massime che è possibile utilizzare prima di pulire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="74181-353">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-354">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="74181-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-355">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="74181-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74181-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-357">**True** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="74181-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="74181-358">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-359">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="74181-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-360">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-362">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="74181-363">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-364">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="74181-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-365">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-367">Per un dispositivo che supporta supporti rimovibili, il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="74181-368">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="74181-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="74181-369">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-370">**Nome**</span><span class="sxs-lookup"><span data-stu-id="74181-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-371">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-373">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="74181-373">The label by which the object is known.</span></span> <span data-ttu-id="74181-374">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="74181-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="74181-375">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="74181-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-376">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="74181-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74181-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-378">**True** se il dispositivo di accesso multimediale deve essere pulito. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="74181-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="74181-379">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-380">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="74181-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-381">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74181-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74181-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-383">Numero massimo di supporti singoli che possono essere supportati o inseriti.</span><span class="sxs-lookup"><span data-stu-id="74181-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="74181-384">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-385">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="74181-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-386">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-388">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="74181-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="74181-389">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="74181-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74181-390">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="74181-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-392">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-394">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74181-394">The current statuses of the object.</span></span> <span data-ttu-id="74181-395">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-396">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="74181-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-397">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-399">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="74181-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="74181-400">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="74181-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="74181-401">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74181-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="74181-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="74181-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-403">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74181-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-405">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="74181-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="74181-406">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="74181-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74181-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="74181-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-408">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-410">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-410">The power management capabilities of the device.</span></span> <span data-ttu-id="74181-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-412">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="74181-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-413">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="74181-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74181-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-415">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="74181-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="74181-416">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-417">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="74181-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-418">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-420">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="74181-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="74181-421">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-422">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="74181-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-423">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-425">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="74181-425">Provides high level status information.</span></span> <span data-ttu-id="74181-426">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="74181-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="74181-427">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="74181-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74181-428">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="74181-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-430">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-432">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="74181-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="74181-433">Lo stato effettivo dell'elemento è rappresentato dalla proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="74181-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="74181-434">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="74181-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="74181-435">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="74181-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="74181-436">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="74181-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="74181-437">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="74181-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="74181-438">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="74181-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-439">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-441">Sicurezza operativa definita per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-441">The operational security defined for the device.</span></span> <span data-ttu-id="74181-442">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-443">**Status**</span><span class="sxs-lookup"><span data-stu-id="74181-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-444">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-446">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74181-446">The current status of the object.</span></span> <span data-ttu-id="74181-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-448">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74181-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-449">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74181-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74181-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-451">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="74181-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="74181-452">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="74181-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74181-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="74181-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-456">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="74181-456">The current state of the logical device.</span></span> <span data-ttu-id="74181-457">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74181-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-459">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-461">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="74181-461">The scoping system's creation class name.</span></span> <span data-ttu-id="74181-462">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="74181-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="74181-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-464">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-466">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="74181-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="74181-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="74181-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-468">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="74181-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-469">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74181-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74181-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-471">Per un dispositivo che supporta supporti rimovibili, la data e l'ora più recenti in cui il supporto è stato montato sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="74181-472">Per i dispositivi che accedono a supporti non rimovibili, ad esempio i dischi rigidi, questa proprietà non ha significato e non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="74181-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="74181-473">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-474">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="74181-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-475">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74181-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74181-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-477">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="74181-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="74181-478">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="74181-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74181-479">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="74181-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-480">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-482">Per un dispositivo che supporta supporti rimovibili, il tempo totale (in secondi) per cui sono stati montati i supporti per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74181-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="74181-483">Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="74181-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="74181-484">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="74181-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-486">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-488">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="74181-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="74181-489">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="74181-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-491">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74181-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74181-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-493">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="74181-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="74181-494">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="74181-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74181-495">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="74181-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-496">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74181-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74181-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-498">Velocità di trasferimento dati prolungata, in KB al secondo, che il dispositivo può leggere e scrivere su un supporto.</span><span class="sxs-lookup"><span data-stu-id="74181-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="74181-499">Si tratta di una velocità dati continua e non elaborata.</span><span class="sxs-lookup"><span data-stu-id="74181-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="74181-500">Frequenze o tariffe massime che presuppongono che la compressione non venga segnalata in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="74181-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="74181-501">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-502">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="74181-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-503">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74181-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74181-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-505">Unità relative all'uso in **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="74181-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="74181-506">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-507">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="74181-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-508">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-509">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-510">Numero corrente di unità utilizzate.</span><span class="sxs-lookup"><span data-stu-id="74181-510">The current number of units used.</span></span> <span data-ttu-id="74181-511">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="74181-512">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="74181-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74181-513">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74181-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74181-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74181-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74181-515">Tempo, in millisecondi, durante il quale è possibile leggere o scrivere un supporto nel relativo ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="74181-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="74181-516">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="74181-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74181-517">Commenti</span><span class="sxs-lookup"><span data-stu-id="74181-517">Remarks</span></span>

<span data-ttu-id="74181-518">L'accesso alla **classe \_ DVDDrive di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="74181-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="74181-519">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="74181-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="74181-520">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74181-520">Requirements</span></span>



| <span data-ttu-id="74181-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="74181-521">Requirement</span></span> | <span data-ttu-id="74181-522">Valore</span><span class="sxs-lookup"><span data-stu-id="74181-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74181-523">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74181-523">Minimum supported client</span></span><br/> | <span data-ttu-id="74181-524">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="74181-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74181-525">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74181-525">Minimum supported server</span></span><br/> | <span data-ttu-id="74181-526">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="74181-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74181-527">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74181-527">Namespace</span></span><br/>                | <span data-ttu-id="74181-528">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="74181-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74181-529">MOF</span><span class="sxs-lookup"><span data-stu-id="74181-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74181-530"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74181-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74181-531">DLL</span><span class="sxs-lookup"><span data-stu-id="74181-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74181-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74181-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74181-533">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74181-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74181-534">**\_DVDDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="74181-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="74181-535">[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74181-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74181-536">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="74181-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

