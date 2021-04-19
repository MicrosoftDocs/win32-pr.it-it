---
title: BUTTONGROUP. hoverImage
description: L'attributo hoverImage specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in BUTTONGROUP. Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- Media Player Windows BUTTONGROUP. hoverImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324103"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="4bea5-105">BUTTONGROUP. hoverImage</span><span class="sxs-lookup"><span data-stu-id="4bea5-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="4bea5-106">L'attributo **hoverImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="4bea5-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="4bea5-107">Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.</span><span class="sxs-lookup"><span data-stu-id="4bea5-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="4bea5-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="4bea5-108">Possible Values</span></span>

<span data-ttu-id="4bea5-109">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4bea5-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bea5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bea5-110">Remarks</span></span>

<span data-ttu-id="4bea5-111">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="4bea5-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="4bea5-112">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .</span><span class="sxs-lookup"><span data-stu-id="4bea5-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="4bea5-113">L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4bea5-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="4bea5-114">Se l'immagine del passaggio del mouse è maggiore della regione specificata, l'immagine del passaggio del mouse verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="4bea5-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="4bea5-115">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="4bea5-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="4bea5-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4bea5-116">Examples</span></span>

<span data-ttu-id="4bea5-117">Vedere *ButtonElement*. attributo [mappingColor](buttonelement-mappingcolor.md) per un esempio che illustra l'uso di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="4bea5-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bea5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bea5-118">Requirements</span></span>



| <span data-ttu-id="4bea5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bea5-119">Requirement</span></span> | <span data-ttu-id="4bea5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4bea5-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4bea5-121">Versione</span><span class="sxs-lookup"><span data-stu-id="4bea5-121">Version</span></span><br/> | <span data-ttu-id="4bea5-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="4bea5-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bea5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bea5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bea5-124">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="4bea5-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="4bea5-125">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="4bea5-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="4bea5-126">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="4bea5-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="4bea5-127">**BUTTONGROUP. saturazione**</span><span class="sxs-lookup"><span data-stu-id="4bea5-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





