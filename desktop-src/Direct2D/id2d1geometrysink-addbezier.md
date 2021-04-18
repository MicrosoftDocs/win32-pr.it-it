---
title: Metodi AddBezier di ID2D1GeometrySink (D2d1. h)
description: Crea una curva di Bezier cubica tra il punto corrente e il punto finale specificato e la aggiunge al sink di geometria.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Metodo AddBezier Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330073"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a><span data-ttu-id="d41c3-104">Metodi ID2D1GeometrySink:: AddBezier</span><span class="sxs-lookup"><span data-stu-id="d41c3-104">ID2D1GeometrySink::AddBezier methods</span></span>

<span data-ttu-id="d41c3-105">Crea una curva di Bezier cubica tra il punto corrente e il punto finale specificato e la aggiunge al sink di geometria.</span><span class="sxs-lookup"><span data-stu-id="d41c3-105">Creates a cubic Bezier curve between the current point and the specified end point and adds it to the geometry sink.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d41c3-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="d41c3-106">Overload list</span></span>



| <span data-ttu-id="d41c3-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="d41c3-107">Method</span></span>                                                                                            | <span data-ttu-id="d41c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d41c3-108">Description</span></span>                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d41c3-109">[**AddBezier ( \_ segmento Bezier D2D1 \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span><span class="sxs-lookup"><span data-stu-id="d41c3-109">[**AddBezier(D2D1\_BEZIER\_SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span></span>  | <span data-ttu-id="d41c3-110">Crea una curva di Bézier cubica tra il punto corrente e il punto finale specificato.</span><span class="sxs-lookup"><span data-stu-id="d41c3-110">Creates a cubic Bezier curve between the current point and the specified end point.</span></span><br/> |
| <span data-ttu-id="d41c3-111">[**AddBezier ( \_ segmento Bezier \_ d2d1 \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span><span class="sxs-lookup"><span data-stu-id="d41c3-111">[**AddBezier(D2D1\_BEZIER\_SEGMENT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span></span> | <span data-ttu-id="d41c3-112">Crea una curva di Bezier cubica tra il punto corrente e l'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="d41c3-112">Creates a cubic Bezier curve between the current point and the specified endpoint.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="d41c3-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="d41c3-113">Examples</span></span>

<span data-ttu-id="d41c3-114">Nell'esempio seguente viene creato un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), viene recuperato un sink e utilizzato per definire una forma di clessidra.</span><span class="sxs-lookup"><span data-stu-id="d41c3-114">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span> <span data-ttu-id="d41c3-115">Per l'esempio completo, vedere [How to disegnare and Fill an Complex Shape](how-to-draw-and-fill-a-complex-shape.md).</span><span class="sxs-lookup"><span data-stu-id="d41c3-115">For the complete example, see [How to Draw and Fill a Complex Shape](how-to-draw-and-fill-a-complex-shape.md).</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="d41c3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d41c3-116">Requirements</span></span>



| <span data-ttu-id="d41c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d41c3-117">Requirement</span></span> | <span data-ttu-id="d41c3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d41c3-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d41c3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d41c3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d41c3-120"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-120"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="d41c3-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d41c3-121">Library</span></span><br/> | <dl> <span data-ttu-id="d41c3-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d41c3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d41c3-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d41c3-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d41c3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d41c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41c3-126">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="d41c3-126">**ID2D1GeometrySink**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

<span data-ttu-id="d41c3-127">�</span><span class="sxs-lookup"><span data-stu-id="d41c3-127">�</span></span>

<span data-ttu-id="d41c3-128">�</span><span class="sxs-lookup"><span data-stu-id="d41c3-128">�</span></span>
