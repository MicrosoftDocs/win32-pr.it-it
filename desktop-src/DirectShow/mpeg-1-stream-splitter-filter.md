---
description: Filtro del separatore di flusso MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro del separatore di flusso MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125220"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="8eead-103">Filtro del separatore di flusso MPEG-1</span><span class="sxs-lookup"><span data-stu-id="8eead-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="8eead-104">Questo filtro suddivide un flusso di sistema MPEG-1 nei flussi audio e video dei componenti.</span><span class="sxs-lookup"><span data-stu-id="8eead-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8eead-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="8eead-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="8eead-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="8eead-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eead-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="8eead-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="8eead-108">Tipo principale: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="8eead-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="8eead-109">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="8eead-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="8eead-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="8eead-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="8eead-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="8eead-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="8eead-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="8eead-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="8eead-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="8eead-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="8eead-114">Vedere <a href="mpeg-1-media-types.md"> <strong>tipi di supporto MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8eead-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eead-115">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="8eead-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="8eead-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="8eead-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eead-117">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="8eead-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="8eead-118">Tipo principale: MEDIATYPE_Audio o MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="8eead-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="8eead-119">Sottotipo: MEDIASUBTYPE_MPEG1Payload o MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="8eead-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="8eead-120">Vedere <a href="mpeg-1-media-types.md"> <strong>tipi di supporto MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8eead-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eead-121">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="8eead-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="8eead-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="8eead-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eead-123">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="8eead-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="8eead-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="8eead-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eead-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8eead-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="8eead-126">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8eead-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eead-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="8eead-127">Executable</span></span></td>
<td><span data-ttu-id="8eead-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="8eead-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eead-129"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="8eead-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="8eead-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="8eead-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eead-131"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="8eead-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="8eead-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8eead-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8eead-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eead-133">Remarks</span></span>

<span data-ttu-id="8eead-134">Questo file supporta solo la modalità pull tramite [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; non supporta la modalità push.</span><span class="sxs-lookup"><span data-stu-id="8eead-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="8eead-135">Poiché il contenuto MPEG-1 non è indicizzato, la ricerca può essere molto approssimativa.</span><span class="sxs-lookup"><span data-stu-id="8eead-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="8eead-136">È in genere ideale per un flusso di sistema MPEG-1 a bitrate fisso, che in genere è hardware generato per il CD video.</span><span class="sxs-lookup"><span data-stu-id="8eead-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="8eead-137">Il filtro supporta l'interfaccia [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) per il recupero dei metadati ID3.</span><span class="sxs-lookup"><span data-stu-id="8eead-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="8eead-138">Non tutti i campioni MPEG hanno timestamp.</span><span class="sxs-lookup"><span data-stu-id="8eead-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="8eead-139">La mancanza di un timestamp di un esempio MPEG non è un errore.</span><span class="sxs-lookup"><span data-stu-id="8eead-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="8eead-140">Per gli sviluppatori di filtri, ciò significa che non è necessario restituire un codice di errore dal metodo **Receive** del PIN di input se [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8eead-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="8eead-141">Se **Receive** restituisce un valore diverso da S \_ OK, la barra di divisione interrompe l'invio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="8eead-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="8eead-142">Se il file contiene un flusso video, la barra di divisione MPEG-1 Stream supporta la ricerca in base al numero di frame.</span><span class="sxs-lookup"><span data-stu-id="8eead-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="8eead-143">Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore **\_ format time format \_ frame**.</span><span class="sxs-lookup"><span data-stu-id="8eead-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eead-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8eead-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eead-145">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="8eead-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




