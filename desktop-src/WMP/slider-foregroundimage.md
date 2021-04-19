---
title: SLIDER. foregroundImage
description: L'attributo foregroundImage specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Media Player Windows SLIDER. foregroundImage
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332243"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="612da-104">SLIDER. foregroundImage</span><span class="sxs-lookup"><span data-stu-id="612da-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="612da-105">L'attributo **foregroundImage** specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="612da-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="612da-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="612da-106">Possible Values</span></span>

<span data-ttu-id="612da-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="612da-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="612da-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="612da-108">Remarks</span></span>

<span data-ttu-id="612da-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="612da-109">This attribute is optional.</span></span> <span data-ttu-id="612da-110">Quando si utilizzano immagini per costruire un controllo dispositivo di scorrimento, la **BackgroundImage** viene utilizzata per l'immagine del dispositivo di scorrimento principale.</span><span class="sxs-lookup"><span data-stu-id="612da-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="612da-111">**ThumbImage** rappresenta il dispositivo di scorrimento effettivo e può essere spostato usando il mouse.</span><span class="sxs-lookup"><span data-stu-id="612da-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="612da-112">Sul dispositivo di scorrimento **thumbImage** è presente una riga invisibile in cui l'immagine di sfondo viene visualizzata su un lato della riga e l'immagine in primo piano viene visualizzata sull'altro lato.</span><span class="sxs-lookup"><span data-stu-id="612da-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="612da-113">Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="612da-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="612da-114">Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.</span><span class="sxs-lookup"><span data-stu-id="612da-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="612da-115">Se l'attributo **affiancato** è impostato su true e l'immagine in primo piano è inferiore all'area di primo piano del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente, a seconda dell'attributo **Direction** , per riempire lo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="612da-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="612da-116">I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="612da-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="612da-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="612da-117">Requirements</span></span>



| <span data-ttu-id="612da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="612da-118">Requirement</span></span> | <span data-ttu-id="612da-119">Valore</span><span class="sxs-lookup"><span data-stu-id="612da-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="612da-120">Versione</span><span class="sxs-lookup"><span data-stu-id="612da-120">Version</span></span><br/> | <span data-ttu-id="612da-121">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="612da-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="612da-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="612da-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612da-123">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="612da-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="612da-124">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="612da-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="612da-125">**SLIDER. Slide**</span><span class="sxs-lookup"><span data-stu-id="612da-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="612da-126">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="612da-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="612da-127">**SLIDER. Value**</span><span class="sxs-lookup"><span data-stu-id="612da-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





