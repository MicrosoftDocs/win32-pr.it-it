---
title: Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono
description: Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Formato di sistemi avanzati (ASF), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), ricerca di codici temporali SMPTE
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- lettori asincroni, ricerca di codici temporali SMPTE
- Reader asincroni, codici temporali SMPTE
- Codici di ora SMPTE, ricerca
- Codici temporali SMPTE, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398544"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="77cdc-113">Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="77cdc-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="77cdc-114">L'oggetto Reader può eseguire ricerche in un punto in un file in base al codice ora SMPTE associato a un flusso video.</span><span class="sxs-lookup"><span data-stu-id="77cdc-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="77cdc-115">I dati del codice temporale sono incapsulati nelle strutture di [**\_ dati dell' \_ estensione \_ del timecode WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , associate a esempi video come estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="77cdc-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="77cdc-116">I codici temporali SMPTE sono definiti da un intervallo e da un codice temporale all'interno di tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="77cdc-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="77cdc-117">Un intervallo è una serie continua di codici temporali.</span><span class="sxs-lookup"><span data-stu-id="77cdc-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="77cdc-118">Ogni volta che il codice viene definito da ore, minuti, secondi e frame.</span><span class="sxs-lookup"><span data-stu-id="77cdc-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="77cdc-119">Per cercare i dati in un file ASF dal codice ora SMPTE usando il Reader asincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="77cdc-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="77cdc-120">Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="77cdc-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="77cdc-121">Impostare il codice dell'ora di inizio e la durata chiamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="77cdc-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="77cdc-122">È necessario specificare il numero di flusso di un flusso video indicizzato dal codice temporale.</span><span class="sxs-lookup"><span data-stu-id="77cdc-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="77cdc-123">Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="77cdc-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="77cdc-124">Gestire gli esempi normalmente nell'implementazione del metodo **IWMReaderCallback:: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="77cdc-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77cdc-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77cdc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77cdc-126">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="77cdc-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="77cdc-127">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="77cdc-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="77cdc-128">**Supporto del codice ora SMPTE**</span><span class="sxs-lookup"><span data-stu-id="77cdc-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




