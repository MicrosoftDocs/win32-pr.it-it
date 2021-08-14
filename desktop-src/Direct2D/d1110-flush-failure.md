---
title: Errore di scaricamento D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Una chiamata flush da una destinazione di rendering non è riuscita
keywords:
- Errore di scaricamento D1110 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12d6a990d3d65c1a711825e6d45720f3df977ca78efb16c1d39bb9b2251c53b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758151"
---
# <a name="d1110-flush-failure"></a>D1110: Errore di scaricamento

Una chiamata Flush da parte di una risorsa di destinazione di rendering non \[ *è riuscita.* \] Tag \[ *tag1,* *tag2* \] .

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Risorsa*
</dt> <dd>

Indirizzo della destinazione di rendering.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Primo valore del tag. Per [**altre informazioni, vedere SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Secondo valore del tag. Per [**altre informazioni, vedere SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="examples"></a>Esempio

**Esempio 1:** Il codice seguente mostra che una chiamata di disegno è in uno stato non valido. Per evitare il messaggio di avviso, usare [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare D2D1 \_ \_ ANTIALIAS MODE \_ ANTIALIASED prima di [**una chiamata a FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md)


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





In questo esempio viene generato il messaggio di debug seguente:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Esempio 2:** Il codice seguente mostra che [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato dopo la [**chiamata EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



In questo esempio viene generato il messaggio di debug seguente:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Possibili cause

La [**chiamata Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) può non riuscire per uno dei due motivi seguenti. Potrebbe non riuscire perché il metodo [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)è stato chiamato all'esterno della chiamata / [**BeginDraw EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oppure potrebbe non riuscire perché si è verificato un errore generato da una delle operazioni di destinazione di rendering elaborate dopo l'ultima chiamata **Flush** o **EndDraw.** Per risolvere il problema, l'applicazione deve determinare la causa dell'errore ed eseguire l'azione appropriata.

## <a name="fixes"></a>Correzioni

Esistono molti motivi per cui una [**chiamata Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) potrebbe non riuscire. L'applicazione deve determinare la causa dell'errore ed eseguire l'azione appropriata.

 

 