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
# <a name="work-queue-identifiers"></a>Identificatori della coda di lavoro

Le costanti seguenti identificano le code di lavoro Media Foundation standard.

Le applicazioni devono usare \_ \_ la coda \_ di callback MFASYNC multithreading o usare una coda di lavoro ottenuta da [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) se vogliono controllare la priorità di esecuzione. Si noti che le priorità predefinite della coda di lavoro della piattaforma possono essere modificate dinamicamente quando un'applicazione chiama [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Per altre informazioni sulle code di lavoro, vedere [code di lavoro](work-queues.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Nella maggior parte dei casi, le applicazioni devono utilizzare <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/> Questa coda di lavoro viene usata per le operazioni sincrone. L'utilizzo della coda di lavoro standard può compromettere il rischio di un deadlock. Le applicazioni possono creare una coda sincrona privata all'inizio della coda multithread usando <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Non per uso generale dell'applicazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </dl></td>
<td style="text-align: left;">Non per uso generale dell'applicazione.<br/> Questa coda di lavoro viene usata internamente per le operazioni di I/O, ad esempio la lettura dei file e la lettura dalla rete.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Non per uso generale dell'applicazione.<br/> Questa coda di lavoro viene utilizzata per callback periodici ed elementi di lavoro pianificati. Le funzioni seguenti inseriscono elementi di lavoro in questa coda:<br/>
<ul>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </dl></td>
<td style="text-align: left;">Questa coda di lavoro multithreading deve essere utilizzata nella maggior parte dei casi. <br/> Questa coda di lavoro viene utilizzata per le operazioni asincrone in Media Foundation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </dl></td>
<td style="text-align: left;">Non per uso generale dell'applicazione. Le applicazioni devono invece usare <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/></td>
</tr>
</tbody>
</table>



Inoltre, le costanti seguenti vengono utilizzate nella connessione con le code di lavoro.



| Costante/valore                                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ 0x00000000 \_ non \_ definito della coda di callback**</dt> <dt></dt> </dl>           | Coda di lavoro non definita.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ \_ \_ \_ Maschera privata della coda di callback**</dt> <dt>0xFFFF0000</dt> </dl> | Maschera di bit per distinguere le code di lavoro della piattaforma da quelle create chiamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Per una coda di lavoro creata da [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), il valore seguente è diverso da zero:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ Coda di CALLBACK \_ \_ tutti**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Tutte le code di lavoro della piattaforma.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> <dt>

[Miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




