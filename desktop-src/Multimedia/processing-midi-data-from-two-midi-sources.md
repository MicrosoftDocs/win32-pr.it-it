---
title: Elaborazione di dati MIDI da due origini MIDI
description: Elaborazione di dati MIDI da due origini MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimedia di Windows, elaborazione di dati MIDI da due origini
- Multimedia, elaborazione di dati MIDI da due origini
- audio multimediale, elaborazione di dati MIDI da due origini
- audio, elaborazione di dati MIDI da due origini
- MIDI (Musical Instrument Digital Interface), elaborazione di dati da due origini
- MIDI (Musical Instrument Digital Interface), elaborazione di dati da due origini
- elaborazione di dati MIDI da due origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046678"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="5ca7e-110">Elaborazione di dati MIDI da due origini MIDI</span><span class="sxs-lookup"><span data-stu-id="5ca7e-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="5ca7e-111">Il sottosistema MIDI può instradare i messaggi MIDI da due origini dati a un singolo dispositivo di output MIDI per la riproduzione simultanea.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="5ca7e-112">Ad esempio, un'origine può essere musica in background o una linea di basso che è stata pre-registrata e memorizzata in un file.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="5ca7e-113">La seconda origine può essere costituita da dati dinamici da uno strumento MIDI, ad esempio una tastiera o una chitarra.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="5ca7e-114">Entrambe le origini dati inviano i dati MIDI a un singolo dispositivo MIDI identificato con un handle.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="5ca7e-115">Inviare un flusso di dati tramite la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e uno o più buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="5ca7e-116">Questo flusso di dati contiene in genere dati preregistrati che vengono compressi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="5ca7e-117">Inviare in modo asincrono il secondo flusso di dati, in genere da uno strumento MIDI, usando la funzione [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ca7e-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="5ca7e-118">Lo stato di esecuzione di un buffer del flusso non verrà influenzato negativamente dalle chiamate asincrone effettuate dal secondo flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="5ca7e-119">Ogni breve messaggio inviato con **midiOutShortMsg** deve essere un messaggio MIDI completo, con un byte di stato e il numero appropriato di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="5ca7e-120">Se il byte di stato viene omesso, **midiOutShortMsg** restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="5ca7e-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="5ca7e-121">(Tuttavia, non è presente alcuno stato di esecuzione con l'output del flusso).</span><span class="sxs-lookup"><span data-stu-id="5ca7e-121">(However, there is no running status with stream output.)</span></span>

 

 