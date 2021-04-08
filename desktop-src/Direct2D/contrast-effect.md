---
title: Effetto contrasto
description: Aumenta o riduce il contrasto di un'immagine.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048472"
---
# <a name="contrast-effect"></a><span data-ttu-id="bc815-103">Effetto contrasto</span><span class="sxs-lookup"><span data-stu-id="bc815-103">Contrast effect</span></span>

<span data-ttu-id="bc815-104">Aumenta o riduce il contrasto di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc815-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="bc815-105">Il CLSID per questo effetto è CLSID \_ D2D1Contrast.</span><span class="sxs-lookup"><span data-stu-id="bc815-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="bc815-106">La funzione di contrasto modifica ogni valore del canale colori utilizzando due polinomi quadratici a tratti che soddisfano la continuità della pendenza nel punto (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="bc815-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![a tratti polinomi quadratici che soddisfano la continuità della pendenza nel punto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [<span data-ttu-id="bc815-108">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="bc815-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="bc815-109">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bc815-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="bc815-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bc815-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="bc815-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc815-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bc815-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc815-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="bc815-113">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="bc815-113">Example images</span></span>

<span data-ttu-id="bc815-114">Questo esempio mostra l'output dell'effetto con il contrasto massimo applicato (contrasto = 1,0).</span><span class="sxs-lookup"><span data-stu-id="bc815-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="bc815-115">Prima</span><span class="sxs-lookup"><span data-stu-id="bc815-115">Before</span></span>

![immagine prima dell'applicazione dell'effetto](images/contrast-effect-before.png)

<span data-ttu-id="bc815-117">After</span><span class="sxs-lookup"><span data-stu-id="bc815-117">After</span></span>

![immagine dopo l'applicazione dell'effetto](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="bc815-119">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="bc815-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="bc815-120">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bc815-120">Effect properties</span></span>

<span data-ttu-id="bc815-121">Le proprietà per l'effetto di contrasto sono definite dall'enumerazione [**d2d1 \_ contrasto \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .</span><span class="sxs-lookup"><span data-stu-id="bc815-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc815-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc815-122">Requirements</span></span>

| <span data-ttu-id="bc815-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc815-123">Requirement</span></span> | <span data-ttu-id="bc815-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bc815-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="bc815-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc815-125">Minimum supported client</span></span> | <span data-ttu-id="bc815-126">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bc815-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bc815-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc815-127">Minimum supported server</span></span> | <span data-ttu-id="bc815-128">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bc815-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bc815-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc815-129">Header</span></span>                   | <span data-ttu-id="bc815-130">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="bc815-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="bc815-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc815-131">Library</span></span>                  | <span data-ttu-id="bc815-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="bc815-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="bc815-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc815-133">Related topics</span></span>

* [<span data-ttu-id="bc815-134">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="bc815-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
