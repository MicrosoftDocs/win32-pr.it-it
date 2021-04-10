---
title: Effetto esposizione
description: Aumentare o ridurre l'esposizione dell'immagine.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964605"
---
# <a name="exposure-effect"></a><span data-ttu-id="4c0f1-103">Effetto esposizione</span><span class="sxs-lookup"><span data-stu-id="4c0f1-103">Exposure effect</span></span>

<span data-ttu-id="4c0f1-104">Aumentare o ridurre l'esposizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="4c0f1-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="4c0f1-105">Il CLSID per questo effetto è CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="4c0f1-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="4c0f1-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="4c0f1-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="4c0f1-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="4c0f1-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="4c0f1-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="4c0f1-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4c0f1-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c0f1-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4c0f1-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c0f1-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4c0f1-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="4c0f1-111">Example image</span></span>

![esempio di output di effetto](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="4c0f1-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="4c0f1-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="4c0f1-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="4c0f1-114">Effect properties</span></span>

<span data-ttu-id="4c0f1-115">Le proprietà per l'effetto di esposizione sono definite dall'enumerazione [**d2d1 \_ Exposure \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .</span><span class="sxs-lookup"><span data-stu-id="4c0f1-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c0f1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c0f1-116">Requirements</span></span>



| <span data-ttu-id="4c0f1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c0f1-117">Requirement</span></span> | <span data-ttu-id="4c0f1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4c0f1-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="4c0f1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c0f1-119">Minimum supported client</span></span> | <span data-ttu-id="4c0f1-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4c0f1-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c0f1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c0f1-121">Minimum supported server</span></span> | <span data-ttu-id="4c0f1-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4c0f1-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c0f1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c0f1-123">Header</span></span>                   | <span data-ttu-id="4c0f1-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="4c0f1-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="4c0f1-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c0f1-125">Library</span></span>                  | <span data-ttu-id="4c0f1-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4c0f1-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="4c0f1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c0f1-127">Related topics</span></span>

* [<span data-ttu-id="4c0f1-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="4c0f1-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




