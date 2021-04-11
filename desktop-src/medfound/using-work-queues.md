---
description: In questo argomento viene descritto come utilizzare le code di lavoro in Microsoft Media Foundation.
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: Uso delle code di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226497"
---
# <a name="using-work-queues"></a>Uso delle code di lavoro

In questo argomento viene descritto come utilizzare le code di lavoro in Microsoft Media Foundation.

-   [Uso delle code di lavoro](#using-work-queues)
-   [Chiusura di code di lavoro](#shutting-down-work-queues)
-   [Uso degli elementi di lavoro pianificati](#using-scheduled-work-items)
-   [Uso di callback periodici](#using-periodic-callbacks)
-   [Argomenti correlati](#related-topics)

## <a name="using-work-queues"></a>Uso delle code di lavoro

Una coda di lavoro è un modo efficiente per eseguire operazioni asincrone su un altro thread. Concettualmente, si inseriscono elementi di lavoro nella coda e la coda include un thread che estrae ogni elemento dalla coda e lo invia. Gli elementi di lavoro vengono implementati come callback tramite l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .

Media Foundation crea diverse code di lavoro standard, denominate *code di lavoro della piattaforma*. Le applicazioni possono inoltre creare le proprie code di lavoro, denominate *code di lavoro private*. Per un elenco delle code di lavoro della piattaforma, vedere [identificatori della coda di lavoro](work-queue-identifiers.md). Per creare una coda di lavoro privata, chiamare [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Questa funzione restituisce un identificatore per la nuova coda di lavoro. Per inserire un elemento nella coda, chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). In entrambi i casi, è necessario specificare un'interfaccia di callback.

-   [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) accetta un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , oltre a un oggetto di stato facoltativo che implementa **IUnknown**. Si tratta degli stessi parametri usati nei metodi asincroni, come descritto nell'argomento [metodi di callback asincroni](asynchronous-callback-methods.md). Internamente, questa funzione crea un oggetto risultato asincrono, che viene passato al metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del callback.
-   [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) accetta un puntatore all'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Questa interfaccia rappresenta un oggetto risultato asincrono. Creare questo oggetto chiamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) e specificando l'interfaccia di callback e, facoltativamente, un oggetto di stato.

In entrambi i casi, il thread della coda di lavoro chiama il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Usare il metodo **Invoke** per eseguire l'elemento di lavoro.

Se più di un thread o un componente condivide la stessa coda di lavoro, è possibile chiamare [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) per bloccare la coda di lavoro, evitando così di rilasciare la piattaforma. Per ogni chiamata a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) o **MFLockWorkQueue**, è necessario chiamare [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) una volta per rilasciare la coda di lavoro. Se, ad esempio, si crea una nuova coda di lavoro e la si blocca una sola volta, è necessario chiamare **MFUnlockWorkQueue** due volte, una per la chiamata a **MFAllocateWorkQueue** e una per la chiamata a **MFLockWorkQueue**.

Il codice seguente illustra come creare una nuova coda di lavoro, inserire un elemento di lavoro nella coda e rilasciare la coda di lavoro.

Per ulteriori informazioni sulle code di lavoro in Windows 8, vedere [miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md) .


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



Questo esempio si basa sul presupposto che *pCallback* sia un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell'applicazione. Si presuppone inoltre che il callback imposti l'handle dell'evento *hEvent* . Il codice attende che questo evento venga impostato prima di chiamare [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue).

I thread della coda di lavoro vengono sempre creati nel processo del chiamante. All'interno di ogni coda di lavoro, vengono serializzati i callback. Se si chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) due volte con la stessa coda di lavoro, il secondo callback non viene richiamato fino a quando non viene restituito il primo callback.

## <a name="shutting-down-work-queues"></a>Chiusura di code di lavoro

Prima di chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), rilasciare tutte le risorse usate dai thread della coda di lavoro. Per sincronizzare questo processo, è possibile bloccare la piattaforma Media Foundation, che impedisce la chiusura di tutti i thread della coda di lavoro da parte della funzione **MFShutdown** . Se **MFShutdown** viene chiamato mentre la piattaforma è bloccata, **MFShutdown** attende alcune centinaia di millisecondi per sbloccare la piattaforma. Se non viene sbloccato entro questo intervallo di tempo, **MFShutdown** chiude i thread della coda di lavoro.

L'implementazione predefinita di [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) blocca automaticamente la piattaforma Media Foundation quando viene creato l'oggetto risultato. Il rilascio dell'interfaccia Sblocca la piattaforma. Pertanto, non sarà mai necessario bloccare direttamente la piattaforma. Tuttavia, se si scrive un'implementazione personalizzata di **IMFAsyncResult**, è necessario bloccare e sbloccare manualmente la piattaforma. Per bloccare la piattaforma, chiamare [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform). Per sbloccare la piattaforma, chiamare [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform). Per un esempio, vedere [oggetti risultato asincrono personalizzati](custom-asynchronous-result-objects.md).

Dopo aver chiamato [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), è necessario assicurarsi che la piattaforma venga sbloccata entro il periodo di timeout di 5 secondi. A tale scopo, rilasciare tutti i puntatori [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) e chiamare [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) se la piattaforma è stata bloccata manualmente. Assicurarsi di rilasciare tutte le risorse usate dai thread della coda di lavoro oppure se l'applicazione potrebbe perdere memoria.

In genere, se l'applicazione viene arrestata e rilascia ogni Media Foundation oggetto prima di chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), non è necessario preoccuparsi del blocco. Il meccanismo di blocco consente semplicemente la chiusura normale dei thread della coda di lavoro dopo la chiamata a **MFShutdown**.

## <a name="using-scheduled-work-items"></a>Uso degli elementi di lavoro pianificati

È possibile pianificare un callback in modo che venga eseguito dopo un periodo di tempo stabilito chiamando [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) o [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex).

-   [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) accetta un puntatore al callback, a un oggetto di stato facoltativo e a un intervallo di timeout.
-   [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) accetta un puntatore a un oggetto risultato asincrono e un valore di timeout.

Specificare il timeout come valore negativo in millisecondi. Ad esempio, per pianificare una richiamata da richiamare in 5 secondi, utilizzare il valore − 5000. Entrambe le funzioni restituiscono un valore di **\_ chiave MFWORKITEM** , che è possibile usare per annullare il callback passandolo alla funzione [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) .

Gli elementi di lavoro pianificati utilizzano sempre la \_ \_ coda di lavoro della piattaforma timer della coda di callback MFASYNC \_ .

## <a name="using-periodic-callbacks"></a>Uso di callback periodici

La funzione [**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) pianifica un callback da richiamare periodicamente finché non viene annullato. L'intervallo di callback è fisso. le applicazioni non possono modificarlo. Per individuare l'intervallo esatto, chiamare [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity). L'intervallo è nell'ordine di 10 millisecondi, quindi questa funzione è destinata alle situazioni in cui è necessario un "tick" frequente, ad esempio l'implementazione di un clock di presentazione. Se si desidera pianificare l'esecuzione di un'operazione con una frequenza minore, utilizzare un elemento di lavoro pianificato, come descritto in precedenza.

Diversamente dagli altri callback descritti in questo argomento, il callback periodico non usa l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . USA invece un puntatore a funzione. Per altre informazioni, vedere [**callback di MFPERIODICCALLBACK**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).

Per annullare il callback periodico, chiamare [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback).

I callback periodici usano la \_ coda di \_ lavoro della piattaforma timer della coda di callback MFASYNC \_ .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Code di lavoro](work-queues.md)
</dt> <dt>

[**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[Miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
