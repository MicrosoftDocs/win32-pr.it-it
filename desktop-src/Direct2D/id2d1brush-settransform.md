---
title: Metodi di trasformazione ID2D1Brush (D2d1 \_ 1. h)
description: Imposta la trasformazione applicata al pennello.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Metodi di trasformazione Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333281"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="aa030-104">Metodi ID2D1Brush:: setransform</span><span class="sxs-lookup"><span data-stu-id="aa030-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="aa030-105">Imposta la trasformazione applicata al pennello.</span><span class="sxs-lookup"><span data-stu-id="aa030-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="aa030-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="aa030-106">Overload list</span></span>



| <span data-ttu-id="aa030-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="aa030-107">Method</span></span>                                                                                       | <span data-ttu-id="aa030-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa030-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="aa030-109">[**Setransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="aa030-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="aa030-110">Imposta la trasformazione applicata al pennello.</span><span class="sxs-lookup"><span data-stu-id="aa030-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="aa030-111">[**Setransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="aa030-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="aa030-112">Imposta la trasformazione applicata al pennello.</span><span class="sxs-lookup"><span data-stu-id="aa030-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aa030-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa030-113">Remarks</span></span>

<span data-ttu-id="aa030-114">Quando si disegna con un pennello, dipinge nello spazio delle coordinate della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="aa030-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="aa030-115">I pennelli non si posizionano automaticamente per allinearsi all'oggetto da disegnare; per impostazione predefinita, iniziano a disegnare nell'origine (0,0) della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="aa030-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="aa030-116">È possibile "spostare" la sfumatura definita da un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) in un'area di destinazione impostando il punto iniziale e il punto finale.</span><span class="sxs-lookup"><span data-stu-id="aa030-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="aa030-117">Analogamente, è possibile spostare la sfumatura definita da un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando il relativo centro e i raggi.</span><span class="sxs-lookup"><span data-stu-id="aa030-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="aa030-118">Per allineare il contenuto di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) all'area da disegnare, è possibile usare il metodo **setransform** per convertire la bitmap nella posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="aa030-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="aa030-119">Questa trasformazione influisca solo sul pennello. non influisce sugli altri contenuti creati dalla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="aa030-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="aa030-120">Nelle illustrazioni seguenti viene illustrato l'effetto dell'utilizzo di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per riempire un rettangolo situato in (100, 100).</span><span class="sxs-lookup"><span data-stu-id="aa030-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="aa030-121">L'illustrazione nell'illustrazione a sinistra mostra il risultato del riempimento del rettangolo senza trasformare il pennello: la bitmap viene disegnata in corrispondenza dell'origine della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="aa030-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="aa030-122">Di conseguenza, nel rettangolo viene visualizzata solo una parte della bitmap.</span><span class="sxs-lookup"><span data-stu-id="aa030-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="aa030-123">L'illustrazione a destra mostra il risultato della trasformazione del [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) in modo che il relativo contenuto venga spostato 50 pixel a destra e 50 pixel in basso.</span><span class="sxs-lookup"><span data-stu-id="aa030-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="aa030-124">La bitmap riempie ora il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa030-124">The bitmap now fills the rectangle.</span></span>

![illustrazione di due quadrati, una disegnata con una bitmap senza un pennello trasformato e una disegnata con un pennello trasformato](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="aa030-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="aa030-126">Examples</span></span>

<span data-ttu-id="aa030-127">Gli esempi di codice seguenti illustrano come creare la trasformazione mostrata nel diagramma a destra nell'illustrazione precedente.</span><span class="sxs-lookup"><span data-stu-id="aa030-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="aa030-128">Per prima cosa applicare una traduzione al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), spostandolo il pennello 50 pixel lungo l'asse x e 50 pixel lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="aa030-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="aa030-129">Usare quindi **ID2D1BitmapBrush** per riempire il rettangolo con angolo superiore sinistro in (100, 100) e l'angolo inferiore destro in (200, 200).</span><span class="sxs-lookup"><span data-stu-id="aa030-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="aa030-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa030-130">Requirements</span></span>



| <span data-ttu-id="aa030-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa030-131">Requirement</span></span> | <span data-ttu-id="aa030-132">Valore</span><span class="sxs-lookup"><span data-stu-id="aa030-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa030-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa030-133">Header</span></span><br/>  | <dl> <span data-ttu-id="aa030-134"><dt>D2d1 \_ 1. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="aa030-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa030-135">Library</span></span><br/> | <dl> <span data-ttu-id="aa030-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="aa030-137">DLL</span><span class="sxs-lookup"><span data-stu-id="aa030-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa030-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa030-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="aa030-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa030-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa030-140">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="aa030-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="aa030-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="aa030-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="aa030-142">�</span><span class="sxs-lookup"><span data-stu-id="aa030-142">�</span></span>

<span data-ttu-id="aa030-143">�</span><span class="sxs-lookup"><span data-stu-id="aa030-143">�</span></span>
