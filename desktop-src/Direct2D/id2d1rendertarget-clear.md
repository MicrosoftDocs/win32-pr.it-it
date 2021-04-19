---
title: Metodi Clear di ID2D1RenderTarget
description: Cancella l'area di disegno dal colore specificato.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Metodi Clear Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330058"
---
# <a name="id2d1rendertargetclear-methods"></a><span data-ttu-id="3d886-104">Metodi ID2D1RenderTarget:: Clear</span><span class="sxs-lookup"><span data-stu-id="3d886-104">ID2D1RenderTarget::Clear methods</span></span>

<span data-ttu-id="3d886-105">Cancella l'area di disegno dal colore specificato.</span><span class="sxs-lookup"><span data-stu-id="3d886-105">Clears the drawing area to the specified color.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3d886-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="3d886-106">Overload list</span></span>



| <span data-ttu-id="3d886-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="3d886-107">Method</span></span>                                                                 | <span data-ttu-id="3d886-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d886-108">Description</span></span>                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="3d886-109">[**Cancella (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="3d886-109">[**Clear(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span></span> | <span data-ttu-id="3d886-110">Cancella l'area di disegno dal colore specificato.</span><span class="sxs-lookup"><span data-stu-id="3d886-110">Clears the drawing area to the specified color.</span></span> <br/> |
| <span data-ttu-id="3d886-111">[**Clear (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="3d886-111">[**Clear(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span></span>  | <span data-ttu-id="3d886-112">Cancella l'area di disegno dal colore specificato.</span><span class="sxs-lookup"><span data-stu-id="3d886-112">Clears the drawing area to the specified color.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="3d886-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d886-113">Remarks</span></span>

<span data-ttu-id="3d886-114">Direct2D interpreta *clearColor* come Alpha lineare (non premoltiplicato).</span><span class="sxs-lookup"><span data-stu-id="3d886-114">Direct2D interprets the *clearColor* as straight alpha (not premultiplied).</span></span> <span data-ttu-id="3d886-115">Se la modalità Alpha della destinazione di rendering [**è \_ d2d1 \_ modalità Alpha \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), il canale alfa di *clearColor* viene ignorato e sostituito con 1,0 f (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="3d886-115">If the render target's alpha mode is [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the alpha channel of *clearColor* is ignored and replaced with 1.0f (fully opaque).</span></span>

<span data-ttu-id="3d886-116">Se la destinazione di rendering ha un clip attivo (specificato da [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), il comando Clear viene applicato solo all'area all'interno dell'area di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="3d886-116">If the render target has an active clip (specified by [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), the clear command is only applied to the area within the clip region.</span></span>

## <a name="examples"></a><span data-ttu-id="3d886-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3d886-117">Examples</span></span>

<span data-ttu-id="3d886-118">Nell'esempio seguente viene usato il metodo **Clear** per creare uno sfondo bianco prima di eseguire il rendering di altro contenuto.</span><span class="sxs-lookup"><span data-stu-id="3d886-118">The following example uses the **Clear** method to create a white background before rendering other content.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3d886-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d886-119">Requirements</span></span>



| <span data-ttu-id="3d886-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d886-120">Requirement</span></span> | <span data-ttu-id="3d886-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3d886-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d886-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d886-122">Library</span></span><br/> | <dl> <span data-ttu-id="3d886-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d886-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d886-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3d886-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d886-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d886-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d886-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d886-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d886-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="3d886-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

