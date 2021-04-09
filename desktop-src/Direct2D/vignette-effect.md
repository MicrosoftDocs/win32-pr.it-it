---
title: Effetto vignette
description: Dissolve l'immagine di input ai bordi di un colore impostato dall'utente.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120607"
---
# <a name="vignette-effect"></a><span data-ttu-id="85b03-103">Effetto vignette</span><span class="sxs-lookup"><span data-stu-id="85b03-103">Vignette effect</span></span>

<span data-ttu-id="85b03-104">Dissolve l'immagine di input ai bordi di un colore impostato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="85b03-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="85b03-105">Il CLSID per questo effetto è CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="85b03-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="85b03-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="85b03-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="85b03-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="85b03-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="85b03-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="85b03-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="85b03-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85b03-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="85b03-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85b03-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="85b03-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="85b03-111">Example image</span></span>

![esempio di output di effetto](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="85b03-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="85b03-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="85b03-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="85b03-114">Effect properties</span></span>

<span data-ttu-id="85b03-115">Le proprietà per l'effetto vignette sono definite dall'enumerazione [**d2d1 \_ vignette \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .</span><span class="sxs-lookup"><span data-stu-id="85b03-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b03-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85b03-116">Requirements</span></span>

| <span data-ttu-id="85b03-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b03-117">Requirement</span></span> | <span data-ttu-id="85b03-118">Valore</span><span class="sxs-lookup"><span data-stu-id="85b03-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="85b03-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85b03-119">Minimum supported client</span></span> | <span data-ttu-id="85b03-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="85b03-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85b03-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85b03-121">Minimum supported server</span></span> | <span data-ttu-id="85b03-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="85b03-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85b03-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85b03-123">Header</span></span>                   | <span data-ttu-id="85b03-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="85b03-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="85b03-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="85b03-125">Library</span></span>                  | <span data-ttu-id="85b03-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="85b03-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="85b03-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85b03-127">Related topics</span></span>

* [<span data-ttu-id="85b03-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="85b03-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
