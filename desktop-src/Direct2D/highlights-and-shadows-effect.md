---
title: Effetti evidenziazione e ombreggiatura
description: Regola le evidenziazioni e le ombre dell'immagine.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104551149"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="77bca-103">Effetti evidenziazione e ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="77bca-103">Highlights and shadows effect</span></span>

<span data-ttu-id="77bca-104">Regola le evidenziazioni e le ombre dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="77bca-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="77bca-105">Il CLSID per questo effetto è CLSID \_ D2D1HighlightsShadows.</span><span class="sxs-lookup"><span data-stu-id="77bca-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="77bca-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="77bca-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="77bca-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="77bca-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="77bca-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="77bca-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="77bca-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77bca-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="77bca-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77bca-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="77bca-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="77bca-111">Example image</span></span>

![esempio di output di effetto](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="77bca-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="77bca-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="77bca-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="77bca-114">Effect properties</span></span>

<span data-ttu-id="77bca-115">Le proprietà per gli effetti evidenziazione e ombreggiatura sono definite dall'enumerazione [**d2d1 \_ HIGHLIGHTSANDSHADOWS \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) .</span><span class="sxs-lookup"><span data-stu-id="77bca-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="77bca-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77bca-116">Requirements</span></span>

| <span data-ttu-id="77bca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77bca-117">Requirement</span></span> | <span data-ttu-id="77bca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="77bca-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="77bca-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77bca-119">Minimum supported client</span></span> | <span data-ttu-id="77bca-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="77bca-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="77bca-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77bca-121">Minimum supported server</span></span> | <span data-ttu-id="77bca-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="77bca-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="77bca-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77bca-123">Header</span></span>                   | <span data-ttu-id="77bca-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="77bca-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="77bca-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="77bca-125">Library</span></span>                  | <span data-ttu-id="77bca-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="77bca-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="77bca-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77bca-127">Related topics</span></span>

* [<span data-ttu-id="77bca-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="77bca-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
