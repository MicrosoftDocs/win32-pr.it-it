---
description: Questi flag specificano come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Flag di ridimensionamento (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330781"
---
# <a name="resize-flags"></a><span data-ttu-id="405ee-103">Ridimensiona flag</span><span class="sxs-lookup"><span data-stu-id="405ee-103">Resize Flags</span></span>

<span data-ttu-id="405ee-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="405ee-104">\[Deprecated.</span></span> <span data-ttu-id="405ee-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="405ee-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="405ee-106">Questi flag specificano come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="405ee-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="405ee-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="405ee-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="405ee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="405ee-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="405ee-109"><dt>**REsizef \_ ESTENSIONE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="405ee-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="405ee-110">L'immagine viene adattata in base alle dimensioni del frame di destinazione in entrambe le dimensioni, senza mantenere le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="405ee-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="405ee-111"><dt>**REsizef \_ Ritaglio**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="405ee-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="405ee-112">L'immagine non viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="405ee-112">The image is not resized.</span></span> <span data-ttu-id="405ee-113">Se l'immagine è più piccola del frame di destinazione, l'area circostante è nera.</span><span class="sxs-lookup"><span data-stu-id="405ee-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="405ee-114">Se l'immagine è più grande del frame di destinazione, l'immagine viene ritagliata.</span><span class="sxs-lookup"><span data-stu-id="405ee-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="405ee-115"><dt>**REsizef \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="405ee-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="405ee-116">L'immagine viene ridimensionata per adattarsi al frame di destinazione lungo una dimensione, mantenendo le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="405ee-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="405ee-117">Se il rapporto tra larghezza e altezza nell'immagine non corrisponde al rapporto nel frame di destinazione, viene creata una letterbox.</span><span class="sxs-lookup"><span data-stu-id="405ee-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="405ee-118"><dt>**REsizef \_ PRESERVEASPECTRATIO \_ noletterbox**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="405ee-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="405ee-119">L'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni.</span><span class="sxs-lookup"><span data-stu-id="405ee-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="405ee-120">Anziché creare una letterbox, questa modalità Ritaglia l'immagine, lungo i lati o nella parte superiore e inferiore.</span><span class="sxs-lookup"><span data-stu-id="405ee-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="405ee-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="405ee-121">Remarks</span></span>

<span data-ttu-id="405ee-122">Le immagini seguenti mostrano gli effetti di questi flag.</span><span class="sxs-lookup"><span data-stu-id="405ee-122">The following images show the effects of these flags.</span></span>

![Ridimensiona flag](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="405ee-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="405ee-124">Requirements</span></span>



| <span data-ttu-id="405ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="405ee-125">Requirement</span></span> | <span data-ttu-id="405ee-126">Valore</span><span class="sxs-lookup"><span data-stu-id="405ee-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="405ee-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="405ee-127">Header</span></span><br/> | <dl> <span data-ttu-id="405ee-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="405ee-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="405ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="405ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405ee-130">**IAMTimelineSrc::GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="405ee-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="405ee-131">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="405ee-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




