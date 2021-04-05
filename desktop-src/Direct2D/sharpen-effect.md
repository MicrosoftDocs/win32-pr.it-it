---
title: Effetto Nitidezza
description: Affila l'immagine.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741178"
---
# <a name="sharpen-effect"></a><span data-ttu-id="11e64-103">Effetto Nitidezza</span><span class="sxs-lookup"><span data-stu-id="11e64-103">Sharpen effect</span></span>

<span data-ttu-id="11e64-104">Affila l'immagine.</span><span class="sxs-lookup"><span data-stu-id="11e64-104">Sharpens the image.</span></span>

<span data-ttu-id="11e64-105">Il CLSID per questo effetto è CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="11e64-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="11e64-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="11e64-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="11e64-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="11e64-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="11e64-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="11e64-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="11e64-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11e64-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="11e64-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11e64-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="11e64-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="11e64-111">Example image</span></span>

![esempio di output di effetto](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="11e64-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="11e64-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="11e64-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="11e64-114">Effect properties</span></span>

<span data-ttu-id="11e64-115">Le proprietà per l'effetto di nitidezza sono definite dall'enumerazione [**d2d1 \_ Sharpe \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .</span><span class="sxs-lookup"><span data-stu-id="11e64-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e64-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11e64-116">Requirements</span></span>



| <span data-ttu-id="11e64-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e64-117">Requirement</span></span> | <span data-ttu-id="11e64-118">Valore</span><span class="sxs-lookup"><span data-stu-id="11e64-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="11e64-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e64-119">Minimum supported client</span></span> | <span data-ttu-id="11e64-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="11e64-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11e64-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e64-121">Minimum supported server</span></span> | <span data-ttu-id="11e64-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="11e64-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11e64-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11e64-123">Header</span></span>                   | <span data-ttu-id="11e64-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="11e64-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="11e64-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="11e64-125">Library</span></span>                  | <span data-ttu-id="11e64-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="11e64-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="11e64-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11e64-127">Related topics</span></span>

* [<span data-ttu-id="11e64-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="11e64-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



