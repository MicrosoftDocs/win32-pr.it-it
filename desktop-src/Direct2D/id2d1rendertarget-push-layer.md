---
title: Metodi ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato PopLayer.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Metodo PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333508"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="bc956-104">ID2D1RenderTarget::P metodi ushLayer</span><span class="sxs-lookup"><span data-stu-id="bc956-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="bc956-105">Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="bc956-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bc956-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="bc956-106">Overload list</span></span>



| <span data-ttu-id="bc956-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc956-107">Method</span></span>                                                                                                                            | <span data-ttu-id="bc956-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc956-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc956-109">[**PushLayer ( \_ parametri del livello D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="bc956-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="bc956-110">Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="bc956-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="bc956-111">[**PushLayer ( \_ parametri del livello d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="bc956-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="bc956-112">Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="bc956-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="bc956-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc956-113">Remarks</span></span>

<span data-ttu-id="bc956-114">Il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) consente a un chiamante di iniziare a reindirizzare il rendering a un livello.</span><span class="sxs-lookup"><span data-stu-id="bc956-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="bc956-115">Tutte le operazioni di rendering sono valide in un livello.</span><span class="sxs-lookup"><span data-stu-id="bc956-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="bc956-116">Il percorso del livello è influenzato dalla trasformazione globale impostata sulla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="bc956-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="bc956-117">Ogni **PushLayer** deve avere una chiamata [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bc956-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="bc956-118">Se sono presenti più chiamate **PopLayer** rispetto alle chiamate di **PushLayer** , la destinazione di rendering viene inserita in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="bc956-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="bc956-119">Se [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato prima che vengano estratti tutti i livelli in attesa, la destinazione di rendering viene inserita in uno stato di errore e viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="bc956-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="bc956-120">Lo stato di errore può essere cancellato da una chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="bc956-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="bc956-121">Una determinata risorsa [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) può essere attiva solo una volta.</span><span class="sxs-lookup"><span data-stu-id="bc956-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="bc956-122">In altre parole, non è possibile chiamare un metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e quindi seguire immediatamente un altro metodo **PushLayer** con la stessa risorsa livello.</span><span class="sxs-lookup"><span data-stu-id="bc956-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="bc956-123">Al contrario, è necessario chiamare il secondo metodo **PushLayer** con risorse di livello differenti.</span><span class="sxs-lookup"><span data-stu-id="bc956-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="bc956-124">Per un esempio, vedere [come ritagliare un'area con livelli](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="bc956-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="bc956-125">Questo metodo non restituisce un codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bc956-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="bc956-126">Per determinare se un'operazione di disegno (ad esempio **PushLayer**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="bc956-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="bc956-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc956-127">Examples</span></span>

<span data-ttu-id="bc956-128">Nell'esempio seguente viene usato un livello per ritagliare una bitmap a una maschera geometrica.</span><span class="sxs-lookup"><span data-stu-id="bc956-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="bc956-129">Per l'esempio completo, vedere [come ritagliare una maschera geometrica](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="bc956-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bc956-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc956-130">Requirements</span></span>



| <span data-ttu-id="bc956-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc956-131">Requirement</span></span> | <span data-ttu-id="bc956-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bc956-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc956-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc956-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bc956-134"><dt>D2d1 \_ 1. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc956-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="bc956-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc956-135">Library</span></span><br/> | <dl> <span data-ttu-id="bc956-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc956-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bc956-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bc956-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc956-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc956-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="bc956-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc956-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc956-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="bc956-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="bc956-141">Panoramica sui livelli</span><span class="sxs-lookup"><span data-stu-id="bc956-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="bc956-142">�</span><span class="sxs-lookup"><span data-stu-id="bc956-142">�</span></span>

<span data-ttu-id="bc956-143">�</span><span class="sxs-lookup"><span data-stu-id="bc956-143">�</span></span>
