---
title: Linee guida per la creazione di file MIDI
description: Linee guida per la creazione di file MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- creazione di file MIDI, linee guida per la creazione di file
- assegnazioni di patch MIDI standard
- assegnazioni di chiavi MIDI standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di chiavi standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di chiavi standard
- creazione di file MIDI, assegnazioni di patch standard
- creazione di file MIDI, assegnazioni di chiavi standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045271"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="67629-114">Linee guida per la creazione di file MIDI</span><span class="sxs-lookup"><span data-stu-id="67629-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="67629-115">Per creare file MIDI indipendenti dal dispositivo per Windows, seguire queste linee guida:</span><span class="sxs-lookup"><span data-stu-id="67629-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="67629-116">Usare le [assegnazioni di patch MIDI standard](standard-midi-patch-assignments.md) e le [assegnazioni di chiavi MIDI standard](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="67629-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="67629-117">Inviare sempre un messaggio di modifica del programma a un canale per selezionare una patch prima di inviare altri messaggi a tale canale.</span><span class="sxs-lookup"><span data-stu-id="67629-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="67629-118">Per i due canali di percussione (10 e 16), selezionare programma numero 0.</span><span class="sxs-lookup"><span data-stu-id="67629-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="67629-119">Seguire sempre un messaggio di modifica del programma MIDI con un messaggio del controller principale del volume MIDI (controller numero 7) per impostare il volume relativo della patch.</span><span class="sxs-lookup"><span data-stu-id="67629-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="67629-120">Usare il valore 80 (0x50) per il controller principale del volume per i livelli di ascolto normali.</span><span class="sxs-lookup"><span data-stu-id="67629-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="67629-121">Per i livelli più tranquilli o più forti, è possibile usare valori inferiori o superiori.</span><span class="sxs-lookup"><span data-stu-id="67629-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="67629-122">Usare solo i messaggi MIDI seguenti: note-on con velocità, nota-off, modifica del programma, curva di pitch, volume principale (controller 7) e pedale Damper (controller 64).</span><span class="sxs-lookup"><span data-stu-id="67629-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="67629-123">I sintetizzatori interni sono necessari per rispondere a questi messaggi e la maggior parte degli strumenti musicali MIDI rispondono anche a tali messaggi.</span><span class="sxs-lookup"><span data-stu-id="67629-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 




