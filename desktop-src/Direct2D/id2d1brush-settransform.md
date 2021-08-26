---
title: Metodi Id2D1Brush SetTransform (D2d1 \_ 1.h)
description: Imposta la trasformazione applicata al pennello.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Metodi SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a5a30d4051303667402fdd1143f5a813d7515223c8093a5913294e6dd1722273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918037"
---
# <a name="id2d1brushsettransform-methods"></a>Metodi ID2D1Brush::SetTransform

Imposta la trasformazione applicata al pennello.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                       | Descrizione                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Imposta la trasformazione applicata al pennello.<br/> |
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Imposta la trasformazione applicata al pennello.<br/> |



## <a name="remarks"></a>Commenti

Quando si disegna con un pennello, viene dipinta nello spazio delle coordinate della destinazione di rendering. I pennelli non si posizionano automaticamente per allinearsi all'oggetto di disegno; Per impostazione predefinita, iniziano a disegnare all'origine (0, 0) della destinazione di rendering.

È possibile "spostare" la sfumatura definita da [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) su un'area di destinazione impostandone il punto iniziale e il punto finale. Analogamente, è possibile spostare la sfumatura definita da [**un oggetto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) modificandone il centro e i raggi.

Per allineare il contenuto di [**un oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) all'area disegnata, è possibile usare il **metodo SetTransform** per convertire la bitmap nella posizione desiderata. Questa trasformazione influisce solo sul pennello. non influisce su nessun altro contenuto disegnato dalla destinazione di rendering.

Le illustrazioni seguenti illustrano l'effetto dell'uso di [**un oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per riempire un rettangolo posizionato in corrispondenza di (100, 100). L'illustrazione a sinistra mostra il risultato del riempimento del rettangolo senza trasformare il pennello: la bitmap viene disegnata all'origine della destinazione di rendering. Di conseguenza, nel rettangolo viene visualizzata solo una parte della bitmap.

L'illustrazione a destra mostra il risultato della trasformazione di [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) in modo che il contenuto sia spostato di 50 pixel a destra e di 50 pixel verso il basso. La bitmap riempie ora il rettangolo.

![illustrazione di due quadrati, uno dipinge con una bitmap senza pennello trasformato e uno con un pennello trasformato](images/brushes-ovw-transform.png)

## <a name="examples"></a>Esempio

Gli esempi di codice seguenti illustrano come creare la trasformazione illustrata nel diagramma di destra nella figura precedente. Applicare prima una traslazione all'oggetto [**ID2D1BitmapBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)spostando il pennello di 50 pixel verso destra lungo l'asse x e 50 pixel verso il basso lungo l'asse y. Usare quindi **ID2D1BitmapBrush** per riempire il rettangolo con l'angolo superiore sinistro (100, 100) e l'angolo inferiore destro in corrispondenza di (200, 200).


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
| Intestazione<br/>  | <dl> <dt>D2d1 \_ 1.h (includere D2d1.h)</dt> </dl> |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
