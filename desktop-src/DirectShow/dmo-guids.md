---
description: Nella tabella seguente sono elencati gli identificatori univoci globali (GUID) definiti per le categorie Microsoft DirectX Media Object (DMO). Questi GUID vengono definiti nel file di intestazione Dmoreg. h ed esportati dalla libreria Dmoguids. lib.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: GUID DMO (Dmoreg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327669"
---
# <a name="dmo-guids"></a><span data-ttu-id="fb81f-104">GUID DMO</span><span class="sxs-lookup"><span data-stu-id="fb81f-104">DMO GUIDs</span></span>

<span data-ttu-id="fb81f-105">Nella tabella seguente sono elencati gli identificatori univoci globali (GUID) definiti per le categorie Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="fb81f-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="fb81f-106">Questi GUID vengono definiti nel file di intestazione Dmoreg. h ed esportati dalla libreria Dmoguids. lib.</span><span class="sxs-lookup"><span data-stu-id="fb81f-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="fb81f-107">Per enumerare il DMOs registrato in una categoria, passare il GUID corrispondente alla funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="fb81f-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="fb81f-108">GUID</span><span class="sxs-lookup"><span data-stu-id="fb81f-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="fb81f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb81f-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="fb81f-110"><dt>**\_decodificatore audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="fb81f-111">Decoder audio</span><span class="sxs-lookup"><span data-stu-id="fb81f-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="fb81f-112"><dt>**\_effetto audio \_ DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="fb81f-113">Effetto audio</span><span class="sxs-lookup"><span data-stu-id="fb81f-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="fb81f-114"><dt>**\_ \_ codificatore audio DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="fb81f-115">Codificatore audio</span><span class="sxs-lookup"><span data-stu-id="fb81f-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="fb81f-116"><dt>**\_decodificatore video DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="fb81f-117">Decodificatore video</span><span class="sxs-lookup"><span data-stu-id="fb81f-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="fb81f-118"><dt>**\_effetto video \_ DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="fb81f-119">Effetto video</span><span class="sxs-lookup"><span data-stu-id="fb81f-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="fb81f-120"><dt>**\_ \_ codificatore video DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="fb81f-121">Codificatore video</span><span class="sxs-lookup"><span data-stu-id="fb81f-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="fb81f-122"><dt>**\_ \_ effetto acquisizione audio \_ DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="fb81f-123">Effetto acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="fb81f-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fb81f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb81f-124">Requirements</span></span>



| <span data-ttu-id="fb81f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb81f-125">Requirement</span></span> | <span data-ttu-id="fb81f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fb81f-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb81f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb81f-127">Header</span></span><br/> | <dl> <span data-ttu-id="fb81f-128"><dt>Dmoreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb81f-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb81f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb81f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb81f-130">Costanti DMO</span><span class="sxs-lookup"><span data-stu-id="fb81f-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




