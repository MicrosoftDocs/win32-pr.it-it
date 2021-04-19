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
# <a name="id2d1rendertargetclear-methods"></a>Metodi ID2D1RenderTarget:: Clear

Cancella l'area di disegno dal colore specificato.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                 | Descrizione                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Cancella (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Cancella l'area di disegno dal colore specificato. <br/> |
| [**Clear (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Cancella l'area di disegno dal colore specificato. <br/> |



## <a name="remarks"></a>Commenti

Direct2D interpreta *clearColor* come Alpha lineare (non premoltiplicato). Se la modalità Alpha della destinazione di rendering [**è \_ d2d1 \_ modalità Alpha \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), il canale alfa di *clearColor* viene ignorato e sostituito con 1,0 f (completamente opaco).

Se la destinazione di rendering ha un clip attivo (specificato da [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), il comando Clear viene applicato solo all'area all'interno dell'area di ritaglio.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato il metodo **Clear** per creare uno sfondo bianco prima di eseguire il rendering di altro contenuto.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

