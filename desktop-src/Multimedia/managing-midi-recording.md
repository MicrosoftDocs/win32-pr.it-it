---
title: Gestione della registrazione MIDI
description: Gestione della registrazione MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (Musical Instrument Digital Interface), registrazione
- MIDI (Musical Instrument Digital Interface), registrazione
- registrazione dell'audio MIDI, gestione
- Registrazione MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472774"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="1c6b0-107">Gestione della registrazione MIDI</span><span class="sxs-lookup"><span data-stu-id="1c6b0-107">Managing MIDI Recording</span></span>

<span data-ttu-id="1c6b0-108">Dopo aver aperto un dispositivo MIDI, è possibile iniziare a registrare i dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="1c6b0-109">Windows fornisce le funzioni seguenti per la gestione della registrazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="1c6b0-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1c6b0-110">Value</span></span>                                      | <span data-ttu-id="1c6b0-111">Significato</span><span class="sxs-lookup"><span data-stu-id="1c6b0-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c6b0-112">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="1c6b0-113">Invia un buffer al driver di dispositivo in modo che possa essere riempito con i dati MIDI esclusivi del sistema registrati.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="1c6b0-114">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="1c6b0-115">Interrompe la registrazione MIDI e contrassegna tutti i buffer in sospeso come eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="1c6b0-116">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="1c6b0-117">Avvia la registrazione MIDI e reimposta il timestamp su zero.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="1c6b0-118">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="1c6b0-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="1c6b0-119">Interrompe la registrazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="1c6b0-120">Per inviare i buffer al driver di dispositivo per la registrazione di messaggi esclusivi del sistema, usare [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="1c6b0-121">L'applicazione riceve una notifica quando i buffer sono riempiti con dati registrati esclusivi del sistema.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="1c6b0-122">Per altre informazioni sulle tecniche di notifica, vedere [Managing MIDI Data blocks](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="1c6b0-123">La funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) avvia il processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="1c6b0-124">Quando si registrano messaggi esclusivi del sistema, inviare almeno un buffer al driver prima di avviare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="1c6b0-125">Per arrestare la registrazione, usare [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="1c6b0-126">Prima di chiudere il dispositivo usando la funzione [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , contrassegnare tutti i blocchi di dati in sospeso come vengono eseguiti chiamando [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="1c6b0-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="1c6b0-127">Le applicazioni che richiedono dati timestamp utilizzano una funzione di callback per ricevere dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="1c6b0-128">Se i requisiti di temporizzazione non sono severi, è possibile usare un callback di finestra o di thread.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="1c6b0-129">Tuttavia, non è possibile usare un callback di evento per ricevere dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="1c6b0-130">Per registrare messaggi esclusivi del sistema con applicazioni che non utilizzano buffer di flusso, è necessario fornire il driver di dispositivo con i buffer.</span><span class="sxs-lookup"><span data-stu-id="1c6b0-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="1c6b0-131">Questi buffer vengono specificati usando una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="1c6b0-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c6b0-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c6b0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6b0-133">Registrazione audio MIDI</span><span class="sxs-lookup"><span data-stu-id="1c6b0-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 