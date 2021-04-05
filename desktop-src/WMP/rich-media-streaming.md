---
title: Streaming multimediale avanzato
description: Streaming multimediale avanzato
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, presentazioni basate sul Web
- Modello a oggetti di Windows Media Player, presentazioni basate sul Web
- modello a oggetti, presentazioni basate sul Web
- Presentazioni Windows Media Player per dispositivi mobili, basate sul Web
- Windows Media Player ActiveX Control, presentazioni basate sul Web
- Controllo ActiveX Windows Media Player Mobile, presentazioni basate sul Web
- Controllo ActiveX, presentazioni basate sul Web
- Windows Media Player, streaming multimediale avanzato
- Modello a oggetti di Windows Media Player, streaming multimediale avanzato
- modello a oggetti, flusso multimediale avanzato
- Windows Media Player Mobile, streaming multimediale avanzato
- Controllo ActiveX di Windows Media Player, streaming multimediale avanzato
- Controllo ActiveX Windows Media Player Mobile, streaming multimediale avanzato
- Controllo ActiveX, streaming multimediale avanzato
- Presentazioni basate sul Web, streaming multimediale avanzato
- creazione di presentazioni basate sul Web, streaming multimediale avanzato
- streaming multimediale avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712715"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="91650-120">Streaming multimediale avanzato</span><span class="sxs-lookup"><span data-stu-id="91650-120">Rich Media Streaming</span></span>

<span data-ttu-id="91650-121">Le pagine Web complesse contengono molti componenti diversi, normalmente trasferiti separatamente.</span><span class="sxs-lookup"><span data-stu-id="91650-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="91650-122">In una connessione lenta, tali pagine visualizzano una parte alla volta e possono richiedere alcuni minuti per la visualizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="91650-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="91650-123">Questo potrebbe impedire di sincronizzare efficacemente le pagine Web con i supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="91650-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="91650-124">La soluzione a questo problema è costituita da flussi multimediali avanzati, ovvero l'aggiunta di pagine Web al flusso multimediale digitale, in modo che vengano recapitate contemporaneamente ai dati audio o video.</span><span class="sxs-lookup"><span data-stu-id="91650-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="91650-125">Lo streaming multimediale avanzato usa un layout con frame semplice e si comporta esattamente come il normale capovolgimento degli URL.</span><span class="sxs-lookup"><span data-stu-id="91650-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="91650-126">Analogamente al capovolgimento degli URL, i comandi di script URL incorporati nei flussi multimediali digitali vengono usati per visualizzare il contenuto nel frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91650-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="91650-127">Anziché puntare a pagine sul Web, tuttavia, i comandi script URL vengono usati da Windows Media Player 9 Series o versioni successive per accedere ai file nella cache di Internet Explorer in cui viene inserito il contenuto HTML trasmesso al momento della ricezione.</span><span class="sxs-lookup"><span data-stu-id="91650-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="91650-128">Analogamente al normale capovolgimento degli URL, è possibile scrivere i gestori eventi che rispondono a questi comandi di script URL oppure è possibile consentire al controllo Media Player di Windows di gestire tutti gli elementi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91650-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="91650-129">Qualsiasi contenuto HTML distribuito attraverso flussi multimediali avanzati viene riprodotto nell'area di sicurezza Internet ed è soggetto alle impostazioni di sicurezza del browser dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91650-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="91650-130">Per ulteriori informazioni sulla creazione di presentazioni multimediali avanzate, vedere la serie Windows Media Format 9 o versioni successive SDK e Windows Media Encoder 9 Series SDK.</span><span class="sxs-lookup"><span data-stu-id="91650-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91650-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91650-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91650-132">**Creazione di presentazioni Web-Based**</span><span class="sxs-lookup"><span data-stu-id="91650-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="91650-133">**Uso dello script per controllare il capovolgimento degli URL**</span><span class="sxs-lookup"><span data-stu-id="91650-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




