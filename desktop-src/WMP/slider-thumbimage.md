---
title: SLIDER. thumbImage
description: L'attributo thumbImage specifica o recupera l'immagine che verrà usata per rappresentare la posizione corrente del dispositivo di scorrimento.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Media Player Windows SLIDER. thumbImage
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331578"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="fda0f-104">SLIDER. thumbImage</span><span class="sxs-lookup"><span data-stu-id="fda0f-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="fda0f-105">L'attributo **thumbImage** specifica o recupera l'immagine che verrà usata per rappresentare la posizione corrente del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="fda0f-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="fda0f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fda0f-106">Possible Values</span></span>

<span data-ttu-id="fda0f-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="fda0f-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda0f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fda0f-108">Remarks</span></span>

<span data-ttu-id="fda0f-109">**ThumbImage** specifica l'immagine che verrà usata per rappresentare la posizione corrente, oltre a indicare che l'utente può eseguire un'azione con il controllo.</span><span class="sxs-lookup"><span data-stu-id="fda0f-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="fda0f-110">Se non viene specificata alcuna immagine Thumb, il dispositivo di scorrimento non è interattivo.</span><span class="sxs-lookup"><span data-stu-id="fda0f-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="fda0f-111">L'immagine Thumb è centrata nella dimensione stretta del controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="fda0f-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="fda0f-112">Se l'immagine Thumb è più stretta del controllo, l'immagine viene visualizzata al centro dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="fda0f-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="fda0f-113">Se l'immagine Thumb è più grande del controllo, le estremità dell'immagine vengono tagliate.</span><span class="sxs-lookup"><span data-stu-id="fda0f-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="fda0f-114">La posizione del dispositivo di scorrimento è specificata dal centro dell'immagine Thumb.</span><span class="sxs-lookup"><span data-stu-id="fda0f-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="fda0f-115">Se **borderSize** è zero, solo metà dell'immagine Thumb sarà visibile nelle posizioni iniziale e finale del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="fda0f-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="fda0f-116">Per evitare questo problema, impostare **borderSize** su un valore maggiore o uguale a metà della larghezza dell'immagine del cursore (o metà dell'altezza se **Direction** è impostato su "Vertical").</span><span class="sxs-lookup"><span data-stu-id="fda0f-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="fda0f-117">I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="fda0f-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="fda0f-118">Vedere **CUSTOMSLIDER**. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="fda0f-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda0f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fda0f-119">Requirements</span></span>



| <span data-ttu-id="fda0f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fda0f-120">Requirement</span></span> | <span data-ttu-id="fda0f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fda0f-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fda0f-122">Versione</span><span class="sxs-lookup"><span data-stu-id="fda0f-122">Version</span></span><br/> | <span data-ttu-id="fda0f-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="fda0f-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fda0f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fda0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda0f-125">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="fda0f-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="fda0f-126">**SLIDER. borderSize**</span><span class="sxs-lookup"><span data-stu-id="fda0f-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="fda0f-127">**SLIDER. Direction**</span><span class="sxs-lookup"><span data-stu-id="fda0f-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





