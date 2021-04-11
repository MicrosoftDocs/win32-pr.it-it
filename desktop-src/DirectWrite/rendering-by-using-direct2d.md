---
title: Rendering tramite Direct2D
description: Direct2D fornisce metodi per il rendering di testo con formattazione descritta solo da un IDWriteTextFormat o un IDWriteTextLayout in una superficie Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047285"
---
# <a name="render-using-direct2d"></a><span data-ttu-id="dd0ea-103">Rendering tramite Direct2D</span><span class="sxs-lookup"><span data-stu-id="dd0ea-103">Render Using Direct2D</span></span>

<span data-ttu-id="dd0ea-104">Direct2D fornisce metodi per il rendering di testo con formattazione descritta solo da un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) in una superficie Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dd0ea-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="dd0ea-105">Rendering del testo descritto da IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="dd0ea-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="dd0ea-106">Per eseguire il rendering di una stringa usando un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per descrivere la formattazione per l'intera stringa, usare il metodo [**ID2D1RenderTarget::D Rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fornito da [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="dd0ea-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="dd0ea-107">Definire l'area per il layout del testo recuperando le dimensioni dell'area di rendering e creare un rettangolo [Direct2D](../direct2d/direct2d-portal.md) con le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="dd0ea-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="dd0ea-108">Usare il metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e l'oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per eseguire il rendering del testo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="dd0ea-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="dd0ea-109">Il metodo **ID2D1RenderTarget::D rawtext** accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd0ea-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="dd0ea-110">Stringa di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="dd0ea-110">A string to render.</span></span>
    -   <span data-ttu-id="dd0ea-111">Puntatore a un'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="dd0ea-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="dd0ea-112">Rettangolo di layout [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dd0ea-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="dd0ea-113">Puntatore a un'interfaccia che espone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="dd0ea-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="dd0ea-114">Rendering di un oggetto layout IDWriteText</span><span class="sxs-lookup"><span data-stu-id="dd0ea-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="dd0ea-115">Per tracciare il testo con le impostazioni di layout del testo specificate dall'oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modificare il codice nel metodo multiformattedtext::D rawtext per usare [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="dd0ea-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="dd0ea-116">Delcare una variabile [**d2d1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) e la imposta sul punto in alto a sinistra della finestra.</span><span class="sxs-lookup"><span data-stu-id="dd0ea-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="dd0ea-117">Disegnare il testo sullo schermo chiamando il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) della destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) e passando il puntatore [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="dd0ea-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 