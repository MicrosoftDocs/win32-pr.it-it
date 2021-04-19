---
title: BUTTONGROUP. transparencyColor
description: L'attributo transparencyColor specifica o Recupera il colore trasparente delle immagini BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- Media Player Windows BUTTONGROUP. transparencyColor
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326479"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="5f1e5-104">BUTTONGROUP. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="5f1e5-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="5f1e5-105">L'attributo **transparencyColor** specifica o Recupera il colore trasparente delle immagini **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="5f1e5-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="5f1e5-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5f1e5-106">Possible Values</span></span>

<span data-ttu-id="5f1e5-107">Questo attributo è una **stringa** di lettura/scrittura e non prevede alcun valore predefinito, contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="5f1e5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5f1e5-108">Value</span></span>                                       | <span data-ttu-id="5f1e5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f1e5-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1e5-110">Auto</span><span class="sxs-lookup"><span data-stu-id="5f1e5-110">Auto</span></span>                                        | <span data-ttu-id="5f1e5-111">Il pixel nella posizione 0, 0 nell'immagine diventa il colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="5f1e5-112">qualsiasi valore di colore di Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="5f1e5-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="5f1e5-113">Un valore di colore di Internet Explorer diventa il colore trasparente (ad esempio, "Red" o " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="5f1e5-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="5f1e5-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="5f1e5-114">None</span></span>                                        | <span data-ttu-id="5f1e5-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-115">Default.</span></span> <span data-ttu-id="5f1e5-116">Nessuna trasparenza.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5f1e5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f1e5-117">Remarks</span></span>

<span data-ttu-id="5f1e5-118">Un colore trasparente in un'immagine consentirà tutto ciò che si trova dietro l'immagine per visualizzare le aree di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="5f1e5-119">L'area trasparente è selezionabile a meno che non venga troncata dal tag **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="5f1e5-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="5f1e5-120">Il colore può essere qualsiasi valore di colore di Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="5f1e5-121">Se il valore è auto, viene usato il colore del pixel nella posizione 0, 0 nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="5f1e5-122">Se il colore specificato non è uno dei colori di Internet Explorer validi, viene restituito un avviso e viene mantenuto il valore precedente.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="5f1e5-123">Poiché i jpg sono con perdita di tempo e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate quando si usa **transparencyColor** .</span><span class="sxs-lookup"><span data-stu-id="5f1e5-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1e5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f1e5-124">Requirements</span></span>



| <span data-ttu-id="5f1e5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1e5-125">Requirement</span></span> | <span data-ttu-id="5f1e5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5f1e5-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5f1e5-127">Versione</span><span class="sxs-lookup"><span data-stu-id="5f1e5-127">Version</span></span><br/> | <span data-ttu-id="5f1e5-128">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5f1e5-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f1e5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f1e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1e5-130">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="5f1e5-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="5f1e5-131">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="5f1e5-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





