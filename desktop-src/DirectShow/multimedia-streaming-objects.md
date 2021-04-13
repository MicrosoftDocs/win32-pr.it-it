---
description: Oggetti streaming multimediali
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Oggetti streaming multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351686"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="798c0-103">Oggetti streaming multimediali</span><span class="sxs-lookup"><span data-stu-id="798c0-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="798c0-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="798c0-104">This API is deprecated.</span></span> <span data-ttu-id="798c0-105">Le nuove applicazioni non devono utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="798c0-105">New applications should not use it.</span></span>

 

<span data-ttu-id="798c0-106">Nella tabella seguente vengono descritti gli oggetti di streaming multimediali.</span><span class="sxs-lookup"><span data-stu-id="798c0-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="798c0-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="798c0-107">CLSID</span></span></th>
<th><span data-ttu-id="798c0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="798c0-108">Description</span></span></th>
<th><span data-ttu-id="798c0-109">Interfacce supportate</span><span class="sxs-lookup"><span data-stu-id="798c0-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="798c0-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="798c0-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="798c0-111">Consente di creare esempi di supporti per qualsiasi tipo di dati supportato da DirectShow</span><span class="sxs-lookup"><span data-stu-id="798c0-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="798c0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="798c0-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="798c0-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="798c0-117">Implementazione dell'oggetto contenitore audio <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="798c0-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="798c0-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="798c0-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="798c0-120">Flusso multimediale DirectDraw che può essere aggiunto a un flusso multimediale DirectShow.</span><span class="sxs-lookup"><span data-stu-id="798c0-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="798c0-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="798c0-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="798c0-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="798c0-127">Implementazione di DirectShow del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="798c0-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="798c0-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="798c0-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="798c0-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="798c0-131">Fornisce funzionalità di streaming multimediale per l'oggetto CLSID_AMMultiMediaStream tramite l'interfaccia <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="798c0-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="798c0-133">N/D</span><span class="sxs-lookup"><span data-stu-id="798c0-133">N/A</span></span></td>
<td><span data-ttu-id="798c0-134">Esempi creati dall'oggetto CLSID_AMMediaTypeStream.</span><span class="sxs-lookup"><span data-stu-id="798c0-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="798c0-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="798c0-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="798c0-138">N/D</span><span class="sxs-lookup"><span data-stu-id="798c0-138">N/A</span></span></td>
<td><span data-ttu-id="798c0-139">Esempi creati dal flusso DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="798c0-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="798c0-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="798c0-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="798c0-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="798c0-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



