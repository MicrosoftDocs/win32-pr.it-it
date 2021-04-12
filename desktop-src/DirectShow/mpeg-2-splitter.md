---
description: Splitter MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Splitter MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225453"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="68aba-103">Splitter MPEG-2</span><span class="sxs-lookup"><span data-stu-id="68aba-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="68aba-104">A partire da Microsoft® Windows® XP, il filtro della barra di divisione MPEG-2 è deprecato.</span><span class="sxs-lookup"><span data-stu-id="68aba-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="68aba-105">Usare invece [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="68aba-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="68aba-106">Nelle piattaforme precedenti usare il separatore MPEG-2 per i flussi di programma MPEG-2 recapitati in modalità pull che contengono almeno uno dei tipi di flusso seguenti: MPEG-2 video; Audio MPEG-2; Audio AC3 codificato come definito per il video DVD; o audio PCM codificato come definito per il video DVD.</span><span class="sxs-lookup"><span data-stu-id="68aba-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="68aba-107">Questo filtro analizza i flussi, crea un pin di output per ogni flusso e genera i pacchetti audio o video MPEG compressi in un filtro di decodificatore MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="68aba-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="68aba-108">Per i flussi di programma e trasporto distribuiti in modalità push, usare il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md)su tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="68aba-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="68aba-109">Il separatore MPEG-2 non supporta la ricerca con precisione dei frame.</span><span class="sxs-lookup"><span data-stu-id="68aba-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68aba-110">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="68aba-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="68aba-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span><span class="sxs-lookup"><span data-stu-id="68aba-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68aba-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="68aba-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="68aba-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="68aba-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="68aba-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="68aba-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="68aba-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="68aba-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68aba-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="68aba-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="68aba-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="68aba-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68aba-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="68aba-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="68aba-119">Dipende dal tipo di flusso.</span><span class="sxs-lookup"><span data-stu-id="68aba-119">Depends on the stream type.</span></span> <span data-ttu-id="68aba-120">Vedere <a href="mpeg-2-splitter-media-types.md">tipi di supporti Splitter MPEG-2</a></span><span class="sxs-lookup"><span data-stu-id="68aba-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68aba-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="68aba-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="68aba-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="68aba-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68aba-123">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="68aba-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="68aba-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="68aba-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68aba-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="68aba-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="68aba-126">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="68aba-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68aba-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="68aba-127">Executable</span></span></td>
<td><span data-ttu-id="68aba-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="68aba-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68aba-129"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="68aba-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="68aba-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="68aba-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68aba-131"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="68aba-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="68aba-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="68aba-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="68aba-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68aba-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68aba-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="68aba-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="68aba-135">Uso della barra di divisione MPEG-2</span><span class="sxs-lookup"><span data-stu-id="68aba-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



