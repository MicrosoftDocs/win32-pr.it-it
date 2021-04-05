---
title: Per eseguire ricerche in base al tempo tramite il lettore sincrono
description: Per eseguire ricerche in base al tempo tramite il lettore sincrono
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Formato Advanced Systems (ASF), ricerca per ora
- ASF (Advanced Systems Format), ricerca per ora
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, ricerca per ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723559"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="0f2a5-108">Per eseguire ricerche in base al tempo tramite il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0f2a5-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="0f2a5-109">Per cercare i dati utilizzando il lettore sincrono, è necessario specificare un intervallo per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="0f2a5-110">Un intervallo è definito da un'ora di presentazione iniziale e da una durata, entrambe in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="0f2a5-111">Per cercare i dati in un file ASF in base all'ora di presentazione usando il lettore sincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="0f2a5-112">Specificare l'ora di inizio e la durata per il recapito di esempio chiamando [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span><span class="sxs-lookup"><span data-stu-id="0f2a5-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="0f2a5-113">Questo metodo non richiede di specificare un numero di flusso perché le ore di presentazione di ogni flusso devono essere già sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="0f2a5-114">Iniziare il recupero degli esempi con le chiamate a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="0f2a5-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="0f2a5-115">Procedere normalmente con il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f2a5-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f2a5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2a5-117">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="0f2a5-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="0f2a5-118">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="0f2a5-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




