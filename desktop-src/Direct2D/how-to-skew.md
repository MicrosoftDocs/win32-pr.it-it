---
title: Come inclinare un oggetto
description: Viene illustrato come inclinare un oggetto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872826"
---
# <a name="how-to-skew-an-object"></a><span data-ttu-id="53e02-103">Come inclinare un oggetto</span><span class="sxs-lookup"><span data-stu-id="53e02-103">How to Skew an Object</span></span>

<span data-ttu-id="53e02-104">Per inclinare (o inclinare) un oggetto significa distorcere un oggetto in base a un angolo specificato dall'asse x, dall'asse y o da entrambi.</span><span class="sxs-lookup"><span data-stu-id="53e02-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="53e02-105">Ad esempio, quando si inclina un quadrato, diventa un parallelogramma.</span><span class="sxs-lookup"><span data-stu-id="53e02-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="53e02-106">Il metodo [**Matrix3x2F:: asimmetria**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) accetta 3 parametri:</span><span class="sxs-lookup"><span data-stu-id="53e02-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="53e02-107">*AngleX*: angolo di inclinazione dell'asse x, misurato in gradi in senso antiorario rispetto all'asse y.</span><span class="sxs-lookup"><span data-stu-id="53e02-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="53e02-108">*AngleY*: angolo di inclinazione dell'asse y, misurato in gradi in senso orario dall'asse x.</span><span class="sxs-lookup"><span data-stu-id="53e02-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="53e02-109">*centerPoint*: punto in cui viene eseguita l'asimmetria.</span><span class="sxs-lookup"><span data-stu-id="53e02-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="53e02-110">Per stimare l'effetto di una trasformazione asimmetria, tenere presente che *AngleX* è l'angolo di inclinazione misurato in gradi in senso antiorario rispetto all'asse y.</span><span class="sxs-lookup"><span data-stu-id="53e02-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="53e02-111">Se, ad esempio, *AngleX* è impostato su 30, l'oggetto inclina 30 gradi in senso antiorario lungo l'asse y relativo al *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="53e02-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="53e02-112">Nella figura seguente viene mostrato un quadrato inclinato orizzontalmente di 30 gradi sull'angolo superiore sinistro del quadrato.</span><span class="sxs-lookup"><span data-stu-id="53e02-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y](images/skewx.png)

<span data-ttu-id="53e02-114">Analogamente, *AngleY* è un angolo di inclinazione misurato in gradi in senso orario dall'asse x.</span><span class="sxs-lookup"><span data-stu-id="53e02-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="53e02-115">Se ad esempio *AngleY* è impostato su 30, l'oggetto inclina 30 gradi in senso orario lungo l'asse x relativo a *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="53e02-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="53e02-116">Nella figura seguente viene mostrato un quadrato inclinato in verticale di 30 gradi sull'angolo superiore sinistro del quadrato.</span><span class="sxs-lookup"><span data-stu-id="53e02-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![illustrazione di un quadrato inclinato di 30 gradi in senso orario dall'asse x](images/skewy.png)

<span data-ttu-id="53e02-118">Se si impostano sia *AngleX* che *AngleY* su 30 gradi e il *centerPoint* nell'angolo superiore sinistro del quadrato, viene visualizzato il quadrato inclinato seguente (con linee solide).</span><span class="sxs-lookup"><span data-stu-id="53e02-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="53e02-119">Si noti che il quadrato inclinato è inclinato di 30 gradi in senso antiorario rispetto all'asse y e 30 gradi in senso orario dall'asse x.</span><span class="sxs-lookup"><span data-stu-id="53e02-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y e 30 gradi in senso orario dall'asse x](images/skewxy.png)

<span data-ttu-id="53e02-121">L'esempio di codice seguente inclina il quadrato di 45 gradi orizzontalmente rispetto all'angolo superiore sinistro del quadrato.</span><span class="sxs-lookup"><span data-stu-id="53e02-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="53e02-122">Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione asimmetria al quadrato, in cui il quadrato originale è un contorno tratteggiato e l'oggetto inclinato (parallelogramma) è un contorno a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="53e02-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="53e02-123">Si noti che l'angolo di inclinazione è di 45 gradi in senso antiorario rispetto all'asse y.</span><span class="sxs-lookup"><span data-stu-id="53e02-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![illustrazione di un quadrato inclinato di 45 gradi in senso antiorario dall'asse y](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="53e02-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53e02-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53e02-126">Cenni preliminari sulle trasformazioni Direct2D</span><span class="sxs-lookup"><span data-stu-id="53e02-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="53e02-127">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="53e02-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 