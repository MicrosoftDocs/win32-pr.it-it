---
description: Il filtro del codificatore Microsoft AC-3 codifica l'audio PCM stereo in un bitstream Digital bitstream.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 encoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124518"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="40bf8-103">Codificatore Microsoft AC-3</span><span class="sxs-lookup"><span data-stu-id="40bf8-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="40bf8-104">Il filtro del codificatore Microsoft AC-3 codifica l'audio PCM stereo in un bitstream Digital bitstream.</span><span class="sxs-lookup"><span data-stu-id="40bf8-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="40bf8-105">L'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40bf8-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="40bf8-106">Questo filtro non è supportato nelle piattaforme basate su IA-64.</span><span class="sxs-lookup"><span data-stu-id="40bf8-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="40bf8-107">Informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="40bf8-107">Filter Information</span></span>

<span data-ttu-id="40bf8-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="40bf8-108">Filter Interfaces</span></span>

[<span data-ttu-id="40bf8-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="40bf8-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="40bf8-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="40bf8-110">Input Pin Media Types</span></span>

<span data-ttu-id="40bf8-111">**MEDIATYPE \_ Audio**, **\_ PCM MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="40bf8-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="40bf8-112">Il tipo di input deve essere stereo a 48 kHz, a 16 bit per campione.</span><span class="sxs-lookup"><span data-stu-id="40bf8-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="40bf8-113">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="40bf8-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="40bf8-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="40bf8-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="40bf8-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="40bf8-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="40bf8-116">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="40bf8-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="40bf8-117">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="40bf8-117">Output Pin Media Types</span></span>

<span data-ttu-id="40bf8-118">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="40bf8-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="40bf8-119">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="40bf8-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="40bf8-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="40bf8-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="40bf8-121">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="40bf8-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="40bf8-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="40bf8-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="40bf8-123">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="40bf8-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="40bf8-124">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="40bf8-124">Filter CLSID</span></span>

<span data-ttu-id="40bf8-125">**CLSID \_ CMSAC3Enc** (dichiarata in wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="40bf8-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="40bf8-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="40bf8-126">Executable</span></span>

<span data-ttu-id="40bf8-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="40bf8-127">msac3enc.dll</span></span>

[<span data-ttu-id="40bf8-128">Merito</span><span class="sxs-lookup"><span data-stu-id="40bf8-128">Merit</span></span>](merit.md)

<span data-ttu-id="40bf8-129">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="40bf8-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="40bf8-130">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="40bf8-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="40bf8-131">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="40bf8-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="40bf8-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="40bf8-132">Remarks</span></span>

<span data-ttu-id="40bf8-133">Questo filtro non è disponibile per l'uso da parte di applicazioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="40bf8-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="40bf8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40bf8-134">Requirements</span></span>



| <span data-ttu-id="40bf8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="40bf8-135">Requirement</span></span> | <span data-ttu-id="40bf8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="40bf8-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40bf8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40bf8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="40bf8-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="40bf8-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="40bf8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40bf8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="40bf8-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40bf8-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="40bf8-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40bf8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="40bf8-142"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40bf8-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="40bf8-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40bf8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40bf8-144">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="40bf8-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




