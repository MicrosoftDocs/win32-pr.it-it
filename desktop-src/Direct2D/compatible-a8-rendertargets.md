---
title: Panoramica delle destinazioni di rendering a8 compatibili
description: Descrive le nozioni di base delle destinazioni di rendering a8 compatibili e fornisce esempi che illustrano come usarle.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103963623"
---
# <a name="compatible-a8-render-targets-overview"></a>Panoramica delle destinazioni di rendering a8 compatibili

Questo argomento descrive le nozioni di base di una destinazione di rendering a8 compatibile e fornisce esempi su come usarla.

Una destinazione di rendering a8 compatibile è una destinazione di rendering compatibile ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) che usa un formato pixel A8 ( \_ formato DXGI \_ a8 \_ UNORM). È possibile usare una destinazione di rendering a8 compatibile per migliorare le prestazioni dell'applicazione e fornire transizioni più fluide durante l'animazione del testo. Una destinazione di rendering a8 compatibile è particolarmente utile quando si tenta di migliorare gli elementi seguenti:

-   Frequenza dei fotogrammi dell'applicazione che esegue il rendering del testo o della geometria con aliasing che include solo animazioni semplici, ad esempio le modifiche alla conversione, alla rotazione, alla scala o al colore.

-   Continuità visiva dell'applicazione che estende e DIMINSHES il testo durante un'animazione.

Per creare una destinazione di rendering a8 compatibile, usare il metodo [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) insieme al formato DXGI \_ formato \_ a8 \_ UNORM pixel e specificare una destinazione di rendering compatibile restituita. Per ulteriori informazioni sui formati pixel, vedere [formati di pixel supportati e modalità Alpha](./supported-pixel-formats-and-alpha-modes.md).

Ad esempio, per animare in modo efficiente il testo illustrato nello screenshot seguente, usare una destinazione di rendering a8 compatibile per memorizzare nella cache il testo come maschera di opacità. Applicare quindi le trasformazioni alla maschera di opacità per ottenere risultati di rendering veloci.

![screenshot del testo a cui aggiungere un'animazione](images/a8rendertarget.png)

A tal fine, osservare il codice indicato di seguito. Viene creata una destinazione di rendering a8 compatibile, viene recuperata la bitmap, quindi viene eseguito il rendering della bitmap utilizzando [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a>Argomenti correlati

[Riferimento Direct2D](reference.md)