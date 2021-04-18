---
description: Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID di Rilevamento modifiche resiliente fornito o dall'ID dello snapshot VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Metodo GetVirtualDiskChanges della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307893"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0cf61-103">Metodo GetVirtualDiskChanges della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="0cf61-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0cf61-104">Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID di Rilevamento modifiche resiliente fornito o dall'ID dello snapshot VHDSet.</span><span class="sxs-lookup"><span data-stu-id="0cf61-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cf61-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0cf61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cf61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf61-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-108">Percorso completo che specifica il percorso del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cf61-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-109">*LimitId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-110">Un ID di Rilevamento modifiche resiliente o un ID dello snapshot del set VHD che indica la linea di base per le modifiche nel disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cf61-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-111">*TargetSnapshotId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-112">ID dello snapshot VHDSet che indica lo snapshot da confrontare con la linea di base quando si denominano le modifiche nel disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cf61-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="0cf61-113">Questo parametro è valido solo per i file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="0cf61-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-114">*ByteOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-115">Offset di byte dell'area del disco virtuale per la quale eseguire una query sulle modifiche.</span><span class="sxs-lookup"><span data-stu-id="0cf61-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-116">*ByteLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-117">Lunghezza in byte dell'area del disco virtuale per la quale eseguire una query sulle modifiche.</span><span class="sxs-lookup"><span data-stu-id="0cf61-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="0cf61-118">Il numero deve essere inferiore a quello del disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cf61-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-119">*ProcessedByteLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-120">Lunghezza totale in byte elaborata.</span><span class="sxs-lookup"><span data-stu-id="0cf61-120">The total byte length that was processed.</span></span> <span data-ttu-id="0cf61-121">Potrebbe essere uguale a ByteLength o less.</span><span class="sxs-lookup"><span data-stu-id="0cf61-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-122">*ChangedByteOffsets* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-123">Elenco di offset di byte nel disco virtuale che indica l'inizio di ogni intervallo modificato.</span><span class="sxs-lookup"><span data-stu-id="0cf61-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-124">*ChangedByteLengths* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-125">Elenco di lunghezze in byte degli intervalli modificati nel disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cf61-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="0cf61-126">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf61-127">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="0cf61-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf61-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cf61-128">Return value</span></span>

<span data-ttu-id="0cf61-129">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cf61-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0cf61-130">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0cf61-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-131">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="0cf61-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-132">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="0cf61-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-133">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="0cf61-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-134">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="0cf61-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-135">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="0cf61-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-136">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0cf61-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-137">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0cf61-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-138">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0cf61-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-139">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="0cf61-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-140">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0cf61-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-141">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="0cf61-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-142">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0cf61-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0cf61-143">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="0cf61-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0cf61-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cf61-144">Requirements</span></span>



| <span data-ttu-id="0cf61-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cf61-145">Requirement</span></span> | <span data-ttu-id="0cf61-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0cf61-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf61-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cf61-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf61-148">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0cf61-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0cf61-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cf61-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf61-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0cf61-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0cf61-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0cf61-151">Namespace</span></span><br/>                | <span data-ttu-id="0cf61-152">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0cf61-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0cf61-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0cf61-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cf61-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cf61-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cf61-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0cf61-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cf61-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0cf61-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0cf61-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cf61-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf61-158">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="0cf61-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




