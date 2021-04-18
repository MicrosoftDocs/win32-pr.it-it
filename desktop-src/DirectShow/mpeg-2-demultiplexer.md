---
description: Questo filtro demultiplexa i flussi del trasporto e del programma MPEG-2 recapitati in modalità push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303990"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="1a52a-103">MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="1a52a-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="1a52a-104">Questo filtro demultiplexa i flussi del trasporto e del programma MPEG-2 recapitati in modalità push.</span><span class="sxs-lookup"><span data-stu-id="1a52a-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="1a52a-105">A partire da Windows XP, questo filtro supporta anche i flussi di programma in modalità pull (riproduzione di file).</span><span class="sxs-lookup"><span data-stu-id="1a52a-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="1a52a-106">Sulle piattaforme precedenti, usare il filtro per la [barra di divisione MPEG-2](mpeg-2-splitter.md) per i flussi di programma in modalità pull.</span><span class="sxs-lookup"><span data-stu-id="1a52a-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="1a52a-107">Questo filtro può essere usato in qualsiasi tipo di grafico filtro, incluso un grafico del filtro Digital TV BDA.</span><span class="sxs-lookup"><span data-stu-id="1a52a-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="1a52a-108">Il Demultiplexer MPEG-2 non supporta la ricerca con precisione dei frame.</span><span class="sxs-lookup"><span data-stu-id="1a52a-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a52a-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1a52a-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1a52a-110">Tutte le modalità:</span><span class="sxs-lookup"><span data-stu-id="1a52a-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="1a52a-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="1a52a-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="1a52a-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="1a52a-113">Solo modalità push:</span><span class="sxs-lookup"><span data-stu-id="1a52a-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="1a52a-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="1a52a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="1a52a-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52a-117">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1a52a-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1a52a-118">Tipo principale: MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="1a52a-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="1a52a-119">Sottotipo</span><span class="sxs-lookup"><span data-stu-id="1a52a-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="1a52a-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="1a52a-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="1a52a-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="1a52a-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="1a52a-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="1a52a-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="1a52a-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="1a52a-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="1a52a-124">Per ulteriori informazioni, vedere la pagina relativa ai <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipi di supporti MPEG-2 Demultiplexer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1a52a-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52a-125">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1a52a-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1a52a-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52a-127">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1a52a-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1a52a-128">I flussi audio e video Elementary devono avere un tipo principale di MEDIATYPE_Audio o MEDIATYPE_Video.</span><span class="sxs-lookup"><span data-stu-id="1a52a-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="1a52a-129">Per ulteriori informazioni, vedere la pagina relativa ai <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipi di supporti MPEG-2 Demultiplexer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1a52a-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52a-130">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1a52a-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1a52a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, solo modalità push <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="1a52a-132">Solo modalità pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52a-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52a-133">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1a52a-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="1a52a-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="1a52a-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52a-135">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1a52a-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1a52a-136">Disponibile solo per i test.</span><span class="sxs-lookup"><span data-stu-id="1a52a-136">Available for testing only.</span></span> <span data-ttu-id="1a52a-137">Usare l'interfaccia <strong>ISpecifyPropertyPages</strong> per accedere alle pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1a52a-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52a-138">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1a52a-138">Executable</span></span></td>
<td><span data-ttu-id="1a52a-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="1a52a-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52a-140"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="1a52a-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1a52a-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="1a52a-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52a-142"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="1a52a-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1a52a-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1a52a-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1a52a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a52a-144">Remarks</span></span>

<span data-ttu-id="1a52a-145">Per restituire flussi audio e video, demux deve ricevere i flussi PCR e SCR.</span><span class="sxs-lookup"><span data-stu-id="1a52a-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="1a52a-146">Sul lato input, questo significa che un flusso di trasporto deve contenere le tabelle PAT e PMT che definiscono il PID per il flusso di PCR. e i flussi del programma devono contenere almeno un'intestazione Pack.</span><span class="sxs-lookup"><span data-stu-id="1a52a-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a52a-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a52a-147">Requirements</span></span>



| <span data-ttu-id="1a52a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a52a-148">Requirement</span></span> | <span data-ttu-id="1a52a-149">Valore</span><span class="sxs-lookup"><span data-stu-id="1a52a-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1a52a-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a52a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1a52a-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1a52a-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1a52a-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a52a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1a52a-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1a52a-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a52a-154">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1a52a-154">End of server support</span></span><br/>    | <span data-ttu-id="1a52a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1a52a-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="1a52a-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a52a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a52a-157">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a52a-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="1a52a-158">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1a52a-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




