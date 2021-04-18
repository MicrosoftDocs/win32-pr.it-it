---
title: Metodi CreateEllipseGeometry di ID2D1Factory (D2d1. h)
description: Crea un ID2D1EllipseGeometry.
ms.assetid: 4c03bb0b-74fe-456a-aa26-5449d758c0ea
keywords:
- Metodo CreateEllipseGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ca991732b9a80fd93e3df3c2b72493f5195ea0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329887"
---
# <a name="id2d1factorycreateellipsegeometry-methods"></a><span data-ttu-id="01c04-104">Metodi ID2D1Factory:: CreateEllipseGeometry</span><span class="sxs-lookup"><span data-stu-id="01c04-104">ID2D1Factory::CreateEllipseGeometry methods</span></span>

<span data-ttu-id="01c04-105">Crea un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="01c04-105">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span>

### <a name="overload-list"></a><span data-ttu-id="01c04-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="01c04-106">Overload list</span></span>



| <span data-ttu-id="01c04-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="01c04-107">Method</span></span>                                                                                                                                                      | <span data-ttu-id="01c04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01c04-108">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="01c04-109">[**CreateEllipseGeometry (D2D1 \_ ELLIPSE&, ID2D1EllipseGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span><span class="sxs-lookup"><span data-stu-id="01c04-109">[**CreateEllipseGeometry(D2D1\_ELLIPSE&,ID2D1EllipseGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span></span>  | <span data-ttu-id="01c04-110">Crea un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="01c04-110">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |
| <span data-ttu-id="01c04-111">[**CreateEllipseGeometry ( \_ ellisse d2d1 \* , ID2D1EllipseGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01c04-111">[**CreateEllipseGeometry(D2D1\_ELLIPSE\*,ID2D1EllipseGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span></span> | <span data-ttu-id="01c04-112">Crea un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="01c04-112">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="01c04-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="01c04-113">Examples</span></span>

<span data-ttu-id="01c04-114">Il codice seguente crea due oggetti [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e li combina usando le diverse modalità di combinazione della geometria.</span><span class="sxs-lookup"><span data-stu-id="01c04-114">The following creates two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and combines them using the different geometry combine modes.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="01c04-115">Questo codice produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="01c04-115">This code produces the output shown in the following illustration.</span></span>

![illustrazione di due ellissi combinati usando quattro modalità di combinazione di geometria (Union, Intersect, XOR ed Exclude)](images/combine-modes.png)

## <a name="requirements"></a><span data-ttu-id="01c04-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c04-117">Requirements</span></span>



| <span data-ttu-id="01c04-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c04-118">Requirement</span></span> | <span data-ttu-id="01c04-119">Valore</span><span class="sxs-lookup"><span data-stu-id="01c04-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01c04-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c04-120">Header</span></span><br/>  | <dl> <span data-ttu-id="01c04-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c04-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="01c04-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="01c04-122">Library</span></span><br/> | <dl> <span data-ttu-id="01c04-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01c04-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="01c04-124">DLL</span><span class="sxs-lookup"><span data-stu-id="01c04-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="01c04-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c04-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c04-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c04-127">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="01c04-127">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
