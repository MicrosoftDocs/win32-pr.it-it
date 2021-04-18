---
title: Effetto di raddrizzamento
description: Ruota e, facoltativamente, ridimensiona un'immagine.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104563592"
---
# <a name="straighten-effect"></a><span data-ttu-id="36917-103">Effetto di raddrizzamento</span><span class="sxs-lookup"><span data-stu-id="36917-103">Straighten effect</span></span>

<span data-ttu-id="36917-104">Ruota e, facoltativamente, ridimensiona un'immagine.</span><span class="sxs-lookup"><span data-stu-id="36917-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="36917-105">Il CLSID per questo effetto è CLSID \_ D2D1Straighten.</span><span class="sxs-lookup"><span data-stu-id="36917-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="36917-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="36917-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="36917-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="36917-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="36917-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="36917-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="36917-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36917-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="36917-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36917-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="36917-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="36917-111">Example image</span></span>

![esempio di output di effetto](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="36917-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="36917-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="36917-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="36917-114">Effect properties</span></span>

<span data-ttu-id="36917-115">Le proprietà per l'effetto di raddrizzamento sono definite dall'enumerazione [**d2d1 \_ Raddrizza \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) .</span><span class="sxs-lookup"><span data-stu-id="36917-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="36917-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36917-116">Requirements</span></span>



| <span data-ttu-id="36917-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36917-117">Requirement</span></span> | <span data-ttu-id="36917-118">Valore</span><span class="sxs-lookup"><span data-stu-id="36917-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="36917-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36917-119">Minimum supported client</span></span> | <span data-ttu-id="36917-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="36917-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="36917-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36917-121">Minimum supported server</span></span> | <span data-ttu-id="36917-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="36917-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="36917-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36917-123">Header</span></span>                   | <span data-ttu-id="36917-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="36917-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="36917-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="36917-125">Library</span></span>                  | <span data-ttu-id="36917-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="36917-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="36917-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36917-127">Related topics</span></span>

* [<span data-ttu-id="36917-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="36917-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

