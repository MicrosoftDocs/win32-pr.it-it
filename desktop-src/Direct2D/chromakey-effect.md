---
title: Effetto chiave Chroma
description: Converte un colore specificato più o meno una tolleranza in alfa. Ad esempio, Chroma-Key può rimuovere lo sfondo di un'immagine per un effetto di sovrapposizione della schermata verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873637"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="da7ae-104">Effetto chiave Chroma</span><span class="sxs-lookup"><span data-stu-id="da7ae-104">Chroma-key effect</span></span>

<span data-ttu-id="da7ae-105">Converte un colore specificato più o meno una tolleranza in alfa.</span><span class="sxs-lookup"><span data-stu-id="da7ae-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="da7ae-106">Ad esempio, Chroma-Key può rimuovere lo sfondo di un'immagine per un effetto di sovrapposizione della schermata verde.</span><span class="sxs-lookup"><span data-stu-id="da7ae-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="da7ae-107">Il CLSID per questo effetto è CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="da7ae-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="da7ae-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="da7ae-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="da7ae-109">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="da7ae-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="da7ae-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="da7ae-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="da7ae-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7ae-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="da7ae-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da7ae-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="da7ae-113">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="da7ae-113">Example image</span></span>

![esempio di output di effetto](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="da7ae-115">In questo esempio l'output dell'effetto della chiave Chroma è la seconda immagine con lo sfondo trasparente a scacchiera.</span><span class="sxs-lookup"><span data-stu-id="da7ae-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="da7ae-116">La terza immagine combina questo oggetto con un'immagine di sfondo per la sovrimpressione finale dello schermo verde.</span><span class="sxs-lookup"><span data-stu-id="da7ae-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="da7ae-117">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="da7ae-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="da7ae-118">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="da7ae-118">Effect properties</span></span>

<span data-ttu-id="da7ae-119">Le proprietà per l'effetto della chiave Chroma sono definite dall'enumerazione [**d2d1 \_ CHROMAKEY \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .</span><span class="sxs-lookup"><span data-stu-id="da7ae-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="da7ae-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7ae-120">Requirements</span></span>

| <span data-ttu-id="da7ae-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="da7ae-121">Requirement</span></span> | <span data-ttu-id="da7ae-122">Valore</span><span class="sxs-lookup"><span data-stu-id="da7ae-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="da7ae-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da7ae-123">Minimum supported client</span></span> | <span data-ttu-id="da7ae-124">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="da7ae-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da7ae-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da7ae-125">Minimum supported server</span></span> | <span data-ttu-id="da7ae-126">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="da7ae-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da7ae-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da7ae-127">Header</span></span>                   | <span data-ttu-id="da7ae-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="da7ae-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="da7ae-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="da7ae-129">Library</span></span>                  | <span data-ttu-id="da7ae-130">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="da7ae-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="da7ae-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da7ae-131">Related topics</span></span>

* [<span data-ttu-id="da7ae-132">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="da7ae-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
