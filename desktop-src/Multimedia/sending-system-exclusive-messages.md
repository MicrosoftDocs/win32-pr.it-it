---
title: Invio di messaggi di System-Exclusive
description: Invio di messaggi di System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- MIDI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- riproduzione di file MIDI, messaggi esclusivi del sistema
- messaggi MIDI esclusivi del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872346"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="e6a08-111">Invio di messaggi di System-Exclusive</span><span class="sxs-lookup"><span data-stu-id="e6a08-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="e6a08-112">MIDI System: i messaggi esclusivi sono gli unici messaggi MIDI che non rientrano in un singolo valore parola doppia.</span><span class="sxs-lookup"><span data-stu-id="e6a08-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="e6a08-113">I messaggi esclusivi del sistema possono essere di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="e6a08-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="e6a08-114">Windows fornisce la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) per l'invio di messaggi esclusivi del sistema ai dispositivi di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="e6a08-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="e6a08-115">Per specificare i blocchi di dati esclusivi del sistema MIDI, utilizzare la struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="e6a08-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="e6a08-116">Dopo aver inviato un blocco di dati esclusivo del sistema tramite **midiOutLongMsg**, è necessario attendere il completamento del blocco di dati da parte del driver di dispositivo prima di liberarlo.</span><span class="sxs-lookup"><span data-stu-id="e6a08-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="e6a08-117">Se si inviano più blocchi di dati, è necessario monitorare il completamento di ogni blocco di dati in modo da stabilire quando inviare blocchi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e6a08-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="e6a08-118">Per informazioni sulle diverse tecniche per il monitoraggio del completamento dei blocchi di dati, vedere [Managing MIDI Data](managing-midi-data-blocks.md)Blocks.</span><span class="sxs-lookup"><span data-stu-id="e6a08-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="e6a08-119">Qualsiasi byte di stato MIDI diverso da un messaggio di sistema in tempo reale terminerà un messaggio esclusivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e6a08-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="e6a08-120">Se si usano più blocchi di dati per inviare un singolo messaggio esclusivo del sistema, non inviare messaggi MIDI diversi dai messaggi di sistema in tempo reale tra i blocchi di dati.</span><span class="sxs-lookup"><span data-stu-id="e6a08-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 