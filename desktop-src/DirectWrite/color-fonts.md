---
title: Caratteri a colori
description: Questo argomento descrive i tipi di carattere a colori, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5c0154e528ab8471d40f4771db5479ca9233320177386adbbd849162dbcd598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329526"
---
# <a name="color-fonts"></a>Caratteri a colori

Questo argomento descrive i tipi di carattere a colori, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.

Questo documento contiene le parti seguenti:

-   [Che cosa sono i tipi di carattere a colori?](#what-are-color-fonts)
-   [Perché usare i tipi di carattere a colori?](#why-use-color-fonts)
-   [Quali tipi di carattere a colori Windows supportati?](#what-kinds-of-color-fonts-does-windows-support)
-   [Uso dei tipi di carattere a colori](#using-color-fonts)
    -   [Uso dei tipi di carattere a colori in un'app XAML](#using-color-fonts-in-a-xaml-app)
    -   [Uso dei tipi di carattere a colori in Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Uso dei tipi di carattere a colori DirectWrite e Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Uso dei tipi di carattere a colori con Win2D](#using-color-fonts-with-win2d)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-color-fonts"></a>Che cosa sono i tipi di carattere a colori?

I tipi di carattere a colori, noti anche come tipi di carattere multicolore o tipi di carattere cromatici, sono una tecnologia dei tipi di carattere che consente ai progettisti di tipi di carattere di usare più colori all'interno di ogni glifo. I tipi di carattere a colori consentono scenari di testo multicolore in app e siti Web con meno codice e supporto del sistema operativo più affidabile rispetto alle tecniche ad hoc implementate sopra il sistema di rendering del testo.

I tipi di carattere con cui si ha maggiore familiarità non sono i tipi di carattere a colori. Questi tipi di carattere definiscono solo la forma dei glifi che contengono, con contorni vettoriali o bitmap monocromatiche. In fase di disegno, un renderer di testo riempie la forma del glifo usando un singolo colore (il colore del carattere ) specificato dall'app o dal documento di cui viene eseguito il rendering. I tipi di carattere a colori, d'altra parte, contengono informazioni sui colori oltre alle informazioni sulla forma. Alcuni approcci consentono ai progettisti di tipi di carattere di offrire più tavolozze dei colori, offrendo la flessibilità necessaria per il tipo di carattere dei colori.

L'esempio seguente mostra un glifo dal tipo di Segoe UI di colore Emoji. Il rendering del glifo viene eseguito in modalità monocromatica a sinistra e a colori a destra.

![Mostra i glifi affiancati, il glifo sinistro di cui viene eseguito il rendering in monocromatica, a destra nel tipo di carattere a colori Segoe U I Emoji.](images/color-font-cat.png)

I tipi di carattere a colori includono in genere informazioni di fallback per le piattaforme che non supportano i tipi di carattere a colori o per gli scenari in cui la funzionalità dei colori è stata disabilitata. In queste piattaforme, il rendering dei tipi di carattere a colori viene eseguito come normali tipi di carattere monocromatici.

## <a name="why-use-color-fonts"></a>Perché usare i tipi di carattere a colori?

In genere, progettisti e sviluppatori hanno usato un'ampia gamma di tecniche per ottenere testo multicolore. Ad esempio, i siti Web usano spesso immagini raster anziché testo per visualizzare intestazioni RTF. Questo approccio offre flessibilità, ma la grafica raster non è adatta a tutte le dimensioni di visualizzazione, né offre le stesse funzionalità di accessibilità del testo reale. Un'altra tecnica comune consiste nel sovrapporre più tipi di carattere monocromatici in colori diversi, ma ciò richiede in genere codice di layout aggiuntivo da gestire.

I tipi di carattere a colori offrono un modo per ottenere questi effetti visivi con tutta la semplicità e le funzionalità dei tipi di carattere normali. Il testo sottoposto a rendering con un tipo di carattere a colori è identico a quello di altro testo: può essere copiato e incollato, analizzato dagli strumenti di accessibilità e così via.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Quali tipi di carattere a colori Windows supportati?

La [specifica OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definisce diversi modi per incorporare informazioni sui colori in un tipo di carattere. A partire Windows 10'aggiornamento dell'anniversario, DirectWrite e Direct2D (e i framework Windows su cui si basano) supportano tutti questi approcci. Sono riepilogati nella tabella seguente:



| Tecnica                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / [Tabelle CPAL](/typography/opentype/spec/cpal) | Usa livelli di vettori colorati, le cui forme sono definite nello stesso modo dei contorni di glifi a colore singolo. **Nota:** Supportato a partire da Windows 8.1. <br/>                                                                                                                                                 |
| [Tabella SVG](/typography/opentype/spec/svg)                                                                 | Usa immagini vettoriali scritte nel formato di grafica vettoriale scalabile. **Nota:** A Windows 10'aggiornamento dell'anniversario, DirectWrite supporta un subset della specifica SVG completa. Non viene garantito il rendering di tutto il contenuto SVG in un tipo di carattere OpenType SVG. Per [altri dettagli, vedere Supporto SVG.](../direct2d/svg-support.md) <br/> |
| [ESERET](/typography/opentype/spec/cbdt) / [Tabelle CBLC](/typography/opentype/spec/cblc) | Usa immagini bitmap a colori incorporate.                                                                                                                                                                                                                                                                                |
| [Tabella sbix](/typography/opentype/spec/sbix)                                                               | Usa immagini bitmap a colori incorporate.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Uso dei tipi di carattere a colori

Dal punto di vista dell'utente, i tipi di carattere a colori sono solo tipi di carattere . Ad esempio, in genere possono essere installati e disinstallati dal sistema allo stesso modo dei tipi di carattere monocromatici e ne viene eseguito il rendering come testo normale e selezionabile.

Anche dal punto di vista dello sviluppatore, i tipi di carattere a colori vengono in genere usati allo stesso modo dei tipi di carattere monocromatici. Nei framework XAML e Microsoft Edge puoi impostare lo stile del testo con tipi di carattere a colori allo stesso modo dei normali tipi di carattere e per impostazione predefinita il rendering del testo verrà eseguito a colori. Tuttavia, se l'app chiama direttamente le API Direct2D (o API Win2D) per eseguire il rendering del testo, deve richiedere in modo esplicito il rendering del tipo di carattere a colori.

### <a name="using-color-fonts-in-a-xaml-app"></a>Uso dei tipi di carattere a colori in un'app XAML

Gli elementi di testo della piattaforma XAML (ad esempio [TextBlock,](/uwp/api/windows.ui.xaml.controls.textblock) [TextBox,](/uwp/api/windows.ui.xaml.controls.textbox) [RichEditBox,](/uwp/api/windows.ui.xaml.controls.richeditbox) [Glifi](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon)](/uwp/api/windows.ui.xaml.controls.fonticon)supportano i tipi di carattere a colori per impostazione predefinita. È sufficiente eseguire lo stile del testo con un tipo di carattere di colore e verrà eseguito il rendering di tutti i glifi a colori. L'esempio di codice seguente illustra un modo per creare uno stile per un controllo TextBlock con un tipo di carattere di colore in pacchetto con l'app. La stessa tecnica si applica ai tipi di carattere normali.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Se non si vuole mai che l'elemento di testo XAML eserne il rendering di testo multicolore, impostarne la proprietà [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) su false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Uso dei tipi di carattere a colori in Microsoft Edge

Il rendering dei tipi di carattere a colori viene eseguito per impostazione predefinita nei siti Web e nelle app Web in Microsoft Edge, incluso il [controllo WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML. È sufficiente usare HTML e CSS per eseguire lo stile del testo con un tipo di carattere di colore e verrà eseguito il rendering di tutti i glifi a colori.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Uso dei tipi di carattere a colori DirectWrite e Direct2D

L'app può usare i metodi di disegno del testo di livello superiore di Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) oppure può usare tecniche di livello inferiore per disegnare direttamente le esecuzioni di glifi. In entrambi i casi, l'app richiede modifiche al codice per gestire correttamente i glifi di colore. Se l'app usa le API **DrawText** e **DrawTextLayout** di Direct2D, si noti che per impostazione predefinita non viene eseguito il rendering dei glifi a colori. Ciò consente di evitare modifiche impreviste del comportamento nelle app per il rendering del testo progettate prima del supporto dei tipi di carattere a colori.

Per acconsentire esplicitamente al rendering del glifo a colori, passare il flag di opzioni [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) al metodo di disegno. L'esempio di codice seguente illustra come chiamare il metodo DrawText di Direct2D per eseguire il rendering di una stringa con un tipo di carattere a colori:


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Se l'app usa API di livello inferiore per gestire direttamente le esecuzioni dei glifi, continuerà a funzionare in presenza di tipi di carattere a colori, ma non sarà in grado di disegnare glifi di colore senza logica aggiuntiva.

Per gestire correttamente i glifi a colori, l'app deve:

1.  Passare le informazioni di esecuzione del glifo a [**TranslateColorGlyphRun,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)insieme a un parametro [**DWRITE \_ GLYPH \_ IMAGE \_ FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) che indica quali tipi di glifi di colore l'app è pronta a gestire. Se sono presenti glifi di colore (in base al tipo di carattere e ai formati IMAGE **\_ DWRITE GLYPH \_ \_** richiesti), DirectWrite suddividerà l'esecuzione del glifo primario in singole esecuzioni di glifi a colori accessibili tramite l'oggetto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) restituito nel passaggio 4.
2.  Controllare il valore HRESULT restituito [**da TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) per determinare se sono state rilevate esecuzioni di glifi di colore. Un **valore HRESULT** **di DWRITE E \_ \_ NOCOLOR** indica l'assenza di un'esecuzione di glifi di colore applicabile.
3.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) non ha segnalato esecuzioni di glifi di colore (tramite la restituzione di **DWRITE \_ E \_ NOCOLOR),** l'intera esecuzione del glifo viene considerata monocromatica e l'app deve disegnarla come desiderato (ad esempio, usando [**ID2D1DeviceContext::D rawGlyphRun).**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)
4.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) segnala la presenza di esecuzioni di glifi a colori, l'app deve ignorare l'esecuzione dell'icona primaria e usare invece le esecuzioni di glifi a colori restituite da TranslateColorGlyphRun. A tale scopo, eseguire l'iterazione dell'oggetto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) restituito, recuperando ogni esecuzione del glifo colore e disegnandola nel modo appropriato per il formato immagine del glifo. Ad esempio, è possibile usare [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) per disegnare glifi bitmap a colori e glifi SVG rispettivamente.

Nell'esempio di codice seguente viene illustrata la struttura generale di questa procedura:


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Uso dei tipi di carattere a colori con Win2D

Analogamente a Direct2D, le API di disegno del testo Win2D non eseguono il rendering dei glifi a colori per impostazione predefinita. Per acconsentire esplicitamente al rendering dei glifi a colori, imposta il flag di opzioni [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) nell'oggetto formato testo che l'app passa al metodo di disegno del testo. L'esempio di codice seguente illustra come eseguire il rendering di una stringa in un tipo di carattere a colori usando Win2D:


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>Argomenti correlati

[DirectWrite di glifi colorati](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interfaccia IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Metodo IDWriteFactory4::TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**Metodo ID2D1DeviceContext4::D rawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

