---
title: Metodi ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1.h)
description: Crea un oggetto ID2D1GradientStopCollection dalla matrice specificata di strutture GRADIENT STOP D2D1. \_ \_
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Metodi CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e149727650223f40a290d1ada40abc69f9033440
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380635"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="d818e-104">Metodi ID2D1RenderTarget::CreateGradientStopCollection</span><span class="sxs-lookup"><span data-stu-id="d818e-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="d818e-105">Crea un [**oggetto ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) dalla matrice specificata di strutture [**GRADIENT \_ \_ STOP D2D1.**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)</span><span class="sxs-lookup"><span data-stu-id="d818e-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d818e-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="d818e-106">Overload list</span></span>



| <span data-ttu-id="d818e-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="d818e-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="d818e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d818e-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d818e-109">[**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,D2D1 \_ GAMMA,D2D1 \_ EXTEND \_ MODE,ID2D1GradientStopCollection \* \* )**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d818e-109">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span> | <span data-ttu-id="d818e-110">Crea un [**oggetto ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) dalle interruzioni della sfumatura, dall'interpolazione di colori e dalla modalità di estensione specificati.</span><span class="sxs-lookup"><span data-stu-id="d818e-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| <span data-ttu-id="d818e-111">[**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ \* STOP,ID2D1GradientStopCollection \* \* )**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d818e-111">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span>                                                            | <span data-ttu-id="d818e-112">Crea un [**oggetto ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) dalle interruzioni della sfumatura specificate che usa l'interpolazione di colore gamma [**D2D1 \_ GAMMA \_ \_ 2 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) e la modalità di estensione della chiusura.</span><span class="sxs-lookup"><span data-stu-id="d818e-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="d818e-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="d818e-113">Examples</span></span>

<span data-ttu-id="d818e-114">Nell'esempio seguente viene creata una matrice di cursori sfumatura, quindi vengono utilizzati per creare un [**oggetto ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="d818e-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="d818e-115">L'esempio di codice successivo usa [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) per creare un [**oggetto ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)</span><span class="sxs-lookup"><span data-stu-id="d818e-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="d818e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d818e-116">Requirements</span></span>



| <span data-ttu-id="d818e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d818e-117">Requirement</span></span> | <span data-ttu-id="d818e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d818e-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d818e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d818e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d818e-120"><dt>D2d1 \_ 1.h (includere D2d1.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d818e-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="d818e-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d818e-121">Library</span></span><br/> | <dl> <span data-ttu-id="d818e-122"><dt>D2d1.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d818e-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d818e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d818e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d818e-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d818e-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="d818e-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d818e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d818e-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="d818e-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="d818e-127">**CURSORE SFUMATURA D2D1 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d818e-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="d818e-128">Come creare un pennello a sfumatura lineare</span><span class="sxs-lookup"><span data-stu-id="d818e-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="d818e-129">Come creare un pennello sfumatura radiale</span><span class="sxs-lookup"><span data-stu-id="d818e-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="d818e-130">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="d818e-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>
