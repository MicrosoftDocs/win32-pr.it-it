---
title: BUTTON. transparencyColor
description: L'attributo transparencyColor specifica o Recupera il colore che sarà trasparente nelle immagini dei pulsanti.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332687"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="070ef-104">BUTTON. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="070ef-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="070ef-105">L'attributo **transparencyColor** specifica o Recupera il colore che sarà trasparente nelle immagini dei **pulsanti** .</span><span class="sxs-lookup"><span data-stu-id="070ef-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="070ef-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="070ef-106">Possible Values</span></span>

<span data-ttu-id="070ef-107">Questo attributo è una **stringa** di lettura/scrittura e non prevede alcun valore predefinito contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="070ef-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="070ef-108">Valore</span><span class="sxs-lookup"><span data-stu-id="070ef-108">Value</span></span>                                    | <span data-ttu-id="070ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="070ef-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070ef-110">Auto</span><span class="sxs-lookup"><span data-stu-id="070ef-110">Auto</span></span>                                     | <span data-ttu-id="070ef-111">Il colore del pixel nella posizione 0, 0 nell'immagine diventa il colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="070ef-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="070ef-112">Qualsiasi valore del formato di colore di Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="070ef-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="070ef-113">Un valore in formato colore di Internet Explorer diventa il colore trasparente (ad esempio, "rosso" o " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="070ef-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="070ef-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="070ef-114">None</span></span>                                     | <span data-ttu-id="070ef-115">Nessuna trasparenza.</span><span class="sxs-lookup"><span data-stu-id="070ef-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="070ef-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="070ef-116">Remarks</span></span>

<span data-ttu-id="070ef-117">Un colore trasparente in un'immagine consente la visualizzazione di qualsiasi oggetto dietro l'immagine attraverso le aree trasparenti.</span><span class="sxs-lookup"><span data-stu-id="070ef-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="070ef-118">Il **pulsante** riceverà comunque i clic sull'area trasparente.</span><span class="sxs-lookup"><span data-stu-id="070ef-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="070ef-119">Il colore trasparente può essere qualsiasi valore di colore di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="070ef-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="070ef-120">Se il valore dell'attributo **transparencyColor** è impostato su "auto", viene usato il colore del pixel nella posizione 0, 0 nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="070ef-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="070ef-121">Se il colore specificato non è uno dei colori di IE validi, viene mantenuto il valore precedente.</span><span class="sxs-lookup"><span data-stu-id="070ef-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="070ef-122">Poiché i jpg sono con perdita di tempo e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate quando si usa **transparencyColor** .</span><span class="sxs-lookup"><span data-stu-id="070ef-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="070ef-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="070ef-123">Requirements</span></span>



| <span data-ttu-id="070ef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="070ef-124">Requirement</span></span> | <span data-ttu-id="070ef-125">Valore</span><span class="sxs-lookup"><span data-stu-id="070ef-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="070ef-126">Versione</span><span class="sxs-lookup"><span data-stu-id="070ef-126">Version</span></span><br/> | <span data-ttu-id="070ef-127">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="070ef-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="070ef-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="070ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070ef-129">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="070ef-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="070ef-130">**BUTTON. image**</span><span class="sxs-lookup"><span data-stu-id="070ef-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="070ef-131">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="070ef-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





