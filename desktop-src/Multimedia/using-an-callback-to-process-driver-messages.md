---
title: Utilizzo di un callback di evento per elaborare i messaggi del driver
description: Utilizzo di un callback di evento per elaborare i messaggi del driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio Waveform, callback evento
- blocchi di dati audio, callback di evento
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- CreateEvent (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725415"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="f82fd-109">Utilizzo di un callback di evento per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="f82fd-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="f82fd-110">Per usare un callback di evento, usare la funzione [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) per creare un evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="f82fd-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="f82fd-111">Nella chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) specificare l'evento di **callback \_** per il parametro *fdwOpen* .</span><span class="sxs-lookup"><span data-stu-id="f82fd-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="f82fd-112">Dopo aver chiamato la funzione [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , ma prima di inviare dati audio della forma d'onda al dispositivo, inserire l'evento in uno stato non segnalato chiamando la funzione [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) .</span><span class="sxs-lookup"><span data-stu-id="f82fd-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="f82fd-113">Quindi, all'interno di un ciclo che controlla se il flag **WHDR \_ done** è impostato nel membro **dwFlags** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , chiamare la funzione [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , specificando come parametri l'handle di evento e un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="f82fd-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="f82fd-114">Poiché i callback degli eventi non ricevono notifiche Close, done o Open specifiche, è possibile che un'applicazione debba controllare lo stato del processo in attesa dopo che si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="f82fd-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="f82fd-115">È possibile che una serie di attività sia stata completata nel momento in cui [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) restituisce.</span><span class="sxs-lookup"><span data-stu-id="f82fd-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f82fd-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f82fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f82fd-117">Blocchi di dati audio</span><span class="sxs-lookup"><span data-stu-id="f82fd-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 