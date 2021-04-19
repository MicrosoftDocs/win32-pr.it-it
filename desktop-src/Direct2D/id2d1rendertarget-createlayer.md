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
# <a name="id2d1rendertargetcreatelayer-methods"></a>Metodi ID2D1RenderTarget:: CreateLayer

Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                 | Descrizione                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLayer (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili. <br/>                                               |
| [**CreateLayer (D2D1 \_ size \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili. Il nuovo livello ha le dimensioni iniziali specificate. <br/> |
| [**CreateLayer (D2D1 \_ size \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Crea una risorsa livello che può essere utilizzata con questa destinazione di rendering e le relative destinazioni di rendering compatibili. Il nuovo livello ha le dimensioni iniziali specificate. <br/> |



## <a name="remarks"></a>Commenti

Il livello viene automaticamente ridimensionato, in base alle esigenze.

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
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui livelli](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
