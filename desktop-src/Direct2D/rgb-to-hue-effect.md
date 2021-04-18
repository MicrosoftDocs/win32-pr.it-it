---
title: Effetto RGB-to-Hue
description: Converte un'immagine RGB negli spazi dei colori HSL (Hue, Saturation, Lightity) o HSV (Hue, Saturation, value).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400540"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="b2429-103">Effetto RGB-to-Hue</span><span class="sxs-lookup"><span data-stu-id="b2429-103">RGB-to-hue effect</span></span>

<span data-ttu-id="b2429-104">Converte un'immagine RGB negli spazi dei colori HSL (Hue, Saturation, Lightity) o HSV (Hue, Saturation, value).</span><span class="sxs-lookup"><span data-stu-id="b2429-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="b2429-105">HSL e HSV sono due modelli diversi per la rappresentazione di un colore RGB in uno spazio di colore cilindrico.</span><span class="sxs-lookup"><span data-stu-id="b2429-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="b2429-106">Sono utili perché consentono di ragionare su un colore usando concetti più intuitivi, ad esempio Hue e Intensity, e combinando i valori rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="b2429-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="b2429-107">Questo effetto Normalizza i dati di output (tonalità, valore di saturazione per HSV o tonalità, saturazione, luminosità per HSL) nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b2429-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="b2429-108">Il CLSID per questo effetto è CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="b2429-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="b2429-109">Per invertire il comportamento di questo effetto, usare l' [effetto tonalità su RGB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="b2429-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="b2429-110">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="b2429-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="b2429-111">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="b2429-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b2429-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2429-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b2429-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2429-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="b2429-114">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="b2429-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="b2429-115">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="b2429-115">Effect properties</span></span>

<span data-ttu-id="b2429-116">Le proprietà per l'effetto contrasto sono definite dall'enumerazione [**d2d1 \_ RGBTOHUE \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .</span><span class="sxs-lookup"><span data-stu-id="b2429-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2429-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2429-117">Requirements</span></span>



| <span data-ttu-id="b2429-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2429-118">Requirement</span></span> | <span data-ttu-id="b2429-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b2429-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b2429-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2429-120">Minimum supported client</span></span> | <span data-ttu-id="b2429-121">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b2429-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b2429-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2429-122">Minimum supported server</span></span> | <span data-ttu-id="b2429-123">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b2429-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b2429-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2429-124">Header</span></span>                   | <span data-ttu-id="b2429-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b2429-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b2429-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2429-126">Library</span></span>                  | <span data-ttu-id="b2429-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b2429-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="b2429-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2429-128">Related topics</span></span>

* [<span data-ttu-id="b2429-129">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="b2429-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
