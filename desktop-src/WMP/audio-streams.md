---
title: Flussi audio
description: Flussi audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online Store, flussi audio
- archivi online, flussi audio
- digitare 1 negozi online, flussi audio
- Windows Media Player Online Stores, flussi da server musicali
- archivi online, flussi da server musicali
- digitare 1 archivi online, flussi da server musicali
- Windows Media Player Online Stores, flussi server musicali
- archivi online, flussi di server musicali
- digitare 1 archivi online, flussi di server musicali
- flussi audio
- flussi di Music Server
- flussi da server musicali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046333"
---
# <a name="audio-streams"></a><span data-ttu-id="c22b0-115">Flussi audio</span><span class="sxs-lookup"><span data-stu-id="c22b0-115">Audio Streams</span></span>

<span data-ttu-id="c22b0-116">Gli archivi online possono fornire musica come flusso da un server musicale.</span><span class="sxs-lookup"><span data-stu-id="c22b0-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="c22b0-117">Questa operazione è utile per fornire esempi, articoli promozionali speciali o per consentire agli utenti della sottoscrizione di usufruire di musica senza dover scaricare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c22b0-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="c22b0-118">Spesso non è possibile archiviare l'URL del flusso come parte del catalogo musicale, bensì per risolvere l'URL immediatamente prima della riproduzione in base all'ID traccia.</span><span class="sxs-lookup"><span data-stu-id="c22b0-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="c22b0-119">Per abilitare questa operazione, Windows Media Player chiama [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) e fornisce il tipo di flusso (come valore di enumerazione [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) e l'ID per il flusso.</span><span class="sxs-lookup"><span data-stu-id="c22b0-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="c22b0-120">Il plug-in restituisce l'URL per il flusso tramite il parametro *pbstrURL* .</span><span class="sxs-lookup"><span data-stu-id="c22b0-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22b0-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c22b0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22b0-122">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="c22b0-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




