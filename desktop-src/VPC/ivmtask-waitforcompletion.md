---
title: Metodo IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Attende il completamento dell'attività o l'intervallo di timeout specificato.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Metodo WaitForCompletion Virtual PC
- Metodo WaitForCompletion Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, metodo WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302098"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="86cc7-106">Metodo IVMTask:: WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="86cc7-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="86cc7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86cc7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86cc7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="86cc7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86cc7-109">Attende il completamento dell'attività o l'intervallo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="86cc7-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cc7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86cc7-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="86cc7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="86cc7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86cc7-112">*timeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86cc7-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cc7-113">Tempo, in millisecondi, durante il quale questo metodo attenderà il completamento dell'attività prima di restituire il controllo al chiamante.</span><span class="sxs-lookup"><span data-stu-id="86cc7-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="86cc7-114">Il valore-1 indica che il metodo resterà in attesa fino al completamento dell'attività senza timeout. Altri valori di timeout validi sono compresi tra 0 e 4 milioni millisecondi.</span><span class="sxs-lookup"><span data-stu-id="86cc7-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86cc7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86cc7-115">Return value</span></span>

<span data-ttu-id="86cc7-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="86cc7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="86cc7-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="86cc7-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="86cc7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86cc7-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="86cc7-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86cc7-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="86cc7-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="86cc7-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="86cc7-121"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="86cc7-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="86cc7-122">Il parametro *timeout* non è valido.</span><span class="sxs-lookup"><span data-stu-id="86cc7-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="86cc7-123"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86cc7-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="86cc7-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="86cc7-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="86cc7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="86cc7-125">Remarks</span></span>

<span data-ttu-id="86cc7-126">Il metodo **WaitForCompletion** inserisce il thread di esecuzione corrente in modalità di sospensione fino a quando non viene restituito.</span><span class="sxs-lookup"><span data-stu-id="86cc7-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="86cc7-127">Non è consigliabile specificare un'attesa infinita (timeout =-1), a meno che non sia assolutamente fondamentale che l'attività venga completata in qualsiasi circostanza.</span><span class="sxs-lookup"><span data-stu-id="86cc7-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="86cc7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86cc7-128">Requirements</span></span>



| <span data-ttu-id="86cc7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="86cc7-129">Requirement</span></span> | <span data-ttu-id="86cc7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="86cc7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cc7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cc7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="86cc7-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="86cc7-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86cc7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cc7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="86cc7-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="86cc7-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86cc7-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="86cc7-135">End of client support</span></span><br/>    | <span data-ttu-id="86cc7-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86cc7-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86cc7-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="86cc7-137">Product</span></span><br/>                  | <span data-ttu-id="86cc7-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86cc7-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86cc7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86cc7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="86cc7-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="86cc7-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86cc7-141">IID</span><span class="sxs-lookup"><span data-stu-id="86cc7-141">IID</span></span><br/>                      | <span data-ttu-id="86cc7-142">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="86cc7-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="86cc7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86cc7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cc7-144">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="86cc7-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

