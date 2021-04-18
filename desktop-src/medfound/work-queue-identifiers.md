---
description: Le costanti seguenti identificano le code di lavoro Media Foundation standard.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificatori della coda di lavoro (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313033"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="74c15-103">Identificatori della coda di lavoro</span><span class="sxs-lookup"><span data-stu-id="74c15-103">Work Queue Identifiers</span></span>

<span data-ttu-id="74c15-104">Le costanti seguenti identificano le code di lavoro Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="74c15-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="74c15-105">Le applicazioni devono usare \_ \_ la coda \_ di callback MFASYNC multithreading o usare una coda di lavoro ottenuta da [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) se vogliono controllare la priorità di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="74c15-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="74c15-106">Si noti che le priorità predefinite della coda di lavoro della piattaforma possono essere modificate dinamicamente quando un'applicazione chiama [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span><span class="sxs-lookup"><span data-stu-id="74c15-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="74c15-107">Per altre informazioni sulle code di lavoro, vedere [code di lavoro](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="74c15-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="74c15-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="74c15-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="74c15-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74c15-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="74c15-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-111">Nella maggior parte dei casi, le applicazioni devono utilizzare <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="74c15-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="74c15-112">Questa coda di lavoro viene usata per le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="74c15-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="74c15-113">L'utilizzo della coda di lavoro standard può compromettere il rischio di un deadlock.</span><span class="sxs-lookup"><span data-stu-id="74c15-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="74c15-114">Le applicazioni possono creare una coda sincrona privata all'inizio della coda multithread usando <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="74c15-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="74c15-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-116">Non per uso generale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74c15-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="74c15-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-118">Non per uso generale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74c15-118">Not for general application use.</span></span><br/> <span data-ttu-id="74c15-119">Questa coda di lavoro viene usata internamente per le operazioni di I/O, ad esempio la lettura dei file e la lettura dalla rete.</span><span class="sxs-lookup"><span data-stu-id="74c15-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="74c15-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-121">Non per uso generale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74c15-121">Not for general application use.</span></span><br/> <span data-ttu-id="74c15-122">Questa coda di lavoro viene utilizzata per callback periodici ed elementi di lavoro pianificati.</span><span class="sxs-lookup"><span data-stu-id="74c15-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="74c15-123">Le funzioni seguenti inseriscono elementi di lavoro in questa coda:</span><span class="sxs-lookup"><span data-stu-id="74c15-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="74c15-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="74c15-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="74c15-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="74c15-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="74c15-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="74c15-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="74c15-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-128">Questa coda di lavoro multithreading deve essere utilizzata nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="74c15-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="74c15-129">Questa coda di lavoro viene utilizzata per le operazioni asincrone in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="74c15-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="74c15-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="74c15-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="74c15-131">Non per uso generale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74c15-131">Not for general application use.</span></span> <span data-ttu-id="74c15-132">Le applicazioni devono invece usare <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="74c15-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="74c15-133">Inoltre, le costanti seguenti vengono utilizzate nella connessione con le code di lavoro.</span><span class="sxs-lookup"><span data-stu-id="74c15-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="74c15-134">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="74c15-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="74c15-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74c15-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="74c15-136"><dt>**MFASYNC \_ 0x00000000 \_ non \_ definito della coda di callback**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74c15-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="74c15-137">Coda di lavoro non definita.</span><span class="sxs-lookup"><span data-stu-id="74c15-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="74c15-138"><dt>**MFASYNC \_ \_ \_ \_ Maschera privata della coda di callback**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="74c15-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="74c15-139">Maschera di bit per distinguere le code di lavoro della piattaforma da quelle create chiamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="74c15-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="74c15-140">Per una coda di lavoro creata da [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), il valore seguente è diverso da zero:</span><span class="sxs-lookup"><span data-stu-id="74c15-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="74c15-141"><dt>**MFASYNC \_ Coda di CALLBACK \_ \_ tutti**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="74c15-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="74c15-142">Tutte le code di lavoro della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="74c15-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="74c15-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74c15-143">Requirements</span></span>



| <span data-ttu-id="74c15-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="74c15-144">Requirement</span></span> | <span data-ttu-id="74c15-145">Valore</span><span class="sxs-lookup"><span data-stu-id="74c15-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c15-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74c15-146">Minimum supported client</span></span><br/> | <span data-ttu-id="74c15-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74c15-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74c15-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74c15-148">Minimum supported server</span></span><br/> | <span data-ttu-id="74c15-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74c15-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74c15-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74c15-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c15-151"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74c15-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c15-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74c15-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c15-153">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74c15-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="74c15-154">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="74c15-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="74c15-155">Miglioramenti della coda di lavoro e del threading</span><span class="sxs-lookup"><span data-stu-id="74c15-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




