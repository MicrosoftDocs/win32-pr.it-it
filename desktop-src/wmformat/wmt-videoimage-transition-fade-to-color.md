---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transizione di dissolvenza a colori viene risolta dall'immagine in un frame di colore a tinta unita.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327263"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="e231a-104">\_ \_ dissolvenza WMT VIDEOIMAGE transizione \_ \_ a \_ colore</span><span class="sxs-lookup"><span data-stu-id="e231a-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="e231a-105">La transizione di dissolvenza a colori viene risolta dall'immagine in un frame di colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="e231a-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="e231a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e231a-106">Parameters</span></span>

<span data-ttu-id="e231a-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="e231a-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="e231a-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="e231a-108">Parameter</span></span>         | <span data-ttu-id="e231a-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="e231a-109">Structure member</span></span> | <span data-ttu-id="e231a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e231a-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e231a-111">Red</span><span class="sxs-lookup"><span data-stu-id="e231a-111">Red</span></span>               | <span data-ttu-id="e231a-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="e231a-112">**fEffectPara0**</span></span> | <span data-ttu-id="e231a-113">Valore rosso del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="e231a-113">Red value of the background color.</span></span> <span data-ttu-id="e231a-114">Impostare su un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e231a-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="e231a-115">Green</span><span class="sxs-lookup"><span data-stu-id="e231a-115">Green</span></span>             | <span data-ttu-id="e231a-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="e231a-116">**fEffectPara1**</span></span> | <span data-ttu-id="e231a-117">Valore verde del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="e231a-117">Green value of the background color.</span></span> <span data-ttu-id="e231a-118">Impostare su un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e231a-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e231a-119">Blu</span><span class="sxs-lookup"><span data-stu-id="e231a-119">Blue</span></span>              | <span data-ttu-id="e231a-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="e231a-120">**fEffectPara2**</span></span> | <span data-ttu-id="e231a-121">Valore blu del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="e231a-121">Blue value of the background color.</span></span> <span data-ttu-id="e231a-122">Impostare su un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="e231a-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="e231a-123">Spessore sfondo</span><span class="sxs-lookup"><span data-stu-id="e231a-123">Background weight</span></span> | <span data-ttu-id="e231a-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="e231a-124">**fEffectPara3**</span></span> | <span data-ttu-id="e231a-125">Spessore del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="e231a-125">Weight of the background color.</span></span> <span data-ttu-id="e231a-126">Questo parametro esprime la percentuale del colore di sfondo nella combinazione come decimale.</span><span class="sxs-lookup"><span data-stu-id="e231a-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="e231a-127">Ad esempio, per fondere il colore di sfondo al 30%, impostando su 0,30 l'immagine 70% della combinazione.</span><span class="sxs-lookup"><span data-stu-id="e231a-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e231a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e231a-128">Requirements</span></span>



| <span data-ttu-id="e231a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e231a-129">Requirement</span></span> | <span data-ttu-id="e231a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e231a-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e231a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e231a-131">Header</span></span><br/> | <dl> <span data-ttu-id="e231a-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e231a-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e231a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e231a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e231a-134">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="e231a-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





