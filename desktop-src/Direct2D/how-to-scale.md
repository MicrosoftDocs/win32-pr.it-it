---
title: Come ridimensionare un oggetto
description: Viene illustrato come ridimensionare un oggetto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473830"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="94c73-103">Come ridimensionare un oggetto</span><span class="sxs-lookup"><span data-stu-id="94c73-103">How to Scale an Object</span></span>

<span data-ttu-id="94c73-104">In questo argomento viene descritto come ridimensionare un oggetto utilizzando la classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="94c73-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="94c73-105">Per ridimensionare un oggetto significa che l'oggetto è più grande o più piccolo.</span><span class="sxs-lookup"><span data-stu-id="94c73-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="94c73-106">È possibile chiamare uno dei due metodi seguenti per ridimensionare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="94c73-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="94c73-107">**Matrix3x2F:: scale (D2D1 \_ size \_ F SCALEFACTOR, d2d1 \_ Point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="94c73-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="94c73-108">**Matrix3x2F:: scale (float scaleX, float scaleY, D2D1 \_ Point \_ 2F Centerpoint)**</span><span class="sxs-lookup"><span data-stu-id="94c73-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="94c73-109">Il primo metodo Archivia *ScaleX* e *ScaleY* come coppia ordinata di valori a virgola mobile nella struttura [**d2d1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) .</span><span class="sxs-lookup"><span data-stu-id="94c73-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="94c73-110">Il secondo metodo definisce *ScaleX* e *ScaleY* come singoli parametri.</span><span class="sxs-lookup"><span data-stu-id="94c73-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="94c73-111">Indipendentemente dal metodo usato, è necessario specificare sia il metodo *ScaleX* che i fattori di *scalabilità* .</span><span class="sxs-lookup"><span data-stu-id="94c73-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="94c73-112">Il valore *ScaleX* è il fattore di scala nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="94c73-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="94c73-113">Ad esempio, un valore *ScaleX* di 1,5 estende l'oggetto a 150% lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="94c73-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="94c73-114">Analogamente, il valore di *scalabilità* è il fattore di scala nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="94c73-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="94c73-115">Ad esempio, un valore di *scalabilità* di 0,5 compatta l'altezza dell'oggetto del 50% lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="94c73-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="94c73-116">Per specificare un punto come centro dell'operazione di ridimensionamento, usare il parametro *Centerpoint* .</span><span class="sxs-lookup"><span data-stu-id="94c73-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="94c73-117">Per impostazione predefinita, un oggetto viene centrato sulla relativa origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="94c73-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="94c73-118">Nell'esempio di codice seguente viene creata una trasformazione di scala per aumentare le dimensioni di un quadrato al 130% delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="94c73-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="94c73-119">*Centerpoint* è impostato in modo da essere l'angolo superiore sinistro del quadrato originale.</span><span class="sxs-lookup"><span data-stu-id="94c73-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="94c73-120">Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione scala al quadrato.</span><span class="sxs-lookup"><span data-stu-id="94c73-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="94c73-121">Il quadrato originale è un contorno tratteggiato e il quadrato ridimensionato è un contorno a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="94c73-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![illustrazione del quadrato ridimensionato al 130% delle dimensioni originali](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="94c73-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94c73-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c73-124">Cenni preliminari sulle trasformazioni Direct2D</span><span class="sxs-lookup"><span data-stu-id="94c73-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="94c73-125">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="94c73-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 