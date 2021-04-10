---
title: Effetto tonalità-RGB
description: Converte un'immagine HSL (Hue, Saturation, luminosità) o HSV (Hue, Saturation, value) nello spazio colori RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964150"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="46c95-103">Effetto tonalità-RGB</span><span class="sxs-lookup"><span data-stu-id="46c95-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="46c95-104">Converte un'immagine HSL (Hue, Saturation, luminosità) o HSV (Hue, Saturation, value) nello spazio colori RGB.</span><span class="sxs-lookup"><span data-stu-id="46c95-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="46c95-105">HSL e HSV sono due modelli diversi per la rappresentazione di un colore RGB in uno spazio di colore cilindrico.</span><span class="sxs-lookup"><span data-stu-id="46c95-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="46c95-106">Sono utili perché consentono di ragionare su un colore usando concetti più intuitivi, ad esempio Hue e Intensity, e combinando i valori rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="46c95-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="46c95-107">Questo effetto passa tutti i valori alfa di input.</span><span class="sxs-lookup"><span data-stu-id="46c95-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="46c95-108">Il CLSID per questo effetto è CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="46c95-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="46c95-109">Per invertire il comportamento di questo effetto, usare l' [effetto RGB a tonalità](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="46c95-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="46c95-110">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="46c95-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="46c95-111">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="46c95-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="46c95-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46c95-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="46c95-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46c95-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="46c95-114">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="46c95-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="46c95-115">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="46c95-115">Effect properties</span></span>

<span data-ttu-id="46c95-116">Le proprietà per l'effetto contrasto sono definite dall'enumerazione [**d2d1 \_ HUETORGB \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .</span><span class="sxs-lookup"><span data-stu-id="46c95-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c95-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46c95-117">Requirements</span></span>



| <span data-ttu-id="46c95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c95-118">Requirement</span></span> | <span data-ttu-id="46c95-119">Valore</span><span class="sxs-lookup"><span data-stu-id="46c95-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="46c95-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46c95-120">Minimum supported client</span></span> | <span data-ttu-id="46c95-121">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="46c95-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="46c95-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46c95-122">Minimum supported server</span></span> | <span data-ttu-id="46c95-123">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="46c95-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="46c95-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46c95-124">Header</span></span>                   | <span data-ttu-id="46c95-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="46c95-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="46c95-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="46c95-126">Library</span></span>                  | <span data-ttu-id="46c95-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="46c95-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="46c95-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46c95-128">Related topics</span></span>

* [<span data-ttu-id="46c95-129">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="46c95-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
