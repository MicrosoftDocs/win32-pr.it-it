---
title: Come ruotare un oggetto
description: Viene illustrato come ruotare un oggetto.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963280"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="2736c-103">Come ruotare un oggetto</span><span class="sxs-lookup"><span data-stu-id="2736c-103">How to Rotate an Object</span></span>

<span data-ttu-id="2736c-104">In questo argomento viene descritto come ruotare un oggetto relativo a un punto specificato.</span><span class="sxs-lookup"><span data-stu-id="2736c-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="2736c-105">Per ruotare un oggetto, chiamare il metodo [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) .</span><span class="sxs-lookup"><span data-stu-id="2736c-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="2736c-106">Questo metodo accetta due parametri, l'angolo e il punto centrale specificati.</span><span class="sxs-lookup"><span data-stu-id="2736c-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="2736c-107">L'angolo è un angolo di rotazione in senso orario in gradi e il punto centrale è il punto in cui l'oggetto ruota.</span><span class="sxs-lookup"><span data-stu-id="2736c-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="2736c-108">Il punto centrale è espresso nel sistema di coordinate dell'oggetto trasformato.</span><span class="sxs-lookup"><span data-stu-id="2736c-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="2736c-109">Il codice seguente, ad esempio, ruota un quadrato di 45 gradi in senso orario sul centro del quadrato.</span><span class="sxs-lookup"><span data-stu-id="2736c-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="2736c-110">Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione di rotazione precedente al quadrato.</span><span class="sxs-lookup"><span data-stu-id="2736c-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="2736c-111">Il quadrato originale è un contorno tratteggiato e il quadrato ruotato è un contorno a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="2736c-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![illustrazione di un quadrato ruotato di 45 gradi in senso orario rispetto al centro del quadrato originale](images/rotate-ovw.png)

<span data-ttu-id="2736c-113">Nella figura seguente viene illustrato l'effetto della rotazione in base allo stesso angolo di un punto centrale diverso.</span><span class="sxs-lookup"><span data-stu-id="2736c-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="2736c-114">Si noti che gli oggetti ruotati si trovano in posizioni diverse rispetto all'originale.</span><span class="sxs-lookup"><span data-stu-id="2736c-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="2736c-115">Il quadrato delineato a sinistra è il risultato della rotazione intorno al centro del quadrato originale e il quadrato con l'allineamento a destra è il risultato della rotazione sull'angolo superiore sinistro del quadrato originale.</span><span class="sxs-lookup"><span data-stu-id="2736c-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![illustrazione di un quadrato ruotato di 45 gradi in senso orario su un punto centrale diverso](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="2736c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2736c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2736c-118">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="2736c-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="2736c-119">Cenni preliminari sulle trasformazioni Direct2D</span><span class="sxs-lookup"><span data-stu-id="2736c-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 