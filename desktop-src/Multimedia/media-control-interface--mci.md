---
title: Interfaccia di controllo multimediale (MCI)
description: Interfaccia di controllo multimediale (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimedia di Windows, interfaccia di controllo multimediale (MCI)
- Multimedia, interfaccia di controllo multimediale (MCI)
- audio multimediale, MCI (Media Control Interface)
- audio, interfaccia di controllo multimediale (MCI)
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (strumento musicale digitale), MCI (Media Control Interface)
- Interfaccia di controllo multimediale (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface), Musical Instrument Digital Interface (MIDI)
- Interfaccia di controllo multimediale (MCI), MIDI sequencer
- MCI (Media Control Interface), MIDI sequencer
- MCI MIDI sequencer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044639"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="c30bb-114">Interfaccia di controllo multimediale (MCI)</span><span class="sxs-lookup"><span data-stu-id="c30bb-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="c30bb-115">MCI MIDI sequencer è il componente di sistema MCI che riproduce file MIDI.</span><span class="sxs-lookup"><span data-stu-id="c30bb-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="c30bb-116">Le applicazioni possono riprodurre facilmente file MIDI usando MCI, ma MCI impone le seguenti restrizioni sulle funzionalità MIDI:</span><span class="sxs-lookup"><span data-stu-id="c30bb-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="c30bb-117">MCI supporta solo l'output MIDI.</span><span class="sxs-lookup"><span data-stu-id="c30bb-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="c30bb-118">MCI non consente la sincronizzazione di chiusura tra eventi MIDI e altri eventi in tempo reale, ad esempio video.</span><span class="sxs-lookup"><span data-stu-id="c30bb-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="c30bb-119">Se è necessaria una sincronizzazione MIDI accurata, è necessario usare i buffer di flusso o i servizi MIDI.</span><span class="sxs-lookup"><span data-stu-id="c30bb-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="c30bb-120">Se sono necessarie funzionalità di input MIDI, è necessario usare i servizi MIDI.</span><span class="sxs-lookup"><span data-stu-id="c30bb-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="c30bb-121">MCI MIDI sequencer riproduce i file MIDI standard e i file MIDI del formato di file di scambio di risorse (RIFF), noti come file RMID.</span><span class="sxs-lookup"><span data-stu-id="c30bb-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="c30bb-122">I file MIDI standard sono conformi alla specifica dei [file MIDI standard 1,0](creating-midi-files.md) .</span><span class="sxs-lookup"><span data-stu-id="c30bb-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="c30bb-123">Poiché i file RMID sono file MIDI standard con un'intestazione RIFF, le informazioni sui file MIDI standard si applicano anche ai file RMID.</span><span class="sxs-lookup"><span data-stu-id="c30bb-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="c30bb-124">Per altre informazioni sui file RIFF, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="c30bb-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="c30bb-125">Sebbene esistano attualmente tre tipi di file MIDI standard, MCI sequencer ne riproduce solo due: formato 0 e formato 1 file MIDI.</span><span class="sxs-lookup"><span data-stu-id="c30bb-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="c30bb-126">Per ulteriori informazioni sul controllo dei dispositivi multimediali (inclusi i sequencer) utilizzando i comandi MCI, vedere [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="c30bb-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 




