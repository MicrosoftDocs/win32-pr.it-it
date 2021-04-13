---
title: Errore di scaricamento D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Una chiamata di scaricamento da una destinazione di rendering non è riuscita
keywords:
- Direct2D errore di scaricamento D1110
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399695"
---
# <a name="d1110-flush-failure"></a>D1110: errore di svuotamento

Una chiamata di scaricamento da una destinazione di rendering non è riuscita \[  \] . Tag \[ *tag1*, *Tag2* \] .

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*risorse*
</dt> <dd>

Indirizzo della destinazione di rendering.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Primo valore del tag. Per ulteriori informazioni, vedere i [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*Tag2*
</dt> <dd>

Il secondo valore del tag. Per ulteriori informazioni, vedere i [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> </dl> 

|             |         |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="examples"></a>Esempio

**Esempio 1:** Il codice seguente mostra che una chiamata di progetto è in uno stato non valido. Per evitare il messaggio di avviso, usare [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare \_ l' \_ antialiasing della modalità antialias d2d1 \_ prima di una chiamata a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





Questo esempio produce il seguente messaggio di debug:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Esempio 2:** Il codice seguente mostra che lo [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato dopo la chiamata a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



Questo esempio produce il seguente messaggio di debug:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Possibili cause

La chiamata di [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) può non riuscire per uno dei due motivi. Potrebbe non riuscire perché il metodo è stato chiamato al [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)di fuori della / [**chiamata EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) BeginDraw o potrebbe non riuscire a causa di un errore prodotto da una delle operazioni di destinazione di rendering elaborate dall'ultima chiamata di **scaricamento** o dalla chiamata a **EndDraw** . Per risolvere il problema, l'applicazione deve determinare la causa dell'errore e intraprendere l'azione appropriata.

## <a name="fixes"></a>Correzioni

Esistono molti motivi per cui una chiamata di [**scaricamento**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) potrebbe non riuscire. L'applicazione deve determinare la causa dell'errore e intraprendere l'azione appropriata.

 

 