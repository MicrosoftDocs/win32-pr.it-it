---
title: BUTTONGROUP. disabledImage
description: L'attributo disabledImage specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Media Player Windows BUTTONGROUP. disabledImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324997"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="e0358-104">BUTTONGROUP. disabledImage</span><span class="sxs-lookup"><span data-stu-id="e0358-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="e0358-105">L'attributo **disabledImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="e0358-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="e0358-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e0358-106">Possible Values</span></span>

<span data-ttu-id="e0358-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e0358-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0358-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0358-108">Remarks</span></span>

<span data-ttu-id="e0358-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="e0358-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="e0358-110">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .</span><span class="sxs-lookup"><span data-stu-id="e0358-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="e0358-111">Quando l'attributo **disabled** di un elemento **ButtonElement** è impostato su true, viene visualizzata l'area corrispondente di **disabledImage** per **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="e0358-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="e0358-112">Se l'immagine disabilitata è più grande dell'area definita, l'immagine disabilitata verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="e0358-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="e0358-113">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="e0358-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0358-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0358-114">Requirements</span></span>



| <span data-ttu-id="e0358-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0358-115">Requirement</span></span> | <span data-ttu-id="e0358-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e0358-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e0358-117">Versione</span><span class="sxs-lookup"><span data-stu-id="e0358-117">Version</span></span><br/> | <span data-ttu-id="e0358-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="e0358-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0358-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0358-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0358-120">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="e0358-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="e0358-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="e0358-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="e0358-122">**BUTTONGROUP. saturazione**</span><span class="sxs-lookup"><span data-stu-id="e0358-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





