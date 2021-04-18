---
title: SLIDER. Value
description: L'attributo value specifica o recupera la posizione corrente del dispositivo di scorrimento. | SLIDER. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Media Player SLIDER. Value Windows
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327703"
---
# <a name="slidervalue"></a><span data-ttu-id="5104d-105">SLIDER. Value</span><span class="sxs-lookup"><span data-stu-id="5104d-105">SLIDER.value</span></span>

<span data-ttu-id="5104d-106">L'attributo **value** specifica o recupera la posizione corrente del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5104d-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="5104d-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5104d-107">Possible Values</span></span>

<span data-ttu-id="5104d-108">Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore predefinito di **min**.</span><span class="sxs-lookup"><span data-stu-id="5104d-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5104d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5104d-109">Remarks</span></span>

<span data-ttu-id="5104d-110">Il **valore** deve essere sempre maggiore o uguale a **min** e minore o uguale a **Max**. Se si specifica un valore non compreso in questo intervallo, il **valore** e la posizione del dispositivo di scorrimento non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="5104d-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="5104d-111">Vedere **CUSTOMSLIDER**. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="5104d-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5104d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5104d-112">Requirements</span></span>



| <span data-ttu-id="5104d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5104d-113">Requirement</span></span> | <span data-ttu-id="5104d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5104d-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5104d-115">Versione</span><span class="sxs-lookup"><span data-stu-id="5104d-115">Version</span></span><br/> | <span data-ttu-id="5104d-116">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5104d-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5104d-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5104d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5104d-118">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="5104d-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="5104d-119">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="5104d-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





