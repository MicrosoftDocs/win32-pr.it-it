---
description: Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento della raccolta.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319512"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="41b16-103">\_Classe MSVM CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="41b16-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="41b16-104">Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="41b16-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="41b16-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="41b16-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b16-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41b16-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="41b16-107">Members</span><span class="sxs-lookup"><span data-stu-id="41b16-107">Members</span></span>

<span data-ttu-id="41b16-108">La **classe \_ CollectionReferencePointExportJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="41b16-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="41b16-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="41b16-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41b16-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="41b16-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41b16-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="41b16-111">Methods</span></span>

<span data-ttu-id="41b16-112">La **classe \_ CollectionReferencePointExportJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="41b16-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="41b16-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="41b16-113">Method</span></span>                                                                                  | <span data-ttu-id="41b16-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41b16-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="41b16-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="41b16-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="41b16-116">Recupera un errore.</span><span class="sxs-lookup"><span data-stu-id="41b16-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="41b16-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="41b16-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="41b16-118">Recupera informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="41b16-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="41b16-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="41b16-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="41b16-120">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="41b16-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="41b16-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="41b16-121">Properties</span></span>

<span data-ttu-id="41b16-122">La **classe \_ CollectionReferencePointExportJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="41b16-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41b16-123">**BaseReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="41b16-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="41b16-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-126">GUID del punto di riferimento della raccolta usato come base in exportoperation.</span><span class="sxs-lookup"><span data-stu-id="41b16-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-127">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="41b16-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="41b16-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-130">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="41b16-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="41b16-131">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="41b16-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-132">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="41b16-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="41b16-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-135">GUID del gruppo di macchine virtuali per cui i file di log wereexported.</span><span class="sxs-lookup"><span data-stu-id="41b16-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="41b16-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="41b16-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41b16-139">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="41b16-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="41b16-140">Contiene una descrizione di riepilogo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="41b16-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-141">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="41b16-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="41b16-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-144">Percorso di esportazione.</span><span class="sxs-lookup"><span data-stu-id="41b16-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-145">**ExportedConfigFilePaths**</span><span class="sxs-lookup"><span data-stu-id="41b16-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-146">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-148">Percorso del file di configurazione della macchina virtuale esportato.</span><span class="sxs-lookup"><span data-stu-id="41b16-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-149">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="41b16-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-150">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-152">ID istanza dei dischi virtuali per i quali sono stati esportati i file di log.</span><span class="sxs-lookup"><span data-stu-id="41b16-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-153">**ExportedGuestStateFilePaths**</span><span class="sxs-lookup"><span data-stu-id="41b16-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-154">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-156">Percorso del file di stato guest della macchina virtuale esportato.</span><span class="sxs-lookup"><span data-stu-id="41b16-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="41b16-157">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="41b16-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="41b16-158">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="41b16-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-159">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-161">Percorsi dei file di log esportati.</span><span class="sxs-lookup"><span data-stu-id="41b16-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-162">**ExportedRuntimeFilePaths**</span><span class="sxs-lookup"><span data-stu-id="41b16-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-163">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-165">Percorso del file di stato di runtime della macchina virtuale esportato.</span><span class="sxs-lookup"><span data-stu-id="41b16-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-166">**ReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="41b16-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="41b16-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41b16-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-169">GUID del punto di riferimento della raccolta che viene esportato.</span><span class="sxs-lookup"><span data-stu-id="41b16-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="41b16-170">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="41b16-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41b16-171">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="41b16-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41b16-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="41b16-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41b16-173">GUID delle macchine virtuali per cui è stata eseguita l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="41b16-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41b16-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41b16-174">Requirements</span></span>



| <span data-ttu-id="41b16-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b16-175">Requirement</span></span> | <span data-ttu-id="41b16-176">Valore</span><span class="sxs-lookup"><span data-stu-id="41b16-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b16-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b16-177">Minimum supported client</span></span><br/> | <span data-ttu-id="41b16-178">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="41b16-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41b16-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b16-179">Minimum supported server</span></span><br/> | <span data-ttu-id="41b16-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="41b16-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="41b16-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41b16-181">Namespace</span></span><br/>                | <span data-ttu-id="41b16-182">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="41b16-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="41b16-183">MOF</span><span class="sxs-lookup"><span data-stu-id="41b16-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41b16-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41b16-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41b16-185">DLL</span><span class="sxs-lookup"><span data-stu-id="41b16-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b16-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41b16-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41b16-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41b16-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b16-188">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="41b16-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

