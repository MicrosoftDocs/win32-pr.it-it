---
title: Creazione di file MIDI
description: Creazione di file MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Multimedia di Windows, creazione di file MIDI
- Multimedia, creazione di file MIDI
- audio multimediale, creazione di file MIDI
- audio, creazione di file MIDI
- MIDI (Musical Instrument Digital Interface), creazione di file
- MIDI (Musical Instrument Digital Interface), creazione di file
- creazione di file MIDI, informazioni
- Associazione MIDI Manufacturers (MMA)
- MMA (associazione MIDI Manufacturers)
- Specifica MIDI dettagliata
- Specifica dei file MIDI standard
- Specifica MIDI (GM) generale
- Specifica GM (MIDI generale)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044434"
---
# <a name="creating-midi-files"></a><span data-ttu-id="3e1cb-116">Creazione di file MIDI</span><span class="sxs-lookup"><span data-stu-id="3e1cb-116">Creating MIDI Files</span></span>

<span data-ttu-id="3e1cb-117">Le specifiche MIDI (Musical Instrument Digital Interface) sono pubblicate da e sono materiale protetto da copyright di MIDI Manufacturers Association (MMA).</span><span class="sxs-lookup"><span data-stu-id="3e1cb-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="3e1cb-118">Nell'elenco seguente vengono descritte le specifiche che hanno il maggior interesse generale:</span><span class="sxs-lookup"><span data-stu-id="3e1cb-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="3e1cb-119">Specifica MIDI dettagliata</span><span class="sxs-lookup"><span data-stu-id="3e1cb-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="3e1cb-120">La specifica MIDI descrive i protocolli hardware e software MIDI.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="3e1cb-121">Questa operazione è utile per gli utenti che sviluppano applicazioni multimediali che implementano il supporto MIDI usando funzioni MIDI per registrare, modificare e/o riprodurre dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="3e1cb-122">File MIDI standard 1,0</span><span class="sxs-lookup"><span data-stu-id="3e1cb-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="3e1cb-123">La specifica dei file MIDI standard definisce un modo per interscambiare i dati MIDI con timestamp tra applicazioni diverse su piattaforme hardware identiche o diverse.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="3e1cb-124">Questa operazione è utile per gli sviluppatori che scrivono applicazioni che leggono e analizzano i file su disco contenenti dati MIDI e/o scrivono file di dati MIDI su disco.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="3e1cb-125">Sistema MIDI generale di livello 1</span><span class="sxs-lookup"><span data-stu-id="3e1cb-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="3e1cb-126">La specifica generale MIDI (GM) definisce una configurazione MIDI minima di un "sistema MIDI generale".</span><span class="sxs-lookup"><span data-stu-id="3e1cb-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="3e1cb-127">Questo sistema è costituito da una classe specifica di dispositivi di riproduzione MIDI ed è di particolare interesse per gli sviluppatori di contenuti multimediali che creano file MIDI.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="3e1cb-128">La maggior parte delle schede audio e dei sintetizzatori MIDI del PC prodotti attualmente sono compatibili con la specifica GM.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="3e1cb-129">I file MIDI che vengono creati nella specifica GM dovrebbero in genere suonare come se fossero progettati per il suono, indipendentemente dal dispositivo compatibile con GM su cui sono stati riprodotti.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="3e1cb-130">Per consentire ai file MIDI di essere un formato valido per rappresentare la musica nell'elaborazione multimediale, Windows segue la specifica generale MIDI System Level 1.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="3e1cb-131">Negli argomenti seguenti vengono fornite linee guida per la creazione di MIDI aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="3e1cb-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="3e1cb-132">Linee guida per la creazione di file MIDI</span><span class="sxs-lookup"><span data-stu-id="3e1cb-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="3e1cb-133">Assegnazioni di patch MIDI standard</span><span class="sxs-lookup"><span data-stu-id="3e1cb-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="3e1cb-134">Assegnazioni di chiavi MIDI standard</span><span class="sxs-lookup"><span data-stu-id="3e1cb-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 




