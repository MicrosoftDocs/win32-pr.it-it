---
description: Filtro navigatore DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro navigatore DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481853"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="43d8f-103">Filtro navigatore DVD</span><span class="sxs-lookup"><span data-stu-id="43d8f-103">DVD Navigator Filter</span></span>

<span data-ttu-id="43d8f-104">Il filtro di spostamento DVD è il filtro di origine per un grafico filtro di riproduzione DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="43d8f-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="43d8f-105">Apre tutti i file necessari in un volume di DVD-Video, naviga nei file Linear DVD-Video. VOB e analizza il flusso di programma MPEG-2 risultante, suddividendo il flusso in tre pin di output (video, audio, sottoimmagine).</span><span class="sxs-lookup"><span data-stu-id="43d8f-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="43d8f-106">Il filtro di spostamento DVD implementa anche le interfacce [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) che consentono a un'applicazione di riproduzione DVD di controllare DVD-Video la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="43d8f-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43d8f-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="43d8f-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="43d8f-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDVDControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d8f-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="43d8f-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="43d8f-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="43d8f-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43d8f-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="43d8f-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="43d8f-112">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="43d8f-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d8f-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="43d8f-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="43d8f-114">Tipi di base:</span><span class="sxs-lookup"><span data-stu-id="43d8f-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="43d8f-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="43d8f-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="43d8f-117">Immagine subimmagine: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="43d8f-118">Tipi estesi:</span><span class="sxs-lookup"><span data-stu-id="43d8f-118">Extended types:</span></span><br/> <span data-ttu-id="43d8f-119">Video:</span><span class="sxs-lookup"><span data-stu-id="43d8f-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="43d8f-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="43d8f-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="43d8f-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="43d8f-123">Audio:</span><span class="sxs-lookup"><span data-stu-id="43d8f-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="43d8f-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="43d8f-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="43d8f-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="43d8f-127">Sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="43d8f-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="43d8f-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="43d8f-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="43d8f-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="43d8f-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="43d8f-131">Per abilitare i tipi estesi, chiamare <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDVDControl2:: SetOption</strong></a> e impostare il</span><span class="sxs-lookup"><span data-stu-id="43d8f-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43d8f-132">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="43d8f-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="43d8f-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="43d8f-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d8f-134">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="43d8f-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="43d8f-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="43d8f-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43d8f-136">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="43d8f-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="43d8f-137">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="43d8f-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d8f-138">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="43d8f-138">Executable</span></span></td>
<td><span data-ttu-id="43d8f-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="43d8f-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43d8f-140"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="43d8f-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="43d8f-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="43d8f-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d8f-142"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="43d8f-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="43d8f-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="43d8f-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="43d8f-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43d8f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43d8f-145">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="43d8f-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="43d8f-146">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="43d8f-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




