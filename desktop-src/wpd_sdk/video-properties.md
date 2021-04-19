---
description: Dispositivi portatili Windows supporta le seguenti proprietà video.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Proprietà video (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326590"
---
# <a name="video-properties"></a><span data-ttu-id="1368b-103">Proprietà video</span><span class="sxs-lookup"><span data-stu-id="1368b-103">Video Properties</span></span>

<span data-ttu-id="1368b-104">Dispositivi portatili Windows supporta le seguenti proprietà video.</span><span class="sxs-lookup"><span data-stu-id="1368b-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="1368b-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1368b-105">Property</span></span>                                         | <span data-ttu-id="1368b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="1368b-106">VarType</span></span>        | <span data-ttu-id="1368b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1368b-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1368b-108">**\_autore video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="1368b-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1368b-110">Autore del file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="1368b-111">**\_velocità in \_ bit video WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="1368b-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-112">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-113">Velocità in bit del file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="1368b-114">**\_dimensioni del \_ buffer \_ video WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="1368b-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-115">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-116">Valore che specifica la dimensione del buffer video necessaria per il rendering di questo file.</span><span class="sxs-lookup"><span data-stu-id="1368b-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="1368b-117">**\_crediti video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="1368b-118">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1368b-119">Crediti che elencano il cast e la troupe del video.</span><span class="sxs-lookup"><span data-stu-id="1368b-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="1368b-120">**\_ \_ Codice FourCC video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="1368b-121">**\_DWORD VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="1368b-122">Codice FourCC registrato che indica il codec usato per il file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="1368b-123">Per un elenco dei formati FourCC, vedere l'articolo [codici FourCC registrati e formati Wave](https://msdn2.microsoft.com/library/ms867195.aspx) nel sito Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="1368b-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="1368b-124">**\_framerate video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="1368b-125">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-125">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-126">Frequenza dei fotogrammi del file video, in frame al secondo x 1.000.</span><span class="sxs-lookup"><span data-stu-id="1368b-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="1368b-127">Una frequenza di fotogrammi di 29,97, ad esempio, viene rappresentata come 29970.</span><span class="sxs-lookup"><span data-stu-id="1368b-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="1368b-128">**\_genere video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="1368b-129">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1368b-130">Genere di questo file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-130">The genre of this video file.</span></span> <span data-ttu-id="1368b-131">Non sono presenti definizioni di genere standard.</span><span class="sxs-lookup"><span data-stu-id="1368b-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="1368b-132">**\_ \_ \_ distanza fotogramma chiave video WPD \_**</span><span class="sxs-lookup"><span data-stu-id="1368b-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="1368b-133">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-133">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-134">Intervallo tra fotogrammi chiave, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="1368b-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="1368b-135">**\_ \_ impostazione qualità video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="1368b-136">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-136">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-137">Impostazione qualità per il file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-137">The quality setting for the video file.</span></span> <span data-ttu-id="1368b-138">Si tratta di un dipendente dal codec.</span><span class="sxs-lookup"><span data-stu-id="1368b-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="1368b-139">**WPD \_ video \_ - \_ numero di canale RECORDEDTV \_**</span><span class="sxs-lookup"><span data-stu-id="1368b-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="1368b-140">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-140">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-141">Il numero del canale televisivo dal quale è stato registrato il video.</span><span class="sxs-lookup"><span data-stu-id="1368b-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="1368b-142">**\_Descrizione del programma WPD video \_ RECORDEDTV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1368b-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="1368b-143">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1368b-144">Una descrizione del programma TV registrato.</span><span class="sxs-lookup"><span data-stu-id="1368b-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="1368b-145">**\_ \_ ripetizione RECORDEDTV video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="1368b-146">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="1368b-147">Valore booleano che specifica se il programma televisivo è stato visualizzato ripetutamente.</span><span class="sxs-lookup"><span data-stu-id="1368b-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="1368b-148">**\_nome della \_ \_ stazione RECORDEDTV del video \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="1368b-149">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="1368b-150">Stazione televisiva dalla quale è stato registrato il video.</span><span class="sxs-lookup"><span data-stu-id="1368b-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="1368b-151">**\_tipo di \_ analisi \_ video WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="1368b-152">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="1368b-152">**VT\_UI4**</span></span>    | <span data-ttu-id="1368b-153">Enumeratore [**WPD \_ video \_ Scan \_ types**](wpd-video-scan-types.md) che specifica l'interlacciamento del file video.</span><span class="sxs-lookup"><span data-stu-id="1368b-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="1368b-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1368b-154">Requirements</span></span>



| <span data-ttu-id="1368b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="1368b-155">Requirement</span></span> | <span data-ttu-id="1368b-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1368b-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1368b-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1368b-157">Header</span></span><br/> | <dl> <span data-ttu-id="1368b-158"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1368b-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1368b-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1368b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1368b-160">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="1368b-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




