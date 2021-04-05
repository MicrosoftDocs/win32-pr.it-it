---
description: Gestisce i file multimediali virtuali (file con estensione VHD, VHDX, ISO o VFD) per una macchina virtuale.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752370"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="d54fd-103">\_Classe MSVM servizio</span><span class="sxs-lookup"><span data-stu-id="d54fd-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d54fd-104">Gestisce i file multimediali virtuali (file con estensione VHD, VHDX, ISO o VFD) per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="d54fd-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d54fd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54fd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d54fd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="d54fd-107">Members</span><span class="sxs-lookup"><span data-stu-id="d54fd-107">Members</span></span>

<span data-ttu-id="d54fd-108">La **classe \_ servizio di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d54fd-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="d54fd-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d54fd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d54fd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d54fd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d54fd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d54fd-111">Methods</span></span>

<span data-ttu-id="d54fd-112">La **classe \_ servizio di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d54fd-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="d54fd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="d54fd-113">Method</span></span>                                                                                                           | <span data-ttu-id="d54fd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d54fd-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d54fd-115">**AttachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="d54fd-116">Connette un file di immagine del disco virtuale in modalità loopback.</span><span class="sxs-lookup"><span data-stu-id="d54fd-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="d54fd-117">**CompactVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="d54fd-118">Compatta un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="d54fd-119">**ConvertVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="d54fd-120">Converte un disco rigido virtuale esistente in un tipo o formato diverso.</span><span class="sxs-lookup"><span data-stu-id="d54fd-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="d54fd-121">**ConvertVirtualHardDiskToVHDSet**</span><span class="sxs-lookup"><span data-stu-id="d54fd-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="d54fd-122">Converte un file di disco rigido virtuale creando un nuovo file di set VHD insieme al disco rigido virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="d54fd-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d54fd-123">**CreateVirtualFloppyDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="d54fd-124">Consente di creare un file di disco floppy virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="d54fd-125">**CreateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="d54fd-126">Crea un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="d54fd-127">**DeleteVHDSnapshot**</span><span class="sxs-lookup"><span data-stu-id="d54fd-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="d54fd-128">Elimina una voce di snapshot VHD all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="d54fd-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="d54fd-129">**FindMountedStorageImageInstance**</span><span class="sxs-lookup"><span data-stu-id="d54fd-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="d54fd-130">Trova un \_ oggetto MSVM MountedStorageImage per un determinato percorso dell'immagine disco.</span><span class="sxs-lookup"><span data-stu-id="d54fd-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="d54fd-131">**GetVHDSetInformation**</span><span class="sxs-lookup"><span data-stu-id="d54fd-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="d54fd-132">Recupera le informazioni su un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="d54fd-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="d54fd-133">**GetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="d54fd-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="d54fd-134">Recupera le informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="d54fd-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="d54fd-135">**GetVirtualDiskChanges**</span><span class="sxs-lookup"><span data-stu-id="d54fd-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="d54fd-136">Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID di Rilevamento modifiche resiliente fornito o dall'ID dello snapshot VHDSet.</span><span class="sxs-lookup"><span data-stu-id="d54fd-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="d54fd-137">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="d54fd-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="d54fd-138">Recupera i dati di impostazione associati ai file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="d54fd-139">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="d54fd-140">Recupera lo stato dei file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="d54fd-141">**MergeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="d54fd-142">Unisce un disco rigido virtuale figlio in una catena di differenze con uno o più dischi rigidi virtuali padre nella catena.</span><span class="sxs-lookup"><span data-stu-id="d54fd-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="d54fd-143">**OptimizeVHDSet**</span><span class="sxs-lookup"><span data-stu-id="d54fd-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="d54fd-144">Ottimizza un file di set VHD in modo da utilizzare meno spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="d54fd-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="d54fd-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d54fd-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="d54fd-146">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="d54fd-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="d54fd-147">**ResizeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="d54fd-148">Ridimensiona un disco rigido virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="d54fd-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="d54fd-149">**SetParentVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="d54fd-150">Aggiorna l'elemento padre per i file di disco rigido virtuale foglia e figlio specificati.</span><span class="sxs-lookup"><span data-stu-id="d54fd-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="d54fd-151">**SetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="d54fd-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="d54fd-152">Modifica una voce di snapshot VHD all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="d54fd-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="d54fd-153">Se l'ID dello snapshot in questione esiste già, la voce di snapshot esistente verrà sovrascritta con la nuova voce.</span><span class="sxs-lookup"><span data-stu-id="d54fd-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="d54fd-154">In caso contrario, la nuova voce verrà aggiunta al file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="d54fd-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="d54fd-155">**SetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="d54fd-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="d54fd-156">Imposta un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="d54fd-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="d54fd-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="d54fd-158">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="d54fd-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="d54fd-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="d54fd-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="d54fd-160">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="d54fd-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="d54fd-161">**ValidatePersistentReservationSupport**</span><span class="sxs-lookup"><span data-stu-id="d54fd-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="d54fd-162">Verifica se un file system può supportare un disco rigido virtuale con prenotazioni permanenti abilitate.</span><span class="sxs-lookup"><span data-stu-id="d54fd-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="d54fd-163">**ValidateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d54fd-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="d54fd-164">Verifica se un'immagine del disco virtuale può essere aperta in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d54fd-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="d54fd-165">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d54fd-165">Properties</span></span>

<span data-ttu-id="d54fd-166">La **classe \_ servizio di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d54fd-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d54fd-167">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d54fd-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-168">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-170">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d54fd-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d54fd-171">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-172">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d54fd-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-175">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d54fd-175">A short description of the object.</span></span> <span data-ttu-id="d54fd-176">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Image Management Service".</span><span class="sxs-lookup"><span data-stu-id="d54fd-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d54fd-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-180">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="d54fd-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d54fd-181">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d54fd-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d54fd-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d54fd-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d54fd-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d54fd-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d54fd-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="d54fd-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="d54fd-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d54fd-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d54fd-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d54fd-190">)</span><span class="sxs-lookup"><span data-stu-id="d54fd-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d54fd-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d54fd-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-194">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="d54fd-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d54fd-195">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ servizio".</span><span class="sxs-lookup"><span data-stu-id="d54fd-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-196">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d54fd-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-199">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d54fd-199">A description of the object.</span></span> <span data-ttu-id="d54fd-200">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "fornisce la manutenzione delle immagini per Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="d54fd-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d54fd-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-204">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="d54fd-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d54fd-205">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d54fd-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d54fd-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d54fd-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="d54fd-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="d54fd-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="d54fd-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="d54fd-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="d54fd-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="d54fd-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d54fd-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d54fd-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d54fd-215">)</span><span class="sxs-lookup"><span data-stu-id="d54fd-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d54fd-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d54fd-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-219">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d54fd-219">A display name for the object.</span></span> <span data-ttu-id="d54fd-220">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Image Management Service".</span><span class="sxs-lookup"><span data-stu-id="d54fd-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d54fd-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-222">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-224">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d54fd-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d54fd-225">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="d54fd-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-227">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-229">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d54fd-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d54fd-230">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="d54fd-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d54fd-231">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="d54fd-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-233">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-235">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d54fd-235">The current health of the element.</span></span> <span data-ttu-id="d54fd-236">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d54fd-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d54fd-237">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d54fd-238">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="d54fd-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d54fd-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-240">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d54fd-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-242">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d54fd-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d54fd-243">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d54fd-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-247">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d54fd-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-248">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d54fd-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d54fd-249">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-250">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d54fd-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-253">Qualificatori: **chiave**, **override** ("Name"), **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d54fd-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-254">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d54fd-254">The label by which the object is known.</span></span> <span data-ttu-id="d54fd-255">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "vhdsvc".</span><span class="sxs-lookup"><span data-stu-id="d54fd-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d54fd-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-259">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d54fd-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d54fd-260">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d54fd-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d54fd-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d54fd-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d54fd-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d54fd-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="d54fd-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="d54fd-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="d54fd-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="d54fd-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="d54fd-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="d54fd-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="d54fd-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="d54fd-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="d54fd-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="d54fd-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="d54fd-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="d54fd-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="d54fd-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="d54fd-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="d54fd-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d54fd-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d54fd-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d54fd-281">)</span><span class="sxs-lookup"><span data-stu-id="d54fd-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d54fd-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d54fd-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-283">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-285">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d54fd-285">The current status of the object.</span></span> <span data-ttu-id="d54fd-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d54fd-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-290">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="d54fd-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d54fd-291">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="d54fd-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d54fd-292">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="d54fd-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-296">Stringa che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="d54fd-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="d54fd-297">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-298">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="d54fd-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-301">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="d54fd-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="d54fd-302">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d54fd-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="d54fd-303">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-304">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d54fd-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-305">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-307">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="d54fd-307">Provides high level status information.</span></span> <span data-ttu-id="d54fd-308">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d54fd-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d54fd-309">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d54fd-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d54fd-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d54fd-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d54fd-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d54fd-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="d54fd-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="d54fd-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d54fd-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d54fd-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d54fd-317">)</span><span class="sxs-lookup"><span data-stu-id="d54fd-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d54fd-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-319">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-321">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d54fd-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="d54fd-322">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d54fd-323">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d54fd-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d54fd-324">Una particolare istanza di **EnabledLogicalElement** potrebbe non supportare **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="d54fd-325">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d54fd-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d54fd-326">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d54fd-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-327">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="d54fd-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-328">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d54fd-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-330">Indica se il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="d54fd-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="d54fd-331">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-332">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="d54fd-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-335">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="d54fd-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="d54fd-336">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="d54fd-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d54fd-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d54fd-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-342">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d54fd-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-344">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d54fd-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d54fd-345">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d54fd-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d54fd-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-349">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d54fd-349">The scoping system's creation class name.</span></span> <span data-ttu-id="d54fd-350">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="d54fd-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d54fd-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d54fd-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-354">Nome del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="d54fd-354">The name of the hosting computer system.</span></span> <span data-ttu-id="d54fd-355">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d54fd-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d54fd-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-357">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d54fd-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-359">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d54fd-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d54fd-360">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d54fd-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d54fd-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d54fd-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d54fd-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d54fd-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d54fd-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d54fd-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d54fd-364">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d54fd-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d54fd-365">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d54fd-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d54fd-366">Commenti</span><span class="sxs-lookup"><span data-stu-id="d54fd-366">Remarks</span></span>

<span data-ttu-id="d54fd-367">L'accesso alla **classe \_ servizio di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d54fd-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d54fd-368">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d54fd-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d54fd-369">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d54fd-369">Requirements</span></span>



| <span data-ttu-id="d54fd-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="d54fd-370">Requirement</span></span> | <span data-ttu-id="d54fd-371">Valore</span><span class="sxs-lookup"><span data-stu-id="d54fd-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d54fd-372">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d54fd-372">Minimum supported client</span></span><br/> | <span data-ttu-id="d54fd-373">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d54fd-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d54fd-374">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d54fd-374">Minimum supported server</span></span><br/> | <span data-ttu-id="d54fd-375">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d54fd-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d54fd-376">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d54fd-376">Namespace</span></span><br/>                | <span data-ttu-id="d54fd-377">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d54fd-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d54fd-378">MOF</span><span class="sxs-lookup"><span data-stu-id="d54fd-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d54fd-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d54fd-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d54fd-380">DLL</span><span class="sxs-lookup"><span data-stu-id="d54fd-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d54fd-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d54fd-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d54fd-382">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d54fd-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54fd-383">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="d54fd-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="d54fd-384">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="d54fd-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="d54fd-385">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d54fd-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

