---
title: Creazione di grafici di filtro per la scrittura di file ASF (QASF)
description: Creazione di grafici di filtro per la scrittura di file ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media Format SDK, creazione di grafici di filtro (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, scrittura di file ASF (QASF)
- ASF (Advanced Systems Format), creazione di grafici di filtri (QASF)
- ASF (Advanced Systems Format), compilazione di grafici di filtro (QASF)
- Formato Advanced Systems (ASF), scrittura (QASF)
- ASF (Advanced Systems Format), scrittura (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, creazione di grafici di filtri (QASF)
- DirectShow, scrittura di file ASF (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297743"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="81bea-118">Creazione di grafici di filtro per la scrittura di file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="81bea-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="81bea-119">Le applicazioni basate su DirectShow usano in genere uno dei tre tipi di grafico di filtro durante la creazione di contenuto basato su Windows Media:</span><span class="sxs-lookup"><span data-stu-id="81bea-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="81bea-120">Filtrare i grafici per la conversione o la transcodifica del contenuto da un altro formato in formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81bea-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="81bea-121">Filtrare i grafici per l'inserimento di contenuto non basato su Windows Media (formati di flusso nativo) in file ASF.</span><span class="sxs-lookup"><span data-stu-id="81bea-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="81bea-122">Filtrare i grafici per l'acquisizione dei dati dinamici e codificarli immediatamente nel formato Windows Media prima di salvarli su disco.</span><span class="sxs-lookup"><span data-stu-id="81bea-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="81bea-123">Ogni tipo di grafico di filtro viene descritto più dettagliatamente nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="81bea-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="81bea-124">Sezione</span><span class="sxs-lookup"><span data-stu-id="81bea-124">Section</span></span>                                                                                                             | <span data-ttu-id="81bea-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81bea-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81bea-126">Transcodifica di file (QASF)</span><span class="sxs-lookup"><span data-stu-id="81bea-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="81bea-127">Viene descritto come creare grafici di filtri per la transcodifica di file.</span><span class="sxs-lookup"><span data-stu-id="81bea-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="81bea-128">Inserimento di formati di flusso nativi in file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="81bea-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="81bea-129">Viene descritto come inserire qualsiasi tipo di dati audio o video compressi o non compressi in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="81bea-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="81bea-130">Acquisizione diretta da un dispositivo a un file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="81bea-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="81bea-131">Viene descritto come creare grafici del filtro di acquisizione che restituiscono un file ASF.</span><span class="sxs-lookup"><span data-stu-id="81bea-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




