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
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget::P metodi ushLayer

Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                            | Descrizione                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer ( \_ parametri del livello D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |
| [**PushLayer ( \_ parametri del livello d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Aggiunge il livello specificato alla destinazione di rendering in modo che riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |



## <a name="remarks"></a>Commenti

Il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) consente a un chiamante di iniziare a reindirizzare il rendering a un livello. Tutte le operazioni di rendering sono valide in un livello. Il percorso del livello è influenzato dalla trasformazione globale impostata sulla destinazione di rendering.

Ogni **PushLayer** deve avere una chiamata [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) corrispondente. Se sono presenti più chiamate **PopLayer** rispetto alle chiamate di **PushLayer** , la destinazione di rendering viene inserita in uno stato di errore. Se [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato prima che vengano estratti tutti i livelli in attesa, la destinazione di rendering viene inserita in uno stato di errore e viene restituito un errore. Lo stato di errore può essere cancellato da una chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

Una determinata risorsa [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) può essere attiva solo una volta. In altre parole, non è possibile chiamare un metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e quindi seguire immediatamente un altro metodo **PushLayer** con la stessa risorsa livello. Al contrario, è necessario chiamare il secondo metodo **PushLayer** con risorse di livello differenti.

Per un esempio, vedere [come ritagliare un'area con livelli](how-to-clip-with-layers.md).

Questo metodo non restituisce un codice di errore se ha esito negativo. Per determinare se un'operazione di disegno (ad esempio **PushLayer**) non è riuscita, controllare il risultato restituito dai metodi [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato un livello per ritagliare una bitmap a una maschera geometrica. Per l'esempio completo, vedere [come ritagliare una maschera geometrica](how-to-clip-with-layers.md).


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1 \_ 1. h (include D2d1. h)</dt> </dl> |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Panoramica sui livelli](direct2d-layers-overview.md)
</dt> </dl>

�

�
