---
title: Effetto temperatura e tinta
description: .
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8a483b926b26c115002b2bb352d8e3120e7479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873817"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="b82de-103">Effetto temperatura e tinta</span><span class="sxs-lookup"><span data-stu-id="b82de-103">Temperature and tint effect</span></span>

<span data-ttu-id="b82de-104">Il CLSID per questo effetto è CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="b82de-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="b82de-105">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="b82de-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="b82de-106">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="b82de-106">Effect properties</span></span>

<span data-ttu-id="b82de-107">Le proprietà per l'effetto temperatura e tinta sono definite dall'enumerazione [**d2d1 \_ TEMPERATUREANDTINT \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) .</span><span class="sxs-lookup"><span data-stu-id="b82de-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82de-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b82de-108">Requirements</span></span>



| <span data-ttu-id="b82de-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b82de-109">Requirement</span></span> | <span data-ttu-id="b82de-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b82de-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b82de-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b82de-111">Minimum supported client</span></span> | <span data-ttu-id="b82de-112">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b82de-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b82de-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b82de-113">Minimum supported server</span></span> | <span data-ttu-id="b82de-114">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b82de-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b82de-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b82de-115">Header</span></span>                   | <span data-ttu-id="b82de-116">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b82de-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b82de-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="b82de-117">Library</span></span>                  | <span data-ttu-id="b82de-118">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b82de-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="b82de-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b82de-119">Related topics</span></span>

* [<span data-ttu-id="b82de-120">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="b82de-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
