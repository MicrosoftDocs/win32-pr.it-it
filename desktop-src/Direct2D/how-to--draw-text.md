---
title: Come disegnare testo
description: Illustra come eseguire il rendering del testo con Direct2D.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd9b98417d81cf1cd3222faf771f56cb009f9a327c44f0f0962feb9bf41cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259981"
---
# <a name="how-to-draw-text"></a>Come disegnare testo

Per disegnare testo con Direct2D, usare il [**metodo ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) per il testo con un unico formato. In caso contrario, usare il [**metodo ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) per più formati, funzionalità OpenType avanzate o hit testing. Questi metodi usano l'API DirectWrite per fornire una visualizzazione di testo di alta qualità.

## <a name="the-drawtext-method"></a>Metodo DrawText

Per disegnare testo con un solo formato, usare il [**metodo DrawText.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) Per usare questo metodo, usare prima [**idWriteFactory per**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) creare un'istanza [**IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)

Il codice seguente crea un [**oggetto IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e lo archivia nella *variabile m \_ pTextFormat.*


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
        
        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }

    return hr;
}
```



Poiché [**gli oggetti IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) sono risorse indipendenti dal [dispositivo,](resources-and-resource-domains.md)è possibile migliorare le prestazioni di un'applicazione creandole una sola volta, invece di crearle di nuovo ogni volta che viene eseguito il rendering di un frame.

Dopo aver creato l'oggetto formato testo, è possibile usarlo con una destinazione di rendering. Il codice seguente disegna il testo usando il [**metodo DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) della destinazione di rendering *(variabile \_ m pRenderTarget).*


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a>Metodo DrawTextLayout

Il [**metodo DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) esegue il rendering di un [**oggetto IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Usare questo metodo per applicare più formati a un blocco di testo,ad esempio per sottolineare una parte di testo, per usare funzionalità OpenType avanzate o per eseguire il supporto dell'hit testing.

Il [**metodo DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) offre anche vantaggi in termini di prestazioni per disegnare ripetutamente lo stesso testo. [**L'oggetto IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) misura e dispone il testo al momento della creazione. Se si crea un oggetto **IDWriteTextLayout** una sola volta e lo si riutilizza ogni volta che è necessario ridisegnare il testo, le prestazioni migliorano perché il sistema non deve misurare e disporre nuovamente il testo.

Prima di poter usare il [**metodo DrawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) è necessario usare [**idWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) per creare oggetti [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [**e IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Dopo aver creato questi oggetti, chiamare il **metodo DrawTextLayout.**

Per altre informazioni ed esempi, vedere La panoramica [di formattazione e layout del](/windows/desktop/DirectWrite/text-formatting-and-layout) testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Drawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Formattazione e layout del testo](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
