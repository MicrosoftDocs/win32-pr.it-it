---
title: Informazioni sulla discontinuità
description: Informazioni sulla discontinuità
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, discontinuità audio
- Plug-in DSP, discontinuità audio
- plug-in DSP audio, discontinuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395415"
---
# <a name="about-discontinuity"></a><span data-ttu-id="ce9af-108">Informazioni sulla discontinuità</span><span class="sxs-lookup"><span data-stu-id="ce9af-108">About Discontinuity</span></span>

<span data-ttu-id="ce9af-109">In qualsiasi momento, Windows Media Player può segnalare un'interruzione nel flusso di input chiamando il metodo **IMediaObject::D di continuità** .</span><span class="sxs-lookup"><span data-stu-id="ce9af-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="ce9af-110">Questo problema si verifica regolarmente all'inizio e alla fine di un flusso e anche prima di ogni operazione di ricerca o quando il contenuto del flusso viene interrotto per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="ce9af-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="ce9af-111">Il plug-in DSP di esempio generato dalla procedura guidata plug-in di Windows Media Player non deve gestire le discontinuità per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce9af-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="ce9af-112">Gli esempi di PCM sono atomici, ovvero possono essere elaborati indipendentemente dagli altri esempi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="ce9af-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="ce9af-113">Alcuni formati video contengono dati che dipendono da fotogrammi chiave ed esempi compressi.</span><span class="sxs-lookup"><span data-stu-id="ce9af-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="ce9af-114">Il codice di esempio viene scritto per forzare sempre il client a elaborare tutti gli output prima che il plug-in accetti un maggior numero di input.</span><span class="sxs-lookup"><span data-stu-id="ce9af-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="ce9af-115">L'implementazione predefinita di **IMediaObject::D la continuità** restituisce semplicemente S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce9af-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce9af-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce9af-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce9af-117">**Implementazione di un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="ce9af-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




