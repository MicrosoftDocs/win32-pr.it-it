---
title: Gestione dei blocchi di dati MIDI
description: Gestione dei blocchi di dati MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- MIDI (Musical Instrument Digital Interface), gestione di blocchi di dati
- MIDI (Musical Instrument Digital Interface), gestione di blocchi di dati
- Servizi MIDI, gestione di blocchi di dati
- gestione dei blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), elaborazione dei messaggi del driver
- MIDI (Musical Instrument Digital Interface), elaborazione dei messaggi del driver
- Servizi MIDI, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- Servizi MIDI, blocchi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956390"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="99c80-114">Gestione dei blocchi di dati MIDI</span><span class="sxs-lookup"><span data-stu-id="99c80-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="99c80-115">Le applicazioni che utilizzano blocchi di dati per passare i messaggi esclusivi del sistema (mediante le funzioni [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) e [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) e i buffer di flusso (mediante la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) devono fornire continuamente al driver di dispositivo i blocchi di dati fino al completamento della riproduzione o della registrazione.</span><span class="sxs-lookup"><span data-stu-id="99c80-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="99c80-116">Anche se viene utilizzato un singolo blocco di dati, un'applicazione deve essere in grado di determinare quando un driver di dispositivo è terminato con il blocco di dati, in modo da poter liberare la memoria associata al blocco di dati e alla struttura dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="99c80-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="99c80-117">Per determinare quando un driver di dispositivo è terminato con un blocco di dati, è possibile usare tre metodi:</span><span class="sxs-lookup"><span data-stu-id="99c80-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="99c80-118">Specificare una funzione di callback per ricevere un messaggio inviato dal driver al termine di un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="99c80-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="99c80-119">Per ottenere i dati di input MIDI timestamp, è necessario usare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="99c80-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="99c80-120">Usare un callback di evento (solo per l'output).</span><span class="sxs-lookup"><span data-stu-id="99c80-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="99c80-121">Usare un callback di finestra o di thread per ricevere un messaggio inviato dal driver al termine di un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="99c80-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="99c80-122">Se un'applicazione non ottiene un blocco di dati per il driver di dispositivo quando necessario, potrebbe verificarsi una lacuna udibile nella riproduzione o una perdita di informazioni registrate in arrivo.</span><span class="sxs-lookup"><span data-stu-id="99c80-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="99c80-123">Come minimo, un'applicazione deve usare uno schema a doppio buffer per mantenere almeno un blocco di dati prima del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99c80-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="99c80-124">Utilizzo di una funzione di callback per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="99c80-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="99c80-125">È possibile scrivere una funzione di callback personalizzata per elaborare i messaggi inviati dal driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99c80-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="99c80-126">Per usare una funzione di callback, specificare il \_ flag della funzione di callback nel parametro *dwFlags* e l'indirizzo della funzione di callback nel parametro *dwCallback* della funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="99c80-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="99c80-127">I messaggi inviati a una funzione di callback sono simili ai messaggi inviati a una finestra, con la differenza che hanno due parametri parola doppia anziché un parametro Unsigned Integer e un parametro parola doppia.</span><span class="sxs-lookup"><span data-stu-id="99c80-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="99c80-128">Per ulteriori informazioni su questi messaggi, vedere [invio di messaggi di System-Exclusive](sending-system-exclusive-messages.md) e [gestione della registrazione MIDI](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="99c80-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="99c80-129">Usare una delle tecniche seguenti per passare i dati dell'istanza da un'applicazione a una funzione di callback:</span><span class="sxs-lookup"><span data-stu-id="99c80-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="99c80-130">Usare il parametro *dwCallbackInstance* della funzione che apre il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99c80-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="99c80-131">Usare il membro **dwUser** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica un blocco di dati inviato a un driver di dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="99c80-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="99c80-132">Se sono necessari più di 32 bit di dati dell'istanza, passare un indirizzo di una struttura contenente le informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="99c80-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="99c80-133">Utilizzo di un callback di evento per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="99c80-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="99c80-134">Per usare un callback di evento, usare la funzione [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) per recuperare l'handle di un evento e specificare un evento di callback \_ nella chiamata alla funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="99c80-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="99c80-135">Un callback di evento viene impostato da qualsiasi elemento che potrebbe causare un callback di funzione.</span><span class="sxs-lookup"><span data-stu-id="99c80-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="99c80-136">Diversamente dalle funzioni di callback e dai callback della finestra o del thread, i callback degli eventi non ricevono notifiche di chiusura, fine o apertura specifiche.</span><span class="sxs-lookup"><span data-stu-id="99c80-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="99c80-137">È pertanto possibile che un'applicazione debba controllare lo stato del processo in attesa dopo l'evento.</span><span class="sxs-lookup"><span data-stu-id="99c80-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="99c80-138">Per ulteriori informazioni sui callback di evento, vedere [utilizzo di un callback di evento per gestire la riproduzione memorizzata nel buffer](using-an-callback-to-manage-buffered-playback.md).</span><span class="sxs-lookup"><span data-stu-id="99c80-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="99c80-139">Utilizzo di una finestra o di un callback di thread per elaborare i messaggi del driver</span><span class="sxs-lookup"><span data-stu-id="99c80-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="99c80-140">Per usare un callback della finestra, specificare il \_ flag della finestra di callback nel parametro *dwFlags* e un handle di finestra nella parola di ordine inferiore del parametro *dwCallback* della funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="99c80-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="99c80-141">I messaggi del driver verranno inviati alla funzione routine della finestra per la finestra identificata dall'handle in *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="99c80-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="99c80-142">Analogamente, per usare un callback di thread, specificare il flag del thread di CALLBACK \_ e un identificatore del thread nella chiamata a **MidiInOpen** o **midiOutOpen**.</span><span class="sxs-lookup"><span data-stu-id="99c80-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="99c80-143">In questo caso, i messaggi verranno inviati al thread specificato anziché a una finestra.</span><span class="sxs-lookup"><span data-stu-id="99c80-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="99c80-144">I messaggi inviati a una finestra o a un callback di thread sono specifici del dispositivo MIDI usato.</span><span class="sxs-lookup"><span data-stu-id="99c80-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="99c80-145">Per ulteriori informazioni su questi messaggi, vedere [invio di messaggi di System-Exclusive](sending-system-exclusive-messages.md) e [gestione della registrazione MIDI](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="99c80-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99c80-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99c80-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99c80-147">Servizi MIDI</span><span class="sxs-lookup"><span data-stu-id="99c80-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 