---
title: SLIDER. backgroundColor
description: L'attributo backgroundColor specifica o Recupera il colore di sfondo del controllo dispositivo di scorrimento.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Windows SLIDER. backgroundColor Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325128"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="3bc57-104">SLIDER. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3bc57-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="3bc57-105">L'attributo **BackgroundColor** specifica o Recupera il colore di sfondo del controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3bc57-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="3bc57-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3bc57-106">Possible Values</span></span>

<span data-ttu-id="3bc57-107">Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3bc57-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="3bc57-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3bc57-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc57-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bc57-109">Remarks</span></span>

<span data-ttu-id="3bc57-110">Un controllo dispositivo di scorrimento di base può essere creato specificando **BackgroundColor** o **BackgroundImage**, **ForegroundColor** o **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="3bc57-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="3bc57-111">Quando si usano i colori, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="3bc57-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="3bc57-112">Il colore di primo piano copre il colore di sfondo quando aumenta la posizione del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3bc57-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="3bc57-113">Per creare un riempimento sfumato dell'area occupata dal colore di sfondo o di primo piano, specificare gli attributi **backgroundEndColor** o **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="3bc57-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="3bc57-114">Vedere *CUSTOMSLIDER*. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="3bc57-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc57-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bc57-115">Requirements</span></span>



| <span data-ttu-id="3bc57-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc57-116">Requirement</span></span> | <span data-ttu-id="3bc57-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3bc57-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3bc57-118">Versione</span><span class="sxs-lookup"><span data-stu-id="3bc57-118">Version</span></span><br/> | <span data-ttu-id="3bc57-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="3bc57-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bc57-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bc57-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc57-121">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="3bc57-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="3bc57-122">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="3bc57-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="3bc57-123">**SLIDER. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="3bc57-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="3bc57-124">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="3bc57-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="3bc57-125">**SLIDER. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="3bc57-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="3bc57-126">**SLIDER. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="3bc57-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="3bc57-127">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="3bc57-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





