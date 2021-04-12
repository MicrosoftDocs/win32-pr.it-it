---
title: Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione
description: Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio della forma d'onda, gestione della riproduzione con messaggi
- waveform-interfaccia audio, gestione della riproduzione con messaggi
- riproduzione di file audio con forma d'onda, gestione della riproduzione con messaggi
- audio Waveform, messaggi
- waveform-interfaccia audio, messaggi
- riproduzione di file audio (Waveform), messaggi
- Messaggio MM_WOM_CLOSE
- Messaggio MM_WOM_DONE
- Messaggio MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337102"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="4dcbb-112">Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione</span><span class="sxs-lookup"><span data-stu-id="4dcbb-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="4dcbb-113">I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della riproduzione dell'audio e della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="4dcbb-114">Message</span><span class="sxs-lookup"><span data-stu-id="4dcbb-114">Message</span></span>                                | <span data-ttu-id="4dcbb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dcbb-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4dcbb-116">**MM \_ WOM \_ Close**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="4dcbb-117">Inviato quando il dispositivo viene chiuso tramite la funzione [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="4dcbb-118">**MM \_ WOM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="4dcbb-119">Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="4dcbb-120">**MM \_ WOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="4dcbb-121">Inviato quando il dispositivo viene aperto tramite la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="4dcbb-122">Un parametro *wParam* e *lParam* è associato a ognuno di questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="4dcbb-123">Il parametro *wParam* specifica sempre un handle del dispositivo waveform aperto-audio.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="4dcbb-124">Per il messaggio [**mm \_ WOM \_ done**](mm-wom-done.md) , *lParam* specifica un puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il blocco di dati completato.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="4dcbb-125">Il parametro *lParam* non è utilizzato per i messaggi di [**chiusura di mm \_ \_ WOM**](mm-wom-close.md) e [**mm \_ WOM \_ aperti**](mm-wom-open.md) .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="4dcbb-126">Il messaggio più utile è probabilmente MM \_ WOM \_ fatto.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="4dcbb-127">Quando questo messaggio segnala che la riproduzione di un blocco di dati è stata completata, è possibile pulire e liberare il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="4dcbb-128">A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario elaborare i \_ messaggi di chiusura mm WOM \_ Open e mm \_ WOM \_ .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="4dcbb-129">La funzione di callback per i dispositivi Waveform-Audio output viene fornita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="4dcbb-130">Per informazioni su questa funzione di callback, vedere la funzione [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4dcbb-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 