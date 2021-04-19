---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Rappresenta una matrice 3 per 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301272"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="aca53-104">\_Matrice d2d1 \_ 3x2 \_ F</span><span class="sxs-lookup"><span data-stu-id="aca53-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="aca53-105">Rappresenta una matrice 3 per 2.</span><span class="sxs-lookup"><span data-stu-id="aca53-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="aca53-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="aca53-106">Remarks</span></span>

<span data-ttu-id="aca53-107">**D2d1 \_ MATRIX \_ 3x2** è un nuovo nome per la struttura [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="aca53-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="aca53-108">Per un elenco dei campi forniti dalla matrice, vedere [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="aca53-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="aca53-109">Per semplificare le operazioni comuni della matrice, Direct2D fornisce la classe [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , derivata dalla struttura [**d2d1 \_ Matrix \_ 3x2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="aca53-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="aca53-110">La classe **Matrix3x2F** fornisce un set di metodi helper per l'esecuzione di attività comuni, ad esempio la creazione di una matrice di traslazione o di inclinazione.</span><span class="sxs-lookup"><span data-stu-id="aca53-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="aca53-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="aca53-111">Examples</span></span>

<span data-ttu-id="aca53-112">Nell'esempio seguente viene usato il metodo [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) per creare una matrice di rotazione che ruota un quadrato di 45 gradi in senso orario sul centro del quadrato e passa la matrice al metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) della destinazione di rendering (*m \_ pRenderTarget*).</span><span class="sxs-lookup"><span data-stu-id="aca53-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="aca53-113">Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione di rotazione precedente al quadrato.</span><span class="sxs-lookup"><span data-stu-id="aca53-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="aca53-114">Il quadrato originale è un contorno tratteggiato e il quadrato ruotato è un contorno a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="aca53-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![illustrazione di un quadrato ruotato di 45 gradi in senso orario rispetto al centro del quadrato originale](images/rotate-ovw.png)


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



<span data-ttu-id="aca53-116">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="aca53-116">Code has been omitted from this example.</span></span> <span data-ttu-id="aca53-117">Per ulteriori informazioni sulle trasformazioni, vedere [Cenni preliminari sulle trasformazioni](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aca53-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aca53-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca53-118">Requirements</span></span>



| <span data-ttu-id="aca53-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca53-119">Requirement</span></span> | <span data-ttu-id="aca53-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aca53-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca53-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca53-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aca53-122">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aca53-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="aca53-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca53-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aca53-124">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aca53-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="aca53-125">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca53-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="aca53-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="aca53-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="aca53-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aca53-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca53-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca53-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="aca53-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca53-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca53-130">**D2D1:: Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="aca53-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="aca53-131">Cenni preliminari sulle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="aca53-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="aca53-132">Come ruotare un oggetto</span><span class="sxs-lookup"><span data-stu-id="aca53-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="aca53-133">Come ridimensionare un oggetto</span><span class="sxs-lookup"><span data-stu-id="aca53-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="aca53-134">Come inclinare un oggetto</span><span class="sxs-lookup"><span data-stu-id="aca53-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="aca53-135">Come tradurre un oggetto</span><span class="sxs-lookup"><span data-stu-id="aca53-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="aca53-136">**\_Matrice D2D \_ 3x2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="aca53-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

