---
title: Effetto rilievo
description: Crea una versione in scala di grigi dell'immagine visualizzata come se fosse stata contrassegnata come carta.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741535"
---
# <a name="emboss-effect"></a><span data-ttu-id="ba0a5-103">Effetto rilievo</span><span class="sxs-lookup"><span data-stu-id="ba0a5-103">Emboss effect</span></span>

<span data-ttu-id="ba0a5-104">Crea una versione in scala di grigi dell'immagine visualizzata come se fosse stata contrassegnata come carta.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="ba0a5-105">Il CLSID per questo effetto è CLSID \_ D2D1Emboss.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="ba0a5-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="ba0a5-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="ba0a5-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="ba0a5-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="ba0a5-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="ba0a5-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ba0a5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0a5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ba0a5-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba0a5-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ba0a5-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="ba0a5-111">Example image</span></span>

![esempio di output di effetto](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="ba0a5-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="ba0a5-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="ba0a5-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="ba0a5-114">Effect properties</span></span>

<span data-ttu-id="ba0a5-115">Le proprietà per l'effetto di rilievo sono definite dall'enumerazione [**d2d1 \_ emboss \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .</span><span class="sxs-lookup"><span data-stu-id="ba0a5-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0a5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0a5-116">Requirements</span></span>



| <span data-ttu-id="ba0a5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0a5-117">Requirement</span></span> | <span data-ttu-id="ba0a5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ba0a5-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="ba0a5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0a5-119">Minimum supported client</span></span> | <span data-ttu-id="ba0a5-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ba0a5-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ba0a5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0a5-121">Minimum supported server</span></span> | <span data-ttu-id="ba0a5-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ba0a5-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ba0a5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba0a5-123">Header</span></span>                   | <span data-ttu-id="ba0a5-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="ba0a5-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="ba0a5-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba0a5-125">Library</span></span>                  | <span data-ttu-id="ba0a5-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ba0a5-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="ba0a5-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba0a5-127">Related topics</span></span>

* [<span data-ttu-id="ba0a5-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="ba0a5-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
