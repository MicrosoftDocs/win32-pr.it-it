---
description: Filtro codificatore video DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro codificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965514"
---
# <a name="dv-video-encoder-filter"></a><span data-ttu-id="f2878-103">Filtro codificatore video DV</span><span class="sxs-lookup"><span data-stu-id="f2878-103">DV Video Encoder Filter</span></span>

<span data-ttu-id="f2878-104">Questo filtro codifica un flusso video non compresso in video digitale (DV).</span><span class="sxs-lookup"><span data-stu-id="f2878-104">This filter encodes an uncompressed video stream into digital video (DV).</span></span> <span data-ttu-id="f2878-105">Fornisce un'interfaccia personalizzata, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), per l'impostazione della risoluzione e del formato della codifica.</span><span class="sxs-lookup"><span data-stu-id="f2878-105">It provides a custom interface, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), for setting the encoding resolution and format.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2878-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="f2878-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f2878-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="f2878-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2878-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="f2878-108">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="f2878-109">Tipo principale: MEDIATYPE_VideoThe sottotipi seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="f2878-109">Major type: MEDIATYPE_VideoThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f2878-110">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="f2878-110">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="f2878-111">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="f2878-111">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="f2878-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="f2878-112">MEDIASUBTYPE_RGB555</span></span></li>
</ul></li>
<li><span data-ttu-id="f2878-113">Tipo formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="f2878-113">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2878-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="f2878-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f2878-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2878-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2878-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="f2878-116">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="f2878-117">Tipo principale: MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="f2878-117">Major type: MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="f2878-118">Sottotipo: MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="f2878-118">Subtype: MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="f2878-119">Tipo formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="f2878-119">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2878-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="f2878-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f2878-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2878-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2878-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="f2878-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="f2878-123">CLSID_DVVideoEnc</span><span class="sxs-lookup"><span data-stu-id="f2878-123">CLSID_DVVideoEnc</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2878-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f2878-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f2878-125">CLSID_DVEncPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="f2878-125">CLSID_DVEncPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2878-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="f2878-126">Executable</span></span></td>
<td><span data-ttu-id="f2878-127">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="f2878-127">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2878-128"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="f2878-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f2878-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="f2878-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2878-130"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="f2878-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f2878-131">CLSID_VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="f2878-131">CLSID_VideoCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f2878-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2878-132">Remarks</span></span>

<span data-ttu-id="f2878-133">Per video a 16 bit (MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565), l'input deve essere 720 x 480 pixel per NTSC o 720 x 576 pixel per PAL.</span><span class="sxs-lookup"><span data-stu-id="f2878-133">For 16-bit video (MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565), the input must be 720 x 480 pixels for NTSC, or 720 x 576 pixels for PAL.</span></span> <span data-ttu-id="f2878-134">Per il video a 24 bit, non sono presenti vincoli di dimensione per l'input.</span><span class="sxs-lookup"><span data-stu-id="f2878-134">For 24-bit video, there are no size constraints on the input.</span></span>

<span data-ttu-id="f2878-135">L'output è sempre 720 x 480 per NTSC o 720 x 576 per PAL; il video a 24 bit viene ridimensionato per adattarsi a queste dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f2878-135">The output is always 720 x 480 for NTSC or 720 x 576 for PAL; 24-bit video is scaled to fit these dimensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2878-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2878-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2878-137">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2878-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f2878-138">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2878-138">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




