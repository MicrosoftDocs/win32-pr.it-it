---
title: BUTTONGROUP. hoverDownImage
description: L'attributo hoverDownImage specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in BUTTONGROUP. Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- Media Player Windows BUTTONGROUP. hoverDownImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324104"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="1f52d-105">BUTTONGROUP. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="1f52d-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="1f52d-106">L'attributo **hoverDownImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="1f52d-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="1f52d-107">Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse.</span><span class="sxs-lookup"><span data-stu-id="1f52d-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="1f52d-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1f52d-108">Possible Values</span></span>

<span data-ttu-id="1f52d-109">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f52d-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f52d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f52d-110">Remarks</span></span>

<span data-ttu-id="1f52d-111">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="1f52d-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="1f52d-112">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .</span><span class="sxs-lookup"><span data-stu-id="1f52d-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="1f52d-113">L'immagine predefinita è quella specificata nell'attributo **downImage** o il relativo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f52d-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="1f52d-114">Se l'immagine al passaggio del mouse è più grande dell'area definita, l'immagine al passaggio del mouse verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="1f52d-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="1f52d-115">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="1f52d-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f52d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f52d-116">Requirements</span></span>



| <span data-ttu-id="1f52d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f52d-117">Requirement</span></span> | <span data-ttu-id="1f52d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1f52d-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1f52d-119">Versione</span><span class="sxs-lookup"><span data-stu-id="1f52d-119">Version</span></span><br/> | <span data-ttu-id="1f52d-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1f52d-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f52d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f52d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f52d-122">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="1f52d-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="1f52d-123">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="1f52d-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="1f52d-124">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="1f52d-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="1f52d-125">**BUTTONGROUP. saturazione**</span><span class="sxs-lookup"><span data-stu-id="1f52d-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





