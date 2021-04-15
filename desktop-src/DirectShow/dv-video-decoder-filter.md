---
description: Filtro decodificatore video DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro decodificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520465"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="26812-103">Filtro decodificatore video DV</span><span class="sxs-lookup"><span data-stu-id="26812-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="26812-104">Questo filtro decodifica un flusso video digitale (DV) in un video non compresso.</span><span class="sxs-lookup"><span data-stu-id="26812-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26812-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="26812-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="26812-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="26812-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26812-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="26812-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="26812-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="26812-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="26812-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="26812-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="26812-110">FORMAT_VideoInfo, FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="26812-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26812-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="26812-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="26812-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="26812-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26812-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="26812-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="26812-114"><strong>Tipo principale</strong>:<strong>sottotipi</strong>MEDIATYPE_Video:</span><span class="sxs-lookup"><span data-stu-id="26812-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="26812-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="26812-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="26812-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="26812-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="26812-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="26812-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="26812-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="26812-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="26812-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="26812-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="26812-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="26812-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="26812-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="26812-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="26812-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="26812-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="26812-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="26812-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="26812-124">
<strong>Tipi di formato</strong>:</span><span class="sxs-lookup"><span data-stu-id="26812-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="26812-125">Format_VideoInfo, Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="26812-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26812-126">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="26812-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="26812-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="26812-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26812-128">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="26812-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="26812-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="26812-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26812-130">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="26812-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="26812-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="26812-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26812-132">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="26812-132">Executable</span></span></td>
<td><span data-ttu-id="26812-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="26812-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26812-134"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="26812-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="26812-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="26812-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26812-136"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="26812-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="26812-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="26812-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="26812-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="26812-138">Remarks</span></span>

<span data-ttu-id="26812-139">Usare l'interfaccia [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) per impostare la risoluzione della decodifica su Full, half size, Quarter size o One-ottave size.</span><span class="sxs-lookup"><span data-stu-id="26812-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="26812-140">**Interlacciamento**: le versioni precedenti del decodificatore deinterlacciano sempre il video.</span><span class="sxs-lookup"><span data-stu-id="26812-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="26812-141">A partire da DirectX 9,0, il decodificatore video DV può mantenere l'interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="26812-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="26812-142">Ciò consente di deinterlacciare il video interlacciato dal renderer video mixing (VMR) per migliorare la qualità del rendering.</span><span class="sxs-lookup"><span data-stu-id="26812-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="26812-143">Per usare questa funzionalità, il filtro downstream deve supportare i formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indicati dal formato del valore \_ VideoInfo2 nel membro **formatType** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="26812-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="26812-144">Con l'output a risoluzione completa, i flag di deinterlacciamento (**dwInterlace**) nella struttura **VIDEOINFOHEADER2** sono impostati su `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , che indica i campi interlacciati.</span><span class="sxs-lookup"><span data-stu-id="26812-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="26812-145">A metà risoluzione o inferiore, **dwInterlace** è impostato su zero, che indica i frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="26812-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26812-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26812-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26812-147">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="26812-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="26812-148">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="26812-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




