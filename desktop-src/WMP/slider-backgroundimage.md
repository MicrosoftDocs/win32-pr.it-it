---
title: SLIDER. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Media Player Windows SLIDER. backgroundImage
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325123"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="c7132-104">SLIDER. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="c7132-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="c7132-105">L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c7132-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="c7132-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c7132-106">Possible Values</span></span>

<span data-ttu-id="c7132-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="c7132-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7132-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7132-108">Remarks</span></span>

<span data-ttu-id="c7132-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c7132-109">This attribute is optional.</span></span> <span data-ttu-id="c7132-110">Quando si usano immagini per costruire un dispositivo di scorrimento, il valore **BackgroundImage** viene usato per l'immagine del dispositivo di scorrimento principale.</span><span class="sxs-lookup"><span data-stu-id="c7132-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="c7132-111">**ThumbImage** rappresenta il dispositivo di scorrimento effettivo e può essere spostato usando il mouse.</span><span class="sxs-lookup"><span data-stu-id="c7132-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="c7132-112">Sul dispositivo di scorrimento **thumbImage** è presente una riga invisibile in cui l'immagine di sfondo viene visualizzata su un lato della riga e l'immagine in primo piano viene visualizzata sull'altro lato.</span><span class="sxs-lookup"><span data-stu-id="c7132-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="c7132-113">Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="c7132-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="c7132-114">Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.</span><span class="sxs-lookup"><span data-stu-id="c7132-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="c7132-115">Se l'attributo **affiancato** è impostato su true e l'immagine di sfondo è minore del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente a seconda dell'attributo **Direction** .</span><span class="sxs-lookup"><span data-stu-id="c7132-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="c7132-116">Se l'attributo **borderSize** è impostato su un valore maggiore di zero, il numero specificato sarà il numero di pixel a partire da sinistra e a destra o superiore e inferiore dell'immagine (anche in questo caso, a seconda dell'attributo **Direction** ) che verrà riservato ai bordi del controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c7132-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="c7132-117">In questo caso, solo la parte centrale dell'immagine viene usata per affiancare il resto del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7132-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="c7132-118">I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="c7132-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7132-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7132-119">Requirements</span></span>



| <span data-ttu-id="c7132-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7132-120">Requirement</span></span> | <span data-ttu-id="c7132-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c7132-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c7132-122">Versione</span><span class="sxs-lookup"><span data-stu-id="c7132-122">Version</span></span><br/> | <span data-ttu-id="c7132-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c7132-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7132-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7132-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7132-125">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="c7132-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c7132-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="c7132-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="c7132-127">**SLIDER. Slide**</span><span class="sxs-lookup"><span data-stu-id="c7132-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="c7132-128">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="c7132-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





