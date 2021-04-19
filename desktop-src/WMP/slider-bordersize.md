---
title: SLIDER. borderSize
description: L'attributo borderSize specifica o recupera lo spessore del bordo in pixel.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Media Player Windows SLIDER. borderSize
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329991"
---
# <a name="sliderbordersize"></a><span data-ttu-id="9e9ff-104">SLIDER. borderSize</span><span class="sxs-lookup"><span data-stu-id="9e9ff-104">SLIDER.borderSize</span></span>

<span data-ttu-id="9e9ff-105">L'attributo **borderSize** specifica o recupera lo spessore del bordo in pixel.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="9e9ff-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9e9ff-106">Possible Values</span></span>

<span data-ttu-id="9e9ff-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) che rappresenta lo spessore del bordo in pixel.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="9e9ff-108">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9ff-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e9ff-109">Remarks</span></span>

<span data-ttu-id="9e9ff-110">Questo attributo definisce un offset dall'inizio e dalla fine del controllo dispositivo di scorrimento, che è da sinistra a destra se l'attributo **Direction** è impostato su "Horizontal" e dall'alto verso il basso se è impostato su "Vertical".</span><span class="sxs-lookup"><span data-stu-id="9e9ff-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="9e9ff-111">Queste posizioni di offset definiscono le posizioni minime e massime del cursore del dispositivo di scorrimento, oltre le quali non verrà applicato il colore di primo piano o l'immagine.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="9e9ff-112">Se un'immagine di sfondo viene utilizzata con l'attributo **affiancato** impostato su true, l'offset viene applicato all'immagine, determinando la quantità dell'immagine, da sinistra a destra o dalla parte superiore e inferiore, da utilizzare per i bordi iniziale e finale del controllo dispositivo di scorrimento, con la parte centrale dell'immagine che viene affiancata nel resto.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="9e9ff-113">In questo modo, è possibile usare una piccola immagine di sfondo per coprire la lunghezza totale di un controllo dispositivo di scorrimento più grande.</span><span class="sxs-lookup"><span data-stu-id="9e9ff-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9ff-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e9ff-114">Requirements</span></span>



| <span data-ttu-id="9e9ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9ff-115">Requirement</span></span> | <span data-ttu-id="9e9ff-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9e9ff-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9e9ff-117">Versione</span><span class="sxs-lookup"><span data-stu-id="9e9ff-117">Version</span></span><br/> | <span data-ttu-id="9e9ff-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="9e9ff-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e9ff-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e9ff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9ff-120">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="9e9ff-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="9e9ff-121">**SLIDER. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="9e9ff-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="9e9ff-122">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="9e9ff-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="9e9ff-123">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="9e9ff-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="9e9ff-124">**SLIDER. affiancato**</span><span class="sxs-lookup"><span data-stu-id="9e9ff-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





