---
title: BUTTONGROUP. image
description: L'attributo Image specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Media Player Windows BUTTONGROUP. image
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332140"
---
# <a name="buttongroupimage"></a><span data-ttu-id="f4d4b-104">BUTTONGROUP. image</span><span class="sxs-lookup"><span data-stu-id="f4d4b-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="f4d4b-105">L'attributo **Image** specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="f4d4b-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="f4d4b-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f4d4b-106">Possible Values</span></span>

<span data-ttu-id="f4d4b-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f4d4b-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d4b-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4d4b-108">Remarks</span></span>

<span data-ttu-id="f4d4b-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="f4d4b-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="f4d4b-110">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .</span><span class="sxs-lookup"><span data-stu-id="f4d4b-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="f4d4b-111">Se l'immagine del controllo è più grande dell'area definita, l'immagine verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="f4d4b-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="f4d4b-112">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="f4d4b-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d4b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4d4b-113">Requirements</span></span>



| <span data-ttu-id="f4d4b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4d4b-114">Requirement</span></span> | <span data-ttu-id="f4d4b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f4d4b-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f4d4b-116">Versione</span><span class="sxs-lookup"><span data-stu-id="f4d4b-116">Version</span></span><br/> | <span data-ttu-id="f4d4b-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="f4d4b-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4d4b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4d4b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4d4b-119">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="f4d4b-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="f4d4b-120">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="f4d4b-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="f4d4b-121">**BUTTONGROUP. saturazione**</span><span class="sxs-lookup"><span data-stu-id="f4d4b-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





