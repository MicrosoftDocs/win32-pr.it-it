---
title: Per recuperare esempi di flusso con il lettore sincrono
description: Per recuperare esempi di flusso con il lettore sincrono
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Formato avanzato dei sistemi (ASF), recupero degli esempi di flusso
- ASF (formato avanzato dei sistemi), recupero di esempi di flusso
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, recupero di esempi di flusso
- flussi, recupero di esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117363"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="a035c-109">Per recuperare esempi di flusso con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="a035c-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="a035c-110">Come il Reader asincrono, il lettore sincrono può recuperare esempi per numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="a035c-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="a035c-111">Diversamente dal reader asincrono, il lettore sincrono può recapitare esempi di flusso compressi o decompressi.</span><span class="sxs-lookup"><span data-stu-id="a035c-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="a035c-112">Per ricevere gli esempi di flusso, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="a035c-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="a035c-113">In qualsiasi momento prima o durante la riproduzione, chiamare [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passando il numero di flusso desiderato.</span><span class="sxs-lookup"><span data-stu-id="a035c-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="a035c-114">Recuperare gli esempi con chiamate continue a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="a035c-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="a035c-115">È possibile verificare se un flusso è selezionato per il recapito di esempio chiamando [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span><span class="sxs-lookup"><span data-stu-id="a035c-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a035c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a035c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a035c-117">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="a035c-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="a035c-118">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="a035c-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




