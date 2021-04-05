---
title: Per recuperare esempi di supporti con il Reader asincrono
description: Per recuperare esempi di supporti con il Reader asincrono
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi di supporti
- ASF (Advanced Systems Format), recupero di esempi di supporti
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, recupero di esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046293"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="d09ec-108">Per recuperare esempi di supporti con il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="d09ec-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="d09ec-109">Dopo aver ricevuto il messaggio di \_ stato WMT aperto nell'implementazione di [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), è possibile iniziare a ricevere esempi chiamando [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span><span class="sxs-lookup"><span data-stu-id="d09ec-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="d09ec-110">Il lettore asincrono recapita esempi all'implementazione di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="d09ec-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="d09ec-111">Gli esempi vengono recapitati in ordine temporale di presentazione.</span><span class="sxs-lookup"><span data-stu-id="d09ec-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="d09ec-112">**Start** è una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="d09ec-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="d09ec-113">Verrà restituito quasi immediatamente e continuerà a essere eseguito su thread separati.</span><span class="sxs-lookup"><span data-stu-id="d09ec-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="d09ec-114">Il lettore asincrono usa più thread durante la decodifica del contenuto e la distribuzione di esempi.</span><span class="sxs-lookup"><span data-stu-id="d09ec-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="d09ec-115">Quando viene raggiunta la fine del file, il lettore invia un \_ messaggio di stato WMT EOF all'implementazione del callback **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="d09ec-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="d09ec-116">Quando \_ si invia WMT EOF, il lettore interrompe la propria elaborazione; non è necessario rispondere a WMT \_ EOF con una chiamata a [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span><span class="sxs-lookup"><span data-stu-id="d09ec-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d09ec-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d09ec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09ec-118">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="d09ec-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="d09ec-119">**Per implementare i messaggi del lettore nel callback OnStatus**</span><span class="sxs-lookup"><span data-stu-id="d09ec-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="d09ec-120">**Per implementare il callback OnSample**</span><span class="sxs-lookup"><span data-stu-id="d09ec-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




