---
description: Informazioni sull'API transcodifica
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informazioni sull'API transcodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560746"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="a85c7-103">Informazioni sull'API transcodifica</span><span class="sxs-lookup"><span data-stu-id="a85c7-103">About the Transcode API</span></span>

<span data-ttu-id="a85c7-104">Il diagramma seguente illustra il modo in cui l'API transcode è correlata al resto della pipeline di codifica Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a85c7-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![diagramma che mostra l'API transcodifica.](images/encoding08.png)

<span data-ttu-id="a85c7-106">La pipeline di codifica contiene gli oggetti di elaborazione dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a85c7-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="a85c7-107">Origine supporto</span><span class="sxs-lookup"><span data-stu-id="a85c7-107">Media source</span></span>
-   <span data-ttu-id="a85c7-108">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="a85c7-108">Decoder</span></span>
-   <span data-ttu-id="a85c7-109">Video Resizer o ricampionatore audio</span><span class="sxs-lookup"><span data-stu-id="a85c7-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="a85c7-110">Codificatore</span><span class="sxs-lookup"><span data-stu-id="a85c7-110">Encoder</span></span>
-   <span data-ttu-id="a85c7-111">Sink multimediale</span><span class="sxs-lookup"><span data-stu-id="a85c7-111">Media sink</span></span>

<span data-ttu-id="a85c7-112">Il video Resizer è necessario solo se le dimensioni del video di output sono diverse dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a85c7-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="a85c7-113">Il ricampionatore audio è necessario solo se l'audio deve essere ricampionato prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="a85c7-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="a85c7-114">La coppia Decodificatore/codificatore è necessaria per la transcodifica, ma non per remuxing.</span><span class="sxs-lookup"><span data-stu-id="a85c7-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="a85c7-115">La *topologia* di codifica è il set di oggetti pipeline (origine, decodificatore, Resizer, Resampler, codificatore e sink multimediale), più i punti di connessione tra di essi.</span><span class="sxs-lookup"><span data-stu-id="a85c7-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="a85c7-116">Per ulteriori informazioni sulle topologie, vedere [topologie](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="a85c7-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="a85c7-117">Componenti diversi sono responsabili della creazione dei vari oggetti pipeline:</span><span class="sxs-lookup"><span data-stu-id="a85c7-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="a85c7-118">L'applicazione usa in genere il [resolver di origine](source-resolver.md) per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="a85c7-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="a85c7-119">La [sessione multimediale](media-session.md) carica e configura il decodificatore, il ridimensionamento video e il ricampionatore audio.</span><span class="sxs-lookup"><span data-stu-id="a85c7-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="a85c7-120">Internamente, usa il caricatore della topologia a tale scopo (vedere [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="a85c7-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="a85c7-121">L'API transcode carica e configura il codificatore e il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="a85c7-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="a85c7-122">Le applicazioni avanzate possono configurare direttamente il codificatore e il sink multimediale, anziché usare l'API transcode.</span><span class="sxs-lookup"><span data-stu-id="a85c7-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a85c7-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a85c7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a85c7-124">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="a85c7-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="a85c7-125">Uso dell'API transcode</span><span class="sxs-lookup"><span data-stu-id="a85c7-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



