---
title: Metodi CreateLayer di ID2D1RenderTarget (D2d1. h)
description: Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Metodo CreateLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6e7fe86f041a818db77c28ed9461d8c8fb48ad64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326084"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a><span data-ttu-id="ed1f8-104">Metodi ID2D1RenderTarget:: CreateLayer</span><span class="sxs-lookup"><span data-stu-id="ed1f8-104">ID2D1RenderTarget::CreateLayer methods</span></span>

<span data-ttu-id="ed1f8-105">Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-105">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ed1f8-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="ed1f8-106">Overload list</span></span>



| <span data-ttu-id="ed1f8-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="ed1f8-107">Method</span></span>                                                                                                                 | <span data-ttu-id="ed1f8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed1f8-108">Description</span></span>                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1f8-109">[**CreateLayer (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="ed1f8-109">[**CreateLayer(ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))</span></span>                                | <span data-ttu-id="ed1f8-110">Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-110">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <br/>                                               |
| <span data-ttu-id="ed1f8-111">[**CreateLayer (D2D1 \_ size \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="ed1f8-111">[**CreateLayer(D2D1\_SIZE\_F,ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span></span>       | <span data-ttu-id="ed1f8-112">Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-112">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <span data-ttu-id="ed1f8-113">Il nuovo livello ha le dimensioni iniziali specificate.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-113">The new layer has the specified initial size.</span></span> <br/> |
| <span data-ttu-id="ed1f8-114">[**CreateLayer (D2D1 \_ size \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="ed1f8-114">[**CreateLayer(D2D1\_SIZE\_F\*,ID2D1Layer\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))</span></span> | <span data-ttu-id="ed1f8-115">Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-115">Creates a layer resource that can be used with this render target and its compatible render targets.</span></span> <span data-ttu-id="ed1f8-116">Il nuovo livello ha le dimensioni iniziali specificate.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-116">The new layer has the specified initial size.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ed1f8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed1f8-117">Remarks</span></span>

<span data-ttu-id="ed1f8-118">Il livello viene automaticamente ridimensionato, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-118">The layer automatically resizes itself, as needed.</span></span>

## <a name="examples"></a><span data-ttu-id="ed1f8-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="ed1f8-119">Examples</span></span>

<span data-ttu-id="ed1f8-120">Nell'esempio seguente viene usato un livello per ritagliare una bitmap a una maschera geometrica.</span><span class="sxs-lookup"><span data-stu-id="ed1f8-120">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="ed1f8-121">Per l'esempio completo, vedere [come ritagliare una maschera geometrica](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="ed1f8-121">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ed1f8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed1f8-122">Requirements</span></span>



| <span data-ttu-id="ed1f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1f8-123">Requirement</span></span> | <span data-ttu-id="ed1f8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ed1f8-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1f8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed1f8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ed1f8-126"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1f8-126"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed1f8-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed1f8-127">Library</span></span><br/> | <dl> <span data-ttu-id="ed1f8-128"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed1f8-128"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ed1f8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ed1f8-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed1f8-130"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed1f8-130"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed1f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1f8-132">Panoramica sui livelli</span><span class="sxs-lookup"><span data-stu-id="ed1f8-132">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="ed1f8-133">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="ed1f8-133">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="ed1f8-134">�</span><span class="sxs-lookup"><span data-stu-id="ed1f8-134">�</span></span>

<span data-ttu-id="ed1f8-135">�</span><span class="sxs-lookup"><span data-stu-id="ed1f8-135">�</span></span>
