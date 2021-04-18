---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo ExportSystemDefinition della \_ classe VirtualSystemManagementService di MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306016"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="8924e-103">\_Classe MSVM VirtualSystemExportSettingData</span><span class="sxs-lookup"><span data-stu-id="8924e-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="8924e-104">Fornisce informazioni aggiuntive da utilizzare con il metodo [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della classe [**\_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8924e-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="8924e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8924e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8924e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8924e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="8924e-107">Members</span><span class="sxs-lookup"><span data-stu-id="8924e-107">Members</span></span>

<span data-ttu-id="8924e-108">La **classe \_ VirtualSystemExportSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8924e-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8924e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8924e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8924e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8924e-110">Properties</span></span>

<span data-ttu-id="8924e-111">La **classe \_ VirtualSystemExportSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8924e-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8924e-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="8924e-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8924e-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-115">Indica l'intenzione di utilizzare i set di backup esportati.</span><span class="sxs-lookup"><span data-stu-id="8924e-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-116">Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8924e-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="8924e-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span><span class="sxs-lookup"><span data-stu-id="8924e-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-118">Tutti i set di backup completi e differenziali esportati verranno conservati così come sono.</span><span class="sxs-lookup"><span data-stu-id="8924e-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="8924e-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span><span class="sxs-lookup"><span data-stu-id="8924e-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-120">I set di backup completi e differenziali esportati verranno uniti per sintetizzare set di backup completi.</span><span class="sxs-lookup"><span data-stu-id="8924e-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8924e-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8924e-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8924e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8924e-124">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8924e-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8924e-125">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8924e-125">A short description of the object.</span></span> <span data-ttu-id="8924e-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8924e-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8924e-127">**CaptureLiveState**</span><span class="sxs-lookup"><span data-stu-id="8924e-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-128">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8924e-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-130">Indica lo stato da acquisire se la destinazione dell'esportazione è una macchina virtuale in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8924e-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="8924e-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span><span class="sxs-lookup"><span data-stu-id="8924e-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-132">Nessun file di stato salvato verrà esportato per la macchina virtuale in esecuzione, inserendolo in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="8924e-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="8924e-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span><span class="sxs-lookup"><span data-stu-id="8924e-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-134">I file di stato salvati per la macchina virtuale in esecuzione verranno esportati insieme alla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="8924e-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span><span class="sxs-lookup"><span data-stu-id="8924e-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-136">Viene esportato lo stato coerente con l'applicazione della macchina virtuale in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8924e-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-137">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8924e-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8924e-138">**CopySnapshotConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8924e-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-139">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8924e-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-141">Indica quali snapshot devono essere esportati con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="8924e-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span><span class="sxs-lookup"><span data-stu-id="8924e-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-143">Tutti gli snapshot verranno esportati con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="8924e-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span><span class="sxs-lookup"><span data-stu-id="8924e-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-145">Non verranno esportati snapshot con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="8924e-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span><span class="sxs-lookup"><span data-stu-id="8924e-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-147">Gli snapshot identificati dalla proprietà **SnapshotVirtualSystem** verranno esportati con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="8924e-148">Le proprietà **CopyVmStorage** e **CopyVmRuntimeInformation** vengono ignorate, le informazioni sull'archiviazione e la fase di esecuzione vengono esportate con la macchina virtuale e tutti i dischi differenze VHD verranno uniti in un nuovo disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="8924e-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span><span class="sxs-lookup"><span data-stu-id="8924e-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8924e-150">Lo snapshot identificato dalla proprietà **SnapshotVirtualSystem** verrà esportato allo scopo di eseguire il backup della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="8924e-151">La configurazione esportata userà l'ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-152">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8924e-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8924e-153">**CopyVmRuntimeInformation**</span><span class="sxs-lookup"><span data-stu-id="8924e-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8924e-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-156">Indica se le informazioni di runtime della macchina virtuale verranno copiate quando viene esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="8924e-157">Valore</span><span class="sxs-lookup"><span data-stu-id="8924e-157">Value</span></span>                                                                                | <span data-ttu-id="8924e-158">Significato</span><span class="sxs-lookup"><span data-stu-id="8924e-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8924e-159"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="8924e-160">Verranno copiate le informazioni sulla fase di esecuzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="8924e-161"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="8924e-162">Le informazioni di run-time della macchina virtuale non verranno copiate.</span><span class="sxs-lookup"><span data-stu-id="8924e-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8924e-163">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="8924e-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-164">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8924e-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-166">Indica se lo spazio di archiviazione della macchina virtuale verrà copiato quando viene esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="8924e-167">Valore</span><span class="sxs-lookup"><span data-stu-id="8924e-167">Value</span></span>                                                                                | <span data-ttu-id="8924e-168">Significato</span><span class="sxs-lookup"><span data-stu-id="8924e-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="8924e-169"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="8924e-170">Verrà copiato lo spazio di archiviazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="8924e-171"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="8924e-172">L'archiviazione della macchina virtuale non verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="8924e-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8924e-173">**CreateVmExportSubdirectory**</span><span class="sxs-lookup"><span data-stu-id="8924e-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8924e-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-176">Indica se verrà creata una sottodirectory con il nome della macchina virtuale quando viene esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="8924e-177">Valore</span><span class="sxs-lookup"><span data-stu-id="8924e-177">Value</span></span>                                                                                | <span data-ttu-id="8924e-178">Significato</span><span class="sxs-lookup"><span data-stu-id="8924e-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="8924e-179"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="8924e-180">Verrà creata una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="8924e-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="8924e-181"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="8924e-182">Non verrà creata una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="8924e-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8924e-183">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8924e-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8924e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8924e-186">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="8924e-186">A description of the object.</span></span> <span data-ttu-id="8924e-187">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8924e-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8924e-188">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="8924e-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-191">Base per l'esportazione differenziale.</span><span class="sxs-lookup"><span data-stu-id="8924e-191">Base for differential export.</span></span> <span data-ttu-id="8924e-192">Si tratta del percorso di un'istanza di [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento o il percorso di un'istanza di [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da utilizzare come base per l'esportazione differenziale.</span><span class="sxs-lookup"><span data-stu-id="8924e-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="8924e-193">Se la proprietà **CopySnapshotConfiguration** non è impostata su 3 (**ExportOneSnapshotForBackup**), questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8924e-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-194">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8924e-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8924e-195">**DisableDifferentialOfIgnoredStorage**</span><span class="sxs-lookup"><span data-stu-id="8924e-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8924e-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-198">Indica se i dischi differenze verranno creati o meno per l'archiviazione ignorata durante l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="8924e-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="8924e-199">Per impostazione predefinita, questo valore è impostato su false, il che significa che i dischi differenze vengono creati per l'archiviazione che non verrà copiata nella destinazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="8924e-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-200">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="8924e-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8924e-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8924e-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8924e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8924e-204">Nome visualizzato per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="8924e-204">The display name for this instance.</span></span> <span data-ttu-id="8924e-205">Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="8924e-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="8924e-206">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8924e-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8924e-207">**ExcludedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="8924e-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-208">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8924e-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8924e-209">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-210">Matrice di ID di istanza [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) che rappresentano i dischi rigidi virtuali che devono essere esclusi dall'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="8924e-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="8924e-211">Se almeno uno degli ID specificati non è un disco rigido virtuale collegato valido, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8924e-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="8924e-212">I dischi rigidi virtuali a cui fa riferimento questa proprietà possono provenire dalla macchina virtuale e/o da uno qualsiasi dei relativi snapshot.</span><span class="sxs-lookup"><span data-stu-id="8924e-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="8924e-213">L'esclusione di dischi rigidi virtuali non è supportata quando la proprietà **CopySnapshotConfiguration** è impostata su 0 (ExportAllSnapshots).</span><span class="sxs-lookup"><span data-stu-id="8924e-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="8924e-214">Si noti che l'ID dell'istanza di RASD per i dischi rigidi virtuali rappresenta il percorso a cui sono collegati ed escludendo questo ID esclude tutti i dischi rigidi virtuali collegati in tale posizione nell'albero degli snapshot della macchina virtuale, indipendentemente dal fatto che siano effettivamente una catena di dischi rigidi virtuali valida.</span><span class="sxs-lookup"><span data-stu-id="8924e-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-215">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="8924e-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8924e-216">**ExportForLiveMigration**</span><span class="sxs-lookup"><span data-stu-id="8924e-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-217">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8924e-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-218">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-219">Indica se la macchina virtuale esportata deve essere utilizzata nella migrazione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="8924e-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="8924e-220">Aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8924e-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8924e-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8924e-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8924e-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8924e-224">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="8924e-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8924e-225">All'interno dell'ambito dello spazio dei nomi di creazione di istanze, in modo opaco e univoco identifica un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="8924e-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8924e-226">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8924e-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8924e-227">**SnapshotVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="8924e-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8924e-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8924e-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8924e-229">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8924e-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8924e-230">Percorso di un'istanza di [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da esportare con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8924e-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="8924e-231">Se la proprietà **CopySnapshotConfiguration** non è impostata su 2 (ExportOneSnapshot), questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8924e-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8924e-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="8924e-232">Remarks</span></span>

<span data-ttu-id="8924e-233">L'accesso alla **classe \_ VirtualSystemExportSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="8924e-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8924e-234">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8924e-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8924e-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8924e-235">Requirements</span></span>



| <span data-ttu-id="8924e-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="8924e-236">Requirement</span></span> | <span data-ttu-id="8924e-237">Valore</span><span class="sxs-lookup"><span data-stu-id="8924e-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8924e-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8924e-238">Minimum supported client</span></span><br/> | <span data-ttu-id="8924e-239">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8924e-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8924e-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8924e-240">Minimum supported server</span></span><br/> | <span data-ttu-id="8924e-241">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8924e-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8924e-242">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8924e-242">Namespace</span></span><br/>                | <span data-ttu-id="8924e-243">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8924e-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8924e-244">MOF</span><span class="sxs-lookup"><span data-stu-id="8924e-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8924e-245"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8924e-246">DLL</span><span class="sxs-lookup"><span data-stu-id="8924e-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8924e-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8924e-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8924e-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8924e-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8924e-249">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8924e-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="8924e-250">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="8924e-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="8924e-251">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="8924e-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

