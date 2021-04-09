---
title: Effetto rilevamento Edge
description: Filtra il contenuto di un'immagine, lasciando le linee ai bordi delle sezioni a contrasto dell'immagine.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048765"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="56147-103">Effetto rilevamento Edge</span><span class="sxs-lookup"><span data-stu-id="56147-103">Edge-detection effect</span></span>

<span data-ttu-id="56147-104">Filtra il contenuto di un'immagine, lasciando le linee ai bordi delle sezioni a contrasto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="56147-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="56147-105">Il CLSID per questo effetto è CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="56147-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="56147-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="56147-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="56147-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="56147-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="56147-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="56147-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="56147-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56147-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="56147-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56147-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="56147-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="56147-111">Example image</span></span>

![esempio di output di effetto](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="56147-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="56147-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="56147-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="56147-114">Effect properties</span></span>

<span data-ttu-id="56147-115">Le proprietà per l'effetto di rilevamento bordo sono definite dall'enumerazione [**d2d1 \_ EDGEDETECTION \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .</span><span class="sxs-lookup"><span data-stu-id="56147-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="56147-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56147-116">Requirements</span></span>



| <span data-ttu-id="56147-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="56147-117">Requirement</span></span> | <span data-ttu-id="56147-118">Valore</span><span class="sxs-lookup"><span data-stu-id="56147-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="56147-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56147-119">Minimum supported client</span></span> | <span data-ttu-id="56147-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="56147-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="56147-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56147-121">Minimum supported server</span></span> | <span data-ttu-id="56147-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="56147-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="56147-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56147-123">Header</span></span>                   | <span data-ttu-id="56147-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="56147-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="56147-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="56147-125">Library</span></span>                  | <span data-ttu-id="56147-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="56147-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="56147-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56147-127">Related topics</span></span>

* [<span data-ttu-id="56147-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="56147-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
