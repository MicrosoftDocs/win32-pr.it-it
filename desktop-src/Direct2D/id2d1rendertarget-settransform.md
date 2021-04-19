---
title: Metodi di trasformazione ID2D1RenderTarget
description: Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente. Tutte le operazioni di disegno successive si verificano nello spazio trasformato.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Metodi di trasformazione Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333504"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="d6b6a-105">Metodi ID2D1RenderTarget:: setransform</span><span class="sxs-lookup"><span data-stu-id="d6b6a-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="d6b6a-106">Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="d6b6a-107">Tutte le operazioni di disegno successive si verificano nello spazio trasformato.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d6b6a-108">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="d6b6a-108">Overload list</span></span>



| <span data-ttu-id="d6b6a-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="d6b6a-109">Method</span></span>                                                                                              | <span data-ttu-id="d6b6a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6b6a-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b6a-111">[**Setransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="d6b6a-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="d6b6a-112">Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="d6b6a-113">Tutte le operazioni di disegno successive si verificano nello spazio trasformato.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="d6b6a-114">[**Setransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="d6b6a-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="d6b6a-115">Applica la trasformazione specificata alla destinazione di rendering, sostituendo la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="d6b6a-116">Tutte le operazioni di disegno successive si verificano nello spazio trasformato.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="d6b6a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6b6a-117">Examples</span></span>

<span data-ttu-id="d6b6a-118">Nell'esempio seguente viene utilizzato il metodo **setransform** per applicare una rotazione alla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d6b6a-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="d6b6a-119">Per l'esempio completo, vedere [come ruotare un oggetto](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="d6b6a-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="d6b6a-120">Per altri esempi che illustrano come trasformare una destinazione di rendering, vedere [come ridimensionare un oggetto](how-to-scale.md), [come inclinare un oggetto](how-to-skew.md)e [come tradurre un oggetto](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="d6b6a-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b6a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6b6a-121">Requirements</span></span>



| <span data-ttu-id="d6b6a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6b6a-122">Requirement</span></span> | <span data-ttu-id="d6b6a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d6b6a-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b6a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6b6a-124">Library</span></span><br/> | <dl> <span data-ttu-id="d6b6a-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6b6a-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6b6a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d6b6a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6b6a-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6b6a-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b6a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6b6a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b6a-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="d6b6a-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="d6b6a-130">Cenni preliminari sulle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="d6b6a-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="d6b6a-131">Come ruotare un oggetto</span><span class="sxs-lookup"><span data-stu-id="d6b6a-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="d6b6a-132">Come ridimensionare un oggetto</span><span class="sxs-lookup"><span data-stu-id="d6b6a-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="d6b6a-133">Come inclinare un oggetto</span><span class="sxs-lookup"><span data-stu-id="d6b6a-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="d6b6a-134">Come tradurre un oggetto</span><span class="sxs-lookup"><span data-stu-id="d6b6a-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="d6b6a-135">Come applicare più trasformazioni a un oggetto</span><span class="sxs-lookup"><span data-stu-id="d6b6a-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

