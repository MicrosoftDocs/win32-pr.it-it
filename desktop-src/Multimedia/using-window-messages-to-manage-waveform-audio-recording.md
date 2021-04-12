---
title: Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio
description: Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio della forma d'onda, gestione della registrazione con messaggi
- waveform-interfaccia audio, gestione della registrazione con messaggi
- registrazione dell'audio della forma d'onda, gestione della registrazione con messaggi
- audio Waveform, messaggi
- waveform-interfaccia audio, messaggi
- registrazione dell'audio della forma d'onda, messaggi
- Messaggio MM_WIM_CLOSE
- Messaggio MM_WIM_DATA
- Messaggio MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472835"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="563ad-112">Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="563ad-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="563ad-113">I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della registrazione audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="563ad-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="563ad-114">Message</span><span class="sxs-lookup"><span data-stu-id="563ad-114">Message</span></span>                                | <span data-ttu-id="563ad-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563ad-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="563ad-116">**\_Wim \_ chiusura di mm**</span><span class="sxs-lookup"><span data-stu-id="563ad-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="563ad-117">Inviato quando il dispositivo viene chiuso tramite la funzione [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .</span><span class="sxs-lookup"><span data-stu-id="563ad-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="563ad-118">**\_dati WIM \_ mm**</span><span class="sxs-lookup"><span data-stu-id="563ad-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="563ad-119">Inviato quando il driver di dispositivo viene terminato con un buffer inviato tramite la funzione [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) .</span><span class="sxs-lookup"><span data-stu-id="563ad-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="563ad-120">**\_Wim \_ aperto mm**</span><span class="sxs-lookup"><span data-stu-id="563ad-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="563ad-121">Inviato quando il dispositivo viene aperto tramite la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .</span><span class="sxs-lookup"><span data-stu-id="563ad-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="563ad-122">Il parametro *lParam* dei [**\_ \_ dati WIM mm**](mm-wim-data.md) specifica un puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="563ad-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="563ad-123">Questo buffer potrebbe non essere completamente riempito con i dati audio della forma d'onda. la registrazione può arrestarsi prima del riempimento del buffer.</span><span class="sxs-lookup"><span data-stu-id="563ad-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="563ad-124">Usare il membro **dwBytesRecorded** della struttura **WAVEHDR** per determinare la quantità di dati validi presenti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="563ad-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="563ad-125">Il messaggio più utile è probabilmente [**i \_ \_ dati WIM mm**](mm-wim-data.md).</span><span class="sxs-lookup"><span data-stu-id="563ad-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="563ad-126">Quando l'applicazione termina usando il blocco di dati inviato dal driver di dispositivo, è possibile pulire e liberare il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="563ad-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="563ad-127">A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario usare i messaggi [**di \_ \_ chiusura**](mm-wim-close.md) WIM con formato WIM [**mm \_ \_**](mm-wim-open.md) .</span><span class="sxs-lookup"><span data-stu-id="563ad-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="563ad-128">La funzione di callback per i dispositivi di input audio e di forma d'onda viene fornita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="563ad-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="563ad-129">Per informazioni su questa funzione di callback, vedere la funzione [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="563ad-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="563ad-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="563ad-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="563ad-131">Registrazione dell'audio della forma d'onda</span><span class="sxs-lookup"><span data-stu-id="563ad-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 