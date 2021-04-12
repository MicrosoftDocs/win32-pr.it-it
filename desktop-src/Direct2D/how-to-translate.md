---
title: Come tradurre un oggetto
description: Viene illustrato come tradurre un oggetto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338743"
---
# <a name="how-to-translate-an-object"></a><span data-ttu-id="fa54e-103">Come tradurre un oggetto</span><span class="sxs-lookup"><span data-stu-id="fa54e-103">How to Translate an Object</span></span>

<span data-ttu-id="fa54e-104">Per tradurre un oggetto 2D è necessario spostare l'oggetto lungo l'asse x, l'asse y o entrambi.</span><span class="sxs-lookup"><span data-stu-id="fa54e-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="fa54e-105">È possibile chiamare uno dei due metodi seguenti per creare una trasformazione di conversione.</span><span class="sxs-lookup"><span data-stu-id="fa54e-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="fa54e-106">[**Translation (D2D1 \_ size \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): accetta una coppia ordinata che definisce la distanza da tradurre lungo l'asse x e l'asse y.</span><span class="sxs-lookup"><span data-stu-id="fa54e-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="fa54e-107">[**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): accetta la distanza da tradurre lungo l'asse x e la distanza per traslare lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="fa54e-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="fa54e-108">Il codice seguente crea una matrice di trasformazione della traduzione che sposta le 20 unità quadrate a destra lungo l'asse x e le 10 unità verso il basso lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="fa54e-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="fa54e-109">Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione traduzione al quadrato, in cui il quadrato originale è un contorno tratteggiato e il quadrato tradotto è un contorno a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="fa54e-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![illustrazione di un quadrato spostato di 20 unità a destra lungo l'asse x e 10 unità verso il basso lungo l'asse y](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="fa54e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa54e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa54e-112">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="fa54e-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="fa54e-113">Cenni preliminari sulle trasformazioni Direct2D</span><span class="sxs-lookup"><span data-stu-id="fa54e-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 