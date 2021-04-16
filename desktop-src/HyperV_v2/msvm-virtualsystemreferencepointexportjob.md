---
description: Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento del sistema virtuale.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530451"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="4cfd7-103">\_Classe MSVM VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="4cfd7-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="4cfd7-104">Questa classe rappresenta un processo dell'operazione di esportazione del punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="4cfd7-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfd7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cfd7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="4cfd7-107">Members</span><span class="sxs-lookup"><span data-stu-id="4cfd7-107">Members</span></span>

<span data-ttu-id="4cfd7-108">La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4cfd7-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="4cfd7-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4cfd7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4cfd7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4cfd7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4cfd7-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4cfd7-111">Methods</span></span>

<span data-ttu-id="4cfd7-112">La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="4cfd7-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="4cfd7-113">Method</span></span>                                                                                     | <span data-ttu-id="4cfd7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cfd7-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="4cfd7-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="4cfd7-116">Recupera l'errore.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="4cfd7-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="4cfd7-118">Recupera informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="4cfd7-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="4cfd7-120">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="4cfd7-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4cfd7-121">Properties</span></span>

<span data-ttu-id="4cfd7-122">La **classe \_ VirtualSystemReferencePointExportJob di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cfd7-123">**BaseReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-126">GUID del punto di riferimento utilizzato come base nell'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-127">**Annullabili**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-130">Indica se il processo può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="4cfd7-131">Il valore di questa proprietà non garantisce che una richiesta di annullamento del processo avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-135">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ processo CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="4cfd7-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-136">Contiene una descrizione di riepilogo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-137">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-140">Percorso di esportazione.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-141">**ExportedConfigFilePath**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-144">Percorso del file di configurazione esportato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-145">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-146">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-148">ID istanza dei dischi virtuali per i quali sono stati esportati i file di log.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-149">**ExportedGuestStateFilePath**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-152">Percorso del file di stato Guest esportato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="4cfd7-153">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4cfd7-154">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-155">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-157">Percorsi dei file di log esportati.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-158">**ExportedRuntimeFilePath**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-161">Percorso del file di stato di runtime esportato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-162">**ReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-165">GUID del punto di riferimento che viene esportato.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="4cfd7-166">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cfd7-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cfd7-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4cfd7-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cfd7-169">GUID della macchina virtuale per cui sono stati esportati i file di log.</span><span class="sxs-lookup"><span data-stu-id="4cfd7-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4cfd7-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cfd7-170">Requirements</span></span>



| <span data-ttu-id="4cfd7-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfd7-171">Requirement</span></span> | <span data-ttu-id="4cfd7-172">Valore</span><span class="sxs-lookup"><span data-stu-id="4cfd7-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfd7-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cfd7-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4cfd7-174">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cfd7-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4cfd7-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cfd7-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4cfd7-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4cfd7-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4cfd7-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4cfd7-177">Namespace</span></span><br/>                | <span data-ttu-id="4cfd7-178">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4cfd7-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4cfd7-179">MOF</span><span class="sxs-lookup"><span data-stu-id="4cfd7-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cfd7-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cfd7-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cfd7-181">DLL</span><span class="sxs-lookup"><span data-stu-id="4cfd7-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cfd7-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4cfd7-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4cfd7-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cfd7-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfd7-184">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="4cfd7-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

