---
title: Eseguire il rendering con Direct2D
description: Direct2D fornisce metodi per il rendering di testo con formattazione descritta solo da idWriteTextFormat o IDWriteTextLayout in una superficie Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad297a8fdf2078c966989baf5e81c69cf515427340f8de8d073035fcf98f434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048481"
---
# <a name="render-using-direct2d"></a>Eseguire il rendering con Direct2D

Direct2D fornisce metodi per il rendering di testo con formattazione descritta solo da [**idWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) in una superficie Direct2D.

## <a name="rendering-text-described-by-idwritetextformat"></a>Rendering del testo descritto da IDWriteTextFormat

Per eseguire il rendering di una stringa usando un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per descrivere la formattazione per l'intera stringa, usare il metodo [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fornito da [Direct2D.](../direct2d/direct2d-portal.md)

1.  Definire l'area per il layout di testo recuperando le dimensioni dell'area di rendering e creare un rettangolo [Direct2D](../direct2d/direct2d-portal.md) con le stesse dimensioni.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Usare il [**metodo ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e l'oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per eseguire il rendering del testo sullo schermo. Il **metodo ID2D1RenderTarget::D rawText** accetta i parametri seguenti:
    -   Stringa di cui eseguire il rendering.
    -   Puntatore a [**un'interfaccia IDWriteTextFormat.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
    -   Rettangolo di layout [Direct2D.](../direct2d/direct2d-portal.md)
    -   Puntatore a un'interfaccia che espone [**ID2D1Brush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Rendering di un oggetto layout IDWriteText

Per disegnare il testo con le impostazioni di layout del testo specificate dall'oggetto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) modificare il codice nel metodo MultiformattedText::D rawText per usare [**IDWriteTextLayout::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Eseguire il delcare [**una variabile D2D1 \_ POINT \_ 2F**](../direct2d/d2d1-point-2f.md) e impostarla sul punto superiore sinistro della finestra.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Disegnare il testo sullo schermo chiamando il metodo [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) della destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) e passando il puntatore [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 