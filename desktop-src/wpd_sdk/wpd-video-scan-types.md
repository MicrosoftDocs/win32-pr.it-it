---
description: Il \_ \_ \_ tipo di enumerazione WPD video Scan types descrive il modo in cui vengono codificati i campi di un file video.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumerazione WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324865"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="8fade-103">\_Enumerazione dei \_ tipi di analisi video WPD \_</span><span class="sxs-lookup"><span data-stu-id="8fade-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="8fade-104">Il tipo di enumerazione **WPD \_ video \_ Scan \_ types** descrive il modo in cui vengono codificati i campi di un file video.</span><span class="sxs-lookup"><span data-stu-id="8fade-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fade-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fade-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="8fade-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8fade-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8fade-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_tipo di analisi video WPD non \_ \_ \_ usato**</span><span class="sxs-lookup"><span data-stu-id="8fade-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-108">Il tipo di analisi non è stato definito per questo file video o non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="8fade-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_tipo di \_ analisi video WPD \_ \_ progressivo**</span><span class="sxs-lookup"><span data-stu-id="8fade-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-110">Un file video di analisi progressiva.</span><span class="sxs-lookup"><span data-stu-id="8fade-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD \_ il \_ campo tipo di analisi video \_ \_ \_ Interleaved \_ superiore \_**</span><span class="sxs-lookup"><span data-stu-id="8fade-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-112">Un file video con interfoliazione in cui i campi alternativi e il campo superiore (con riga 1) vengono disegnati per primi.</span><span class="sxs-lookup"><span data-stu-id="8fade-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="8fade-113">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8fade-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD \_ il \_ campo tipo di analisi video con \_ \_ \_ interfoliazione \_ più basso \_ prima**</span><span class="sxs-lookup"><span data-stu-id="8fade-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-115">Un file video con interfoliazione in cui i campi alternativi e il campo inferiore (con riga 2) vengono disegnati per primi.</span><span class="sxs-lookup"><span data-stu-id="8fade-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="8fade-116">Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.</span><span class="sxs-lookup"><span data-stu-id="8fade-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD \_ il \_ campo tipo di analisi video \_ \_ singolo in \_ \_ \_ primo piano**</span><span class="sxs-lookup"><span data-stu-id="8fade-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-118">Un file video con interfoliazione in cui i campi vengono inviati come campioni contigui e viene disegnato per primo il campo superiore (con riga 1).</span><span class="sxs-lookup"><span data-stu-id="8fade-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="8fade-119">Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.</span><span class="sxs-lookup"><span data-stu-id="8fade-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD \_ \_ campo tipo di analisi video \_ singolo in \_ basso per \_ \_ \_ primo**</span><span class="sxs-lookup"><span data-stu-id="8fade-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-121">Un file video con interfoliazione in cui i campi vengono inviati come campioni contigui e viene inviato per primo il campo inferiore (con riga 2).</span><span class="sxs-lookup"><span data-stu-id="8fade-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_tipo di \_ analisi video WPD \_ \_ mixed \_ Interlace**</span><span class="sxs-lookup"><span data-stu-id="8fade-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-123">Un file video con una combinazione di modalità di interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="8fade-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="8fade-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ tipo di analisi video WPD \_ \_ misto \_ interlacciato \_ e \_ progressivo**</span><span class="sxs-lookup"><span data-stu-id="8fade-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="8fade-125">Un file video con una combinazione di modalità interlacciata e progressiva.</span><span class="sxs-lookup"><span data-stu-id="8fade-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fade-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fade-126">Remarks</span></span>

<span data-ttu-id="8fade-127">Questa enumerazione viene utilizzata dalla proprietà [del \_ \_ \_ tipo di analisi video WPD](properties-and-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="8fade-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="8fade-128">Esistono due tipi di formati di file con interfoliazione specificati da questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="8fade-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="8fade-129">**WPD \_ Il \_ campo tipo di analisi video con \_ \_ \_ interfoliazione** si riferisce a un formato di file in cui i frame vengono recapitati in base ai campi analizzati alternativi e i dati passano riga per riga, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8fade-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="8fade-130">**Fotogramma 1**</span><span class="sxs-lookup"><span data-stu-id="8fade-130">**Frame 1**</span></span>

<span data-ttu-id="8fade-131">Campo 1: riga 1</span><span class="sxs-lookup"><span data-stu-id="8fade-131">Field 1: Line 1</span></span>

<span data-ttu-id="8fade-132">Campo 2: riga 1</span><span class="sxs-lookup"><span data-stu-id="8fade-132">Field 2: Line 1</span></span>

<span data-ttu-id="8fade-133">Campo 1: riga 2</span><span class="sxs-lookup"><span data-stu-id="8fade-133">Field 1: Line 2</span></span>

<span data-ttu-id="8fade-134">Campo 2: riga 2</span><span class="sxs-lookup"><span data-stu-id="8fade-134">Field 2: Line 2</span></span>

<span data-ttu-id="8fade-135">Campo 1: riga 3</span><span class="sxs-lookup"><span data-stu-id="8fade-135">Field 1: Line 3</span></span>

<span data-ttu-id="8fade-136">Campo 2: riga 3</span><span class="sxs-lookup"><span data-stu-id="8fade-136">Field 2: Line 3</span></span>

<span data-ttu-id="8fade-137">...</span><span class="sxs-lookup"><span data-stu-id="8fade-137">...</span></span>

<span data-ttu-id="8fade-138">**WPD \_ Il \_ campo tipo di analisi video \_ \_ \_ singolo** fa riferimento a un formato di file in cui ogni campo viene archiviato in un singolo blocco di righe di analisi e i campi vengono archiviati in sequenza, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8fade-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="8fade-139">**Fotogramma 1**</span><span class="sxs-lookup"><span data-stu-id="8fade-139">**Frame 1**</span></span>

<span data-ttu-id="8fade-140">Campo 1: riga 1</span><span class="sxs-lookup"><span data-stu-id="8fade-140">Field 1: Line 1</span></span>

<span data-ttu-id="8fade-141">Campo 1: riga 2</span><span class="sxs-lookup"><span data-stu-id="8fade-141">Field 1: Line 2</span></span>

<span data-ttu-id="8fade-142">Campo 1: riga 3</span><span class="sxs-lookup"><span data-stu-id="8fade-142">Field 1: Line 3</span></span>

<span data-ttu-id="8fade-143">...</span><span class="sxs-lookup"><span data-stu-id="8fade-143">...</span></span>

<span data-ttu-id="8fade-144">Seguito da</span><span class="sxs-lookup"><span data-stu-id="8fade-144">Followed by</span></span>

<span data-ttu-id="8fade-145">Campo 2: riga 1</span><span class="sxs-lookup"><span data-stu-id="8fade-145">Field 2: Line 1</span></span>

<span data-ttu-id="8fade-146">Campo 2: riga 2</span><span class="sxs-lookup"><span data-stu-id="8fade-146">Field 2: Line 2</span></span>

<span data-ttu-id="8fade-147">Campo 2: riga 3</span><span class="sxs-lookup"><span data-stu-id="8fade-147">Field 2: Line 3</span></span>

<span data-ttu-id="8fade-148">...</span><span class="sxs-lookup"><span data-stu-id="8fade-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="8fade-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fade-149">Requirements</span></span>



| <span data-ttu-id="8fade-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fade-150">Requirement</span></span> | <span data-ttu-id="8fade-151">Valore</span><span class="sxs-lookup"><span data-stu-id="8fade-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fade-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fade-152">Header</span></span><br/> | <dl> <span data-ttu-id="8fade-153"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fade-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fade-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fade-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fade-155">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="8fade-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




