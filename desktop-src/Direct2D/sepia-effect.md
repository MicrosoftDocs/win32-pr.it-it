---
title: Effetto seppia
description: Converte un'immagine in tonalità seppia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964102"
---
# <a name="sepia-effect"></a><span data-ttu-id="8292e-103">Effetto seppia</span><span class="sxs-lookup"><span data-stu-id="8292e-103">Sepia effect</span></span>

<span data-ttu-id="8292e-104">Converte un'immagine in tonalità seppia.</span><span class="sxs-lookup"><span data-stu-id="8292e-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="8292e-105">Il CLSID per questo effetto è CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="8292e-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="8292e-106">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="8292e-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="8292e-107">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8292e-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="8292e-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="8292e-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8292e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8292e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8292e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8292e-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8292e-111">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="8292e-111">Example image</span></span>

![esempio di output di effetto](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="8292e-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8292e-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="8292e-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="8292e-114">Effect properties</span></span>

<span data-ttu-id="8292e-115">Le proprietà per l'effetto seppia sono definite dall'enumerazione [**d2d1 \_ seppia \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .</span><span class="sxs-lookup"><span data-stu-id="8292e-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8292e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8292e-116">Requirements</span></span>



| <span data-ttu-id="8292e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8292e-117">Requirement</span></span> | <span data-ttu-id="8292e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8292e-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="8292e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8292e-119">Minimum supported client</span></span> | <span data-ttu-id="8292e-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8292e-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8292e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8292e-121">Minimum supported server</span></span> | <span data-ttu-id="8292e-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8292e-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8292e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8292e-123">Header</span></span>                   | <span data-ttu-id="8292e-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="8292e-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="8292e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8292e-125">Library</span></span>                  | <span data-ttu-id="8292e-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8292e-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="8292e-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8292e-127">Related topics</span></span>

* [<span data-ttu-id="8292e-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="8292e-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




