---
title: Metodi CreateTransformedGeometry di ID2D1Factory (D2d1. h)
description: Trasforma la geometria specificata e archivia il risultato come oggetto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Metodo CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325792"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="8a1fe-104">Metodi ID2D1Factory:: CreateTransformedGeometry</span><span class="sxs-lookup"><span data-stu-id="8a1fe-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="8a1fe-105">Trasforma la geometria specificata e archivia il risultato come oggetto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a1fe-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8a1fe-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="8a1fe-106">Overload list</span></span>



| <span data-ttu-id="8a1fe-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="8a1fe-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="8a1fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a1fe-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1fe-109">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a1fe-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="8a1fe-110">Trasforma la geometria specificata e archivia il risultato come oggetto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a1fe-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="8a1fe-111">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="8a1fe-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="8a1fe-112">Trasforma la geometria specificata e archivia il risultato come oggetto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a1fe-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8a1fe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a1fe-113">Remarks</span></span>

<span data-ttu-id="8a1fe-114">Analogamente ad altre risorse, una geometria trasformata eredita lo spazio delle risorse e i criteri di threading della factory che lo hanno creato.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="8a1fe-115">Questo oggetto non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-115">This object is immutable.</span></span>

<span data-ttu-id="8a1fe-116">Quando si accarezza una geometria trasformata con il metodo [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , la larghezza del tratto non è interessata dalla trasformazione applicata alla geometria.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="8a1fe-117">La larghezza del tratto è interessata solo dalla trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="8a1fe-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a1fe-118">Examples</span></span>

<span data-ttu-id="8a1fe-119">Nell'esempio seguente viene creato un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), quindi viene disegnato senza trasformarlo.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="8a1fe-120">Produce l'output mostrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-120">It produces the output shown in the following illustration.</span></span>

![illustrazione di un rettangolo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="8a1fe-122">Nell'esempio seguente viene usata la destinazione di rendering per ridimensionare la geometria in base a un fattore 3, quindi viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="8a1fe-123">Nella figura seguente viene illustrato il risultato della creazione del rettangolo senza la trasformazione e con la trasformazione; Si noti che il tratto è più spessa dopo la trasformazione, anche se lo spessore del tratto è 1.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con un tratto più spessa](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="8a1fe-125">Nell'esempio seguente viene usato il metodo **CreateTransformedGeometry** per ridimensionare la geometria per un fattore 3, quindi viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="8a1fe-126">Produce l'output mostrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="8a1fe-127">Si noti che, anche se il rettangolo è più grande, il relativo tratto non è aumentato.</span><span class="sxs-lookup"><span data-stu-id="8a1fe-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con lo stesso tratto](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="8a1fe-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a1fe-129">Requirements</span></span>



| <span data-ttu-id="8a1fe-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1fe-130">Requirement</span></span> | <span data-ttu-id="8a1fe-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1fe-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1fe-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a1fe-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8a1fe-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a1fe-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a1fe-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a1fe-134">Library</span></span><br/> | <dl> <span data-ttu-id="8a1fe-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a1fe-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a1fe-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a1fe-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a1fe-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a1fe-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1fe-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a1fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1fe-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="8a1fe-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
