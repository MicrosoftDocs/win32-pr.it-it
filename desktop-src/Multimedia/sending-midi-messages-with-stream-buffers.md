---
title: Invio di messaggi MIDI con buffer di flusso
description: Invio di messaggi MIDI con buffer di flusso
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- riproduzione di file MIDI, buffer di flusso
- buffer di flusso, invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725359"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="12372-111">Invio di messaggi MIDI con buffer di flusso</span><span class="sxs-lookup"><span data-stu-id="12372-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="12372-112">Quando l'applicazione funziona con i buffer di flusso, usa la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) per inviare tutti i messaggi MIDI (short e Long) al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12372-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="12372-113">Per specificare i blocchi di dati di flusso, utilizzare le strutture [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) e [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="12372-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="12372-114">La struttura **MIDIHDR** contiene un indirizzo di un blocco di dati bloccato, la lunghezza del blocco di dati e alcuni flag assortiti.</span><span class="sxs-lookup"><span data-stu-id="12372-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="12372-115">I dati vengono archiviati sotto forma di strutture **MIDIEVENT** .</span><span class="sxs-lookup"><span data-stu-id="12372-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="12372-116">Il sistema impone un limite di dimensioni di 64K nei buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="12372-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="12372-117">Dopo aver usato **midiStreamOut** per inviare un buffer di flusso di dati, è necessario attendere che il driver di dispositivo non sia terminato con il blocco di dati prima di liberarlo.</span><span class="sxs-lookup"><span data-stu-id="12372-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="12372-118">Se si inviano più blocchi di dati, è necessario monitorare il completamento di ogni blocco di dati in modo da stabilire quando inviare blocchi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="12372-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="12372-119">Per informazioni sulle diverse tecniche per il monitoraggio del completamento dei blocchi di dati, vedere [Managing MIDI Data](managing-midi-data-blocks.md)Blocks.</span><span class="sxs-lookup"><span data-stu-id="12372-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 