---
title: Metodi ID2D1Factory CreateStrokeStyle
description: Crea un oggetto ID2D1StrokeStyle che descrive l'estremità iniziale, il motivo trattino e altre caratteristiche di un tratto.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Metodi CreateStrokeStyle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 7e0cd14de6197a13bf74e987de3a1d70a7d952b274025d0f8801c55aa80369ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342911"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a>Metodi ID2D1Factory::CreateStrokeStyle

Crea un [**oggetto ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, il motivo trattino e altre caratteristiche di un tratto.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                  | Descrizione                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateStrokeStyle(D2D1 \_ STROKE STYLE PROPERTIES \_ \_&, FLOAT , \* UINT, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))  | Crea un [**oggetto ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, il motivo trattino e altre caratteristiche di un tratto.<br/> |
| [**CreateStrokeStyle(D2D1 \_ STROKE STYLE PROPERTIES , FLOAT , \_ \_ \* \* UINT, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle)) | Crea un [**oggetto ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, il motivo trattino e altre caratteristiche di un tratto.<br/> |



## <a name="examples"></a>Esempio

L'esempio seguente crea un tratto che usa un motivo trattino personalizzato.


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



Nell'esempio seguente viene utilizzato lo stile del tratto quando si disegna una linea.


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

