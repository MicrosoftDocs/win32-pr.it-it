---
title: Come applicare più trasformazioni a un oggetto
description: Viene illustrato come applicare più trasformazioni a un oggetto.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708362"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="ff4f7-103">Come applicare più trasformazioni a un oggetto</span><span class="sxs-lookup"><span data-stu-id="ff4f7-103">How to Apply Multiple Transforms to an Object</span></span>

<span data-ttu-id="ff4f7-104">Per eseguire più trasformazioni su un oggetto significa combinare più trasformazioni in una sola.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-104">To perform multiple transforms on an object means to combine several transforms into one.</span></span> <span data-ttu-id="ff4f7-105">Ovvero, prendendo l'output da ogni matrice di trasformazione e utilizzandolo come input per il successivo, ottenendo così gli effetti cumulativi di tutte le trasformazioni di matrice.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-105">That is, taking the output from each transformation matrix and using it as the input for the next, thereby getting the cumulative effects of all the matrix transformations.</span></span>

<span data-ttu-id="ff4f7-106">Si supponga che due matrici di trasformazione, rotazione e traslazione, vengano moltiplicate insieme.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-106">Suppose two transformation matrices, rotation and translation, are multiplied together.</span></span> <span data-ttu-id="ff4f7-107">Il risultato è una nuova matrice che esegue le funzioni di rotazione e traslazione.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-107">The result is a new matrix that performs the functions of both rotation and translation.</span></span> <span data-ttu-id="ff4f7-108">Poiché la moltiplicazione di matrici non è commutativa, una trasformazione di rotazione moltiplicata per una trasformazione di conversione è diversa dalla trasformazione di conversione moltiplicata per la trasformazione di rotazione.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-108">Because matrix multiplication is not commutative, a rotation transformation multiplied by a translation transformation is different from the translation transformation multiplied by the rotation transformation.</span></span>

<span data-ttu-id="ff4f7-109">Gli esempi di codice seguenti illustrano come applicare la rotazione seguita dalla conversione e quindi dalla conversione seguita dalla rotazione.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-109">The following code examples show how to apply rotation followed by translation, and then translation followed by rotation.</span></span> <span data-ttu-id="ff4f7-110">Si noti che i risultati del rendering sono diversi.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-110">Notice that the rendering results are different.</span></span>


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="ff4f7-111">Il codice produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-111">The code produces the output shown in the following illustration.</span></span>

![illustrazione di un rettangolo che è stato convertito e quindi ruotato e un rettangolo che è stato ruotato e quindi convertito](images/multipletransforms.png)

## <a name="related-topics"></a><span data-ttu-id="ff4f7-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff4f7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff4f7-114">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="ff4f7-114">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="ff4f7-115">Cenni preliminari sulle trasformazioni Direct2D</span><span class="sxs-lookup"><span data-stu-id="ff4f7-115">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 




