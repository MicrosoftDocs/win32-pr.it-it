---
title: BUTTONGROUP. downImage
description: L'attributo downImage specifica o Recupera il nome dell'immagine che rappresenta lo stato di inattività di BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- Media Player Windows BUTTONGROUP. downImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327487"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="0c7c1-104">BUTTONGROUP. downImage</span><span class="sxs-lookup"><span data-stu-id="0c7c1-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="0c7c1-105">L'attributo **downImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato di inattività di **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="0c7c1-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="0c7c1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0c7c1-106">Possible Values</span></span>

<span data-ttu-id="0c7c1-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0c7c1-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c7c1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c7c1-108">Remarks</span></span>

<span data-ttu-id="0c7c1-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="0c7c1-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="0c7c1-110">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .</span><span class="sxs-lookup"><span data-stu-id="0c7c1-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="0c7c1-111">L'immagine predefinita è quella specificata nell'attributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="0c7c1-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="0c7c1-112">Se l'immagine inattiva è maggiore dell'area definita, l'immagine in basso verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="0c7c1-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="0c7c1-113">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="0c7c1-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7c1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c7c1-114">Requirements</span></span>



| <span data-ttu-id="0c7c1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c7c1-115">Requirement</span></span> | <span data-ttu-id="0c7c1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c7c1-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0c7c1-117">Versione</span><span class="sxs-lookup"><span data-stu-id="0c7c1-117">Version</span></span><br/> | <span data-ttu-id="0c7c1-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0c7c1-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c7c1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c7c1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7c1-120">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="0c7c1-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="0c7c1-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="0c7c1-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="0c7c1-122">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="0c7c1-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="0c7c1-123">**BUTTONGROUP. saturazione**</span><span class="sxs-lookup"><span data-stu-id="0c7c1-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





