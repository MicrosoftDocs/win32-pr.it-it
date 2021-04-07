---
title: Effetto Posterizzazione
description: L'effetto Posterizzazione riduce il numero di colori univoci in un'immagine.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048537"
---
# <a name="posterize-effect"></a><span data-ttu-id="12d4f-103">Effetto Posterizzazione</span><span class="sxs-lookup"><span data-stu-id="12d4f-103">Posterize effect</span></span>

<span data-ttu-id="12d4f-104">L'effetto Posterizzazione riduce il numero di colori univoci in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="12d4f-104">The posterize effect reduces the number of unique colors in an image.</span></span>

<span data-ttu-id="12d4f-105">Il CLSID per questo effetto è CLSID \_ D2D1Posterize.</span><span class="sxs-lookup"><span data-stu-id="12d4f-105">The CLSID for this effect is CLSID\_D2D1Posterize.</span></span>

-   [<span data-ttu-id="12d4f-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="12d4f-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="12d4f-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="12d4f-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="12d4f-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="12d4f-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="12d4f-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d4f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="12d4f-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12d4f-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="12d4f-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="12d4f-111">Example image</span></span>

![esempio di output di effetto](images/posterize-effect.png)

## <a name="sample-code"></a><span data-ttu-id="12d4f-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="12d4f-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="12d4f-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="12d4f-114">Effect properties</span></span>

<span data-ttu-id="12d4f-115">Le proprietà per l'effetto Posterizzazione sono definite dall'enumerazione [**d2d1 \_ posterizzazione \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) .</span><span class="sxs-lookup"><span data-stu-id="12d4f-115">The properties for the posterize effect are defined by the [**D2D1\_POSTERIZE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d4f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d4f-116">Requirements</span></span>



| <span data-ttu-id="12d4f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d4f-117">Requirement</span></span> | <span data-ttu-id="12d4f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="12d4f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="12d4f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d4f-119">Minimum supported client</span></span> | <span data-ttu-id="12d4f-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12d4f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12d4f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d4f-121">Minimum supported server</span></span> | <span data-ttu-id="12d4f-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="12d4f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="12d4f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12d4f-123">Header</span></span>                   | <span data-ttu-id="12d4f-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="12d4f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="12d4f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="12d4f-125">Library</span></span>                  | <span data-ttu-id="12d4f-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="12d4f-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="12d4f-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12d4f-127">Related topics</span></span>

* [<span data-ttu-id="12d4f-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="12d4f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


