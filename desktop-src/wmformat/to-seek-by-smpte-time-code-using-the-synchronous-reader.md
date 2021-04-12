---
title: Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono
description: Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Formato di sistemi avanzati (ASF), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- lettori sincroni, ricerca di codici temporali SMPTE
- lettori sincroni, codici temporali SMPTE
- Codici di ora SMPTE, ricerca
- Codici temporali SMPTE, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336401"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="021b4-113">Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="021b4-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="021b4-114">L'oggetto Reader sincrono può eseguire ricerche in un punto in un file in base al codice ora SMPTE associato a un flusso video.</span><span class="sxs-lookup"><span data-stu-id="021b4-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="021b4-115">I dati del codice temporale sono incapsulati nelle strutture di [**\_ dati dell' \_ estensione \_ del timecode WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , associate a esempi video come estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="021b4-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="021b4-116">I codici temporali SMPTE sono definiti da un intervallo e da un codice temporale all'interno di tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="021b4-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="021b4-117">Un intervallo è una serie continua di codici temporali.</span><span class="sxs-lookup"><span data-stu-id="021b4-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="021b4-118">Ogni volta che il codice viene definito da ore, minuti, secondi e frame.</span><span class="sxs-lookup"><span data-stu-id="021b4-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="021b4-119">Per cercare i dati in un file ASF dal codice ora SMPTE usando il lettore sincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="021b4-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="021b4-120">Impostare il codice ora di inizio e il codice orario di fine per il recapito di esempio chiamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="021b4-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="021b4-121">È necessario specificare il numero di flusso di un flusso video indicizzato dal codice temporale.</span><span class="sxs-lookup"><span data-stu-id="021b4-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="021b4-122">Il lettore sincrono sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="021b4-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="021b4-123">Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="021b4-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="021b4-124">Procedere normalmente con il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="021b4-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="021b4-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="021b4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="021b4-126">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="021b4-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="021b4-127">**Supporto del codice ora SMPTE**</span><span class="sxs-lookup"><span data-stu-id="021b4-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="021b4-128">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="021b4-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




