---
description: Creazione di un grafico di acquisizione audio con anteprima
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Creazione di un grafico di acquisizione audio con anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965856"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="9f5d4-103">Creazione di un grafico di acquisizione audio con anteprima</span><span class="sxs-lookup"><span data-stu-id="9f5d4-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="9f5d4-104">Il grafico di filtro descritto in [creazione di un grafico di acquisizione audio](creating-an-audio-capture-graph.md) esegue solo l'acquisizione, senza anteprima.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="9f5d4-105">Per visualizzare in anteprima e acquisire allo stesso tempo, è necessario che il grafico di filtro usi il [filtro del Pin Tee infinito](infinite-pin-tee-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9f5d4-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="9f5d4-106">Questo filtro ha un pin di input e crea tutti i pin di output in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="9f5d4-107">(Inizia con un pin di output.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-107">(It starts with one output pin.</span></span> <span data-ttu-id="9f5d4-108">Ogni volta che si connette un pin di output, ne crea un altro. Il filtro del Pin Tee infinito recapita ogni campione che riceve, senza modifiche, attraverso tutti i relativi pin di output.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="9f5d4-109">Connettere il filtro di acquisizione audio al Pin Tee infinito e connettere il pin infinito al multiplexer e al [filtro di renderer DirectSound](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9f5d4-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="9f5d4-110">Connettere il multiplexer al writer di file, come prima.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="9f5d4-111">Il diagramma seguente illustra il grafico filtro risultante per un file AVI.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![grafico di acquisizione audio con anteprima](images/audio-capture-graph.png)

<span data-ttu-id="9f5d4-113">Poiché il renderer DirectSound è il renderer audio predefinito, è possibile chiamare semplicemente il metodo [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) sul pin di output del Pin Tee infinito.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="9f5d4-114">Il gestore del grafico del filtro utilizza la [connessione intelligente](intelligent-connect.md) per creare il renderer, aggiungerlo al grafico di filtro e connettere i pin.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="9f5d4-115">Se si acquisisce audio da un microfono e lo si visualizza in anteprima da un altoparlante nello stesso computer, è possibile creare commenti e suggerimenti audio.</span><span class="sxs-lookup"><span data-stu-id="9f5d4-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9f5d4-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f5d4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f5d4-117">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="9f5d4-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



