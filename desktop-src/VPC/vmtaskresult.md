---
title: Enumerazione VMTaskResult (VPCCOMInterfaces. h)
description: Specifica il risultato di un'attività.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- VMTaskResult enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518909"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="a9c61-104">Enumerazione VMTaskResult</span><span class="sxs-lookup"><span data-stu-id="a9c61-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="a9c61-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9c61-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9c61-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9c61-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9c61-107">Specifica il risultato di un'attività.</span><span class="sxs-lookup"><span data-stu-id="a9c61-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c61-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9c61-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="a9c61-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="a9c61-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9c61-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="a9c61-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-111">L'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a9c61-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="a9c61-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-113">L'attività è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="a9c61-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**\_UnexpectedError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-115">Errore imprevisto dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a9c61-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**\_OutOfMemoryError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-117">Memoria insufficiente per completare l'attività.</span><span class="sxs-lookup"><span data-stu-id="a9c61-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**\_DiskRelatedError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-119">L'attività ha restituito un errore durante la scrittura su disco (assicurarsi che lo spazio su disco sia sufficiente).</span><span class="sxs-lookup"><span data-stu-id="a9c61-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**\_IncompatibleSavedStateError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-121">Non è stato possibile ripristinare la macchina virtuale perché lo stato salvato non è compatibile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**\_TimeOutError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-123">Timeout dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a9c61-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**\_IllegalValueError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-125">Durante l'elaborazione dell'attività è stato letto un valore di preferenza non valido.</span><span class="sxs-lookup"><span data-stu-id="a9c61-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**\_ThreadCrashError vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-127">Thread associato all'attività arrestata in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="a9c61-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="a9c61-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**\_ShutdownAbort vmTaskResult**</span><span class="sxs-lookup"><span data-stu-id="a9c61-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="a9c61-129">La richiesta di arresto è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="a9c61-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9c61-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9c61-130">Requirements</span></span>



| <span data-ttu-id="a9c61-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c61-131">Requirement</span></span> | <span data-ttu-id="a9c61-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a9c61-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c61-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9c61-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c61-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9c61-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9c61-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9c61-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c61-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a9c61-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9c61-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9c61-137">End of client support</span></span><br/>    | <span data-ttu-id="a9c61-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9c61-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9c61-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a9c61-139">Product</span></span><br/>                  | <span data-ttu-id="a9c61-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9c61-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9c61-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9c61-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c61-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c61-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c61-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9c61-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c61-144">**IVMTask:: result**</span><span class="sxs-lookup"><span data-stu-id="a9c61-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

