---
description: Supporto ASF in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Supporto ASF in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320564"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="f113a-103">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f113a-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="f113a-104">Media Foundation supporta i file multimediali nel formato ASF (Advanced Systems Format):</span><span class="sxs-lookup"><span data-stu-id="f113a-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="f113a-105">Windows Media Video (file WMV)</span><span class="sxs-lookup"><span data-stu-id="f113a-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="f113a-106">Windows Media Audio (file WMA)</span><span class="sxs-lookup"><span data-stu-id="f113a-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="f113a-107">Media Foundation fornisce diversi oggetti per la lettura e la scrittura di file ASF.</span><span class="sxs-lookup"><span data-stu-id="f113a-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="f113a-108">Questi oggetti sono disponibili in due livelli architetturali diversi.</span><span class="sxs-lookup"><span data-stu-id="f113a-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="f113a-109">In primo luogo, il livello della *pipeline* contiene gli oggetti che funzionano all'interno della [pipeline Media Foundation](media-foundation-pipeline.md) e sono conformi alle API definite dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f113a-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="f113a-110">Il livello della pipeline ASF contiene:</span><span class="sxs-lookup"><span data-stu-id="f113a-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="f113a-111">[Origine multimediale ASF](asf-media-source.md): analizza i file ASF e recapita i pacchetti di dati audio/video.</span><span class="sxs-lookup"><span data-stu-id="f113a-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="f113a-112">[Codec Windows Media](windows-media-codecs.md): decodifica o codifica i flussi audio o video di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f113a-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="f113a-113">[Sink multimediale ASF](asf-media-sinks.md): riceve i pacchetti di dati e scrive un file ASF.</span><span class="sxs-lookup"><span data-stu-id="f113a-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="f113a-114">In secondo luogo, il livello contenitore WM fornisce il controllo di basso livello sull'analisi e la scrittura di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="f113a-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="f113a-115">Il livello della pipeline utilizza WMContainer internamente.</span><span class="sxs-lookup"><span data-stu-id="f113a-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="f113a-116">Le applicazioni possono anche usare WMContainer per l'analisi e la scrittura di basso livello ASF.</span><span class="sxs-lookup"><span data-stu-id="f113a-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![diagramma che Mostra gli elementi del livello pipeline e il contenitore WM](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="f113a-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f113a-118">In this section</span></span>



| <span data-ttu-id="f113a-119">Argomento</span><span class="sxs-lookup"><span data-stu-id="f113a-119">Topic</span></span>                                                                         | <span data-ttu-id="f113a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f113a-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f113a-121">Struttura di file ASF</span><span class="sxs-lookup"><span data-stu-id="f113a-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="f113a-122">Cenni preliminari sulla struttura dei file ASF e sugli oggetti forniti da Media Foundation per lavorare con i file ASF.</span><span class="sxs-lookup"><span data-stu-id="f113a-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="f113a-123">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="f113a-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="f113a-124">Viene descritto come analizzare e creare file ASF utilizzando il livello pipeline.</span><span class="sxs-lookup"><span data-stu-id="f113a-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="f113a-125">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="f113a-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="f113a-126">Viene descritto come analizzare e creare file ASF usando il livello WMContainer.</span><span class="sxs-lookup"><span data-stu-id="f113a-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="f113a-127">Per informazioni dettagliate sulla struttura di un file ASF, vedere la specifica ASF, che può essere scaricata da questo [sito Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="f113a-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f113a-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f113a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f113a-129">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f113a-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




