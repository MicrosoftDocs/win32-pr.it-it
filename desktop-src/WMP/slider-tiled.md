---
title: SLIDER. affiancato
description: L'attributo affiancato specifica o recupera un valore che indica se l'immagine del dispositivo di scorrimento verrà affiancata.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Media Player Windows SLIDER. tiled
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328198"
---
# <a name="slidertiled"></a><span data-ttu-id="d3edd-104">SLIDER. affiancato</span><span class="sxs-lookup"><span data-stu-id="d3edd-104">SLIDER.tiled</span></span>

<span data-ttu-id="d3edd-105">L'attributo **affiancato** specifica o recupera un valore che indica se l'immagine del dispositivo di scorrimento verrà affiancata.</span><span class="sxs-lookup"><span data-stu-id="d3edd-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="d3edd-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d3edd-106">Possible Values</span></span>

<span data-ttu-id="d3edd-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d3edd-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d3edd-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d3edd-108">Value</span></span> | <span data-ttu-id="d3edd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3edd-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3edd-110">true</span><span class="sxs-lookup"><span data-stu-id="d3edd-110">true</span></span>  | <span data-ttu-id="d3edd-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3edd-111">Default.</span></span> <span data-ttu-id="d3edd-112">La bitmap dell'immagine verrà ripetuta fino a riempire l'intera area del controllo.</span><span class="sxs-lookup"><span data-stu-id="d3edd-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="d3edd-113">false</span><span class="sxs-lookup"><span data-stu-id="d3edd-113">false</span></span> | <span data-ttu-id="d3edd-114">L'immagine non verrà affiancata.</span><span class="sxs-lookup"><span data-stu-id="d3edd-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="d3edd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3edd-115">Remarks</span></span>

<span data-ttu-id="d3edd-116">Questo attributo si applica solo se si usano immagini di primo piano e di sfondo per definire un controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d3edd-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="d3edd-117">Se le immagini sono più piccole dell'area definita del dispositivo di scorrimento e l'attributo **affiancato** è impostato su true, le immagini verranno ripetute fino a riempire l'intera lunghezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="d3edd-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="d3edd-118">È possibile utilizzare questo attributo in combinazione con l'attributo **borderSize** .</span><span class="sxs-lookup"><span data-stu-id="d3edd-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="d3edd-119">L'attributo **borderSize** consente di definire un bordo che non viene ripetuto durante l'affiancamento.</span><span class="sxs-lookup"><span data-stu-id="d3edd-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3edd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3edd-120">Requirements</span></span>



| <span data-ttu-id="d3edd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3edd-121">Requirement</span></span> | <span data-ttu-id="d3edd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d3edd-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d3edd-123">Versione</span><span class="sxs-lookup"><span data-stu-id="d3edd-123">Version</span></span><br/> | <span data-ttu-id="d3edd-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d3edd-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3edd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3edd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3edd-126">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="d3edd-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="d3edd-127">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="d3edd-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="d3edd-128">**SLIDER. borderSize**</span><span class="sxs-lookup"><span data-stu-id="d3edd-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="d3edd-129">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="d3edd-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





