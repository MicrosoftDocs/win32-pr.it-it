---
description: Per diversi GUID di tipo di supporto MPEG-2, Windows DDK definisce nomi diversi dai nomi usati in DirectShow. La tabella seguente illustra i nomi DirectShow (definiti in Ksuuids. h) e i nomi in modalità kernel corrispondenti (definiti in Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipi di supporti MPEG-2 kernel (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330502"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="ab73b-104">Tipi di supporti MPEG-2 kernel</span><span class="sxs-lookup"><span data-stu-id="ab73b-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="ab73b-105">Per diversi GUID di tipo di supporto MPEG-2, Windows DDK definisce nomi diversi dai nomi usati in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ab73b-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="ab73b-106">La tabella seguente illustra i nomi DirectShow (definiti in Ksuuids. h) e i nomi in modalità kernel corrispondenti (definiti in Ksmedia. h).</span><span class="sxs-lookup"><span data-stu-id="ab73b-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="ab73b-107">Nome in Ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="ab73b-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="ab73b-108">Nome in Ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="ab73b-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="ab73b-109">FORMATO \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="ab73b-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="ab73b-110">\_identificatore KSDATAFORMAT \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="ab73b-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="ab73b-111">FORMATO \_ mpeg2video</span><span class="sxs-lookup"><span data-stu-id="ab73b-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="ab73b-112">VIDEO di KSDATAFORMAT \_ specifier \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="ab73b-113">MEDIASUBTYPE \_ ATSC \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="ab73b-114">KSDATAFORMAT \_ sottotipo \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="ab73b-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="ab73b-115">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="ab73b-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="ab73b-116">\_Audio AC3 del sottotipo KSDATAFORMAT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="ab73b-117">MEDIASUBTYPE \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="ab73b-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="ab73b-118">KSDATAFORMAT \_ sottotipo \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="ab73b-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="ab73b-119">\_audio MEDIASUBTYPE DVD \_ LPCM \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="ab73b-120">KSDATAFORMAT \_ sottotipo \_ LPCM \_ audio</span><span class="sxs-lookup"><span data-stu-id="ab73b-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="ab73b-121">\_Audio MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ab73b-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="ab73b-122">\_Audio MPEG2 del sottotipo KSDATAFORMAT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="ab73b-123">\_Programma MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="ab73b-124">\_ \_ Programma MPEG2 di tipo KSDATAFORMAT \_ statico \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="ab73b-125">\_Trasporto MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ab73b-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="ab73b-126">KSDATAFORMAT \_ tipo \_ di \_ trasporto MPEG2</span><span class="sxs-lookup"><span data-stu-id="ab73b-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="ab73b-127">VIDEO di MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="ab73b-128">VIDEO di KSDATAFORMAT \_ sottotipo \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="ab73b-129">\_Sezioni MEDIATYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="ab73b-130">Sezioni KSDATAFORMAT di \_ tipo \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="ab73b-131">\_Audio MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="ab73b-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="ab73b-132">\_audio di tipo KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="ab73b-133">\_PES MEDIATYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="ab73b-134">Tipo di KSDATAFORMAT \_ \_ MPEG2 \_ PE</span><span class="sxs-lookup"><span data-stu-id="ab73b-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="ab73b-135">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="ab73b-136">\_video di tipo KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="ab73b-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="ab73b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab73b-137">Requirements</span></span>



| <span data-ttu-id="ab73b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab73b-138">Requirement</span></span> | <span data-ttu-id="ab73b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ab73b-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab73b-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab73b-140">Header</span></span><br/> | <dl> <span data-ttu-id="ab73b-141"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab73b-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab73b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab73b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab73b-143">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ab73b-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




