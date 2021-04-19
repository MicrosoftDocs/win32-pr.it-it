---
title: Metodi di trasformazione ID2D1Brush (D2d1 \_ 1. h)
description: Imposta la trasformazione applicata al pennello.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Metodi di trasformazione Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333281"
---
# <a name="id2d1brushsettransform-methods"></a>Metodi ID2D1Brush:: setransform

Imposta la trasformazione applicata al pennello.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                       | Descrizione                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**Setransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Imposta la trasformazione applicata al pennello.<br/> |
| [**Setransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Imposta la trasformazione applicata al pennello.<br/> |



## <a name="remarks"></a>Commenti

Quando si disegna con un pennello, dipinge nello spazio delle coordinate della destinazione di rendering. I pennelli non si posizionano automaticamente per allinearsi all'oggetto da disegnare; per impostazione predefinita, iniziano a disegnare nell'origine (0,0) della destinazione di rendering.

È possibile "spostare" la sfumatura definita da un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) in un'area di destinazione impostando il punto iniziale e il punto finale. Analogamente, è possibile spostare la sfumatura definita da un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando il relativo centro e i raggi.

Per allineare il contenuto di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) all'area da disegnare, è possibile usare il metodo **setransform** per convertire la bitmap nella posizione desiderata. Questa trasformazione influisca solo sul pennello. non influisce sugli altri contenuti creati dalla destinazione di rendering.

Nelle illustrazioni seguenti viene illustrato l'effetto dell'utilizzo di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per riempire un rettangolo situato in (100, 100). L'illustrazione nell'illustrazione a sinistra mostra il risultato del riempimento del rettangolo senza trasformare il pennello: la bitmap viene disegnata in corrispondenza dell'origine della destinazione di rendering. Di conseguenza, nel rettangolo viene visualizzata solo una parte della bitmap.

L'illustrazione a destra mostra il risultato della trasformazione del [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) in modo che il relativo contenuto venga spostato 50 pixel a destra e 50 pixel in basso. La bitmap riempie ora il rettangolo.

![illustrazione di due quadrati, una disegnata con una bitmap senza un pennello trasformato e una disegnata con un pennello trasformato](images/brushes-ovw-transform.png)

## <a name="examples"></a>Esempio

Gli esempi di codice seguenti illustrano come creare la trasformazione mostrata nel diagramma a destra nell'illustrazione precedente. Per prima cosa applicare una traduzione al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), spostandolo il pennello 50 pixel lungo l'asse x e 50 pixel lungo l'asse y. Usare quindi **ID2D1BitmapBrush** per riempire il rettangolo con angolo superiore sinistro in (100, 100) e l'angolo inferiore destro in (200, 200).


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1 \_ 1. h (include D2d1. h)</dt> </dl> |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
