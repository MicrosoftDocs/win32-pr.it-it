---
title: SLIDER. foregroundColor
description: L'attributo foregroundColor specifica o Recupera il colore di primo piano del controllo dispositivo di scorrimento.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Media Player Windows SLIDER. foregroundColor
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332246"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="636eb-104">SLIDER. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="636eb-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="636eb-105">L'attributo **ForegroundColor** specifica o Recupera il colore di primo piano del controllo dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="636eb-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="636eb-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="636eb-106">Possible Values</span></span>

<span data-ttu-id="636eb-107">Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="636eb-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="636eb-108">Il valore predefinito è "white".</span><span class="sxs-lookup"><span data-stu-id="636eb-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="636eb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="636eb-109">Remarks</span></span>

<span data-ttu-id="636eb-110">È possibile creare un controllo dispositivo di scorrimento di base specificando una delle due coppie di attributi: **BackgroundColor** e **ForegroundColor** oppure **BackgroundImage** e **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="636eb-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="636eb-111">Quando si crea un controllo dispositivo di scorrimento usando gli attributi di colore, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="636eb-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="636eb-112">Il colore di primo piano copre il colore di sfondo quando aumenta la posizione del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="636eb-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="636eb-113">Per creare un riempimento sfumato nell'area occupata dal colore di sfondo o di primo piano, specificare gli attributi **backgroundEndColor** o **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="636eb-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="636eb-114">Vedere *CUSTOMSLIDER*. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="636eb-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="636eb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="636eb-115">Requirements</span></span>



| <span data-ttu-id="636eb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="636eb-116">Requirement</span></span> | <span data-ttu-id="636eb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="636eb-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="636eb-118">Versione</span><span class="sxs-lookup"><span data-stu-id="636eb-118">Version</span></span><br/> | <span data-ttu-id="636eb-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="636eb-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="636eb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="636eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636eb-121">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="636eb-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="636eb-122">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="636eb-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="636eb-123">**SLIDER. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="636eb-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="636eb-124">**SLIDER. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="636eb-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="636eb-125">**SLIDER. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="636eb-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="636eb-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="636eb-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





