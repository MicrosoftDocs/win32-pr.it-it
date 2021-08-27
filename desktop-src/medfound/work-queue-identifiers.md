---
description: Le costanti seguenti identificano l'Media Foundation code di lavoro standard.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificatori delle code di lavoro (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d454e8b2a199a9c132bf6ea287f31d7d3e5102
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470228"
---
# <a name="work-queue-identifiers"></a>Identificatori delle code di lavoro

Le costanti seguenti identificano l'Media Foundation code di lavoro standard.

Le applicazioni devono usare MFASYNC CALLBACK QUEUE MULTITHREADED o una coda di lavoro ottenuta da \_ \_ \_ [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) se vogliono controllare la priorità di esecuzione. Si noti che le priorità predefinite della coda di lavoro della piattaforma possono cambiare in modo dinamico quando un'applicazione chiama [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Per altre informazioni sulle code di lavoro, vedere [Code di lavoro](work-queues.md).




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt><dt>0x00000001</dt></dl> | Nella maggior parte dei casi, le applicazioni devono <strong>usare MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> Questa coda di lavoro viene usata per le operazioni sincrone. L'uso della coda di lavoro standard può causare il rischio di deadlock. Le applicazioni possono creare una coda sincrona privata sopra la coda multithread usando <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt><dt>0x00000002</dt></dl> | Non per l'uso generale dell'applicazione.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt><dt>0x00000003</dt></dl> | Non per l'uso generale dell'applicazione.<br /> Questa coda di lavoro viene usata internamente per operazioni di I/O, ad esempio la lettura di file e la lettura dalla rete.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt><dt>0x00000004</dt></dl> | Non per l'uso generale dell'applicazione.<br /> Questa coda di lavoro viene usata per i callback periodici e gli elementi di lavoro pianificati. Le funzioni seguenti mettono gli elementi di lavoro in questa coda:<br /><ul><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li></ul> | 
| <span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt><dt>0x00000005</dt></dl> | Questa coda di lavoro multithreading deve essere usata nella maggior parte dei casi. <br /> Questa coda di lavoro viene usata per le operazioni asincrone in Media Foundation.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt><dt>0x00000007</dt></dl> | Non per l'uso generale dell'applicazione. Le applicazioni devono invece <strong>usare MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> | 




Inoltre, le costanti seguenti vengono usate in connessione con le code di lavoro.



| Costante/valore                                                                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ CODA \_ DI CALLBACK \_ NON**</dt> <dt>0X00000000</dt> </dl>           | Coda di lavoro non definita.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ MASCHERA PRIVATA CODA DI CALLBACK \_ \_ \_ 0xFFFF0000**</dt> <dt></dt> </dl> | Maschera di bit per distinguere le code di lavoro della piattaforma da quelle create chiamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Per una coda di lavoro creata [**da MFAllocateWorkQueue,**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)il valore seguente è diverso da zero:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ CODA DI CALLBACK \_ \_ ALL**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Tutte le code di lavoro della piattaforma.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation costanti](media-foundation-constants.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> <dt>

[Miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




