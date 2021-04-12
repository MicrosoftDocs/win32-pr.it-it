---
title: Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono
description: Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Formato di sistemi avanzati (ASF), ricerca per numero di frame
- ASF (Advanced Systems Format), ricerca per numero di frame
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, ricerca per numero di frame
- flussi video, ricerca per numero di frame
- flussi video, lettori sincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336321"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="24009-110">Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="24009-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="24009-111">Per cercare i dati in base al numero di frame utilizzando il lettore sincrono, è necessario specificare un intervallo per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="24009-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="24009-112">Un intervallo è definito da un numero di frame iniziale in un flusso video specifico e da un numero di frame da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="24009-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="24009-113">Per cercare i dati in un file ASF in base al numero di frame usando il lettore sincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="24009-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="24009-114">Impostare il numero del fotogramma iniziale e il numero di fotogrammi da leggere per il recapito di esempio chiamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="24009-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="24009-115">È necessario specificare il numero di flusso di un flusso video indicizzato con frame.</span><span class="sxs-lookup"><span data-stu-id="24009-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="24009-116">Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="24009-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="24009-117">Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="24009-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="24009-118">Procedere normalmente con il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="24009-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24009-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24009-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24009-120">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="24009-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="24009-121">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="24009-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




