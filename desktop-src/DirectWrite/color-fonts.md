---
title: Caratteri a colori
description: Questo argomento descrive i tipi di carattere di colore, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104562652"
---
# <a name="color-fonts"></a>Caratteri a colori

Questo argomento descrive i tipi di carattere di colore, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.

Questo documento contiene le parti seguenti:

-   [Che cosa sono i tipi di carattere colore?](#what-are-color-fonts)
-   [Perché usare i tipi di carattere colore?](#why-use-color-fonts)
-   [Quali tipi di tipi di carattere colori supporta Windows?](#what-kinds-of-color-fonts-does-windows-support)
-   [Uso di tipi di carattere colori](#using-color-fonts)
    -   [Uso di tipi di carattere a colori in un'app XAML](#using-color-fonts-in-a-xaml-app)
    -   [Uso di tipi di carattere a colori in Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Uso dei tipi di carattere colori con DirectWrite e Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Uso dei tipi di carattere colore con Win2D](#using-color-fonts-with-win2d)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-color-fonts"></a>Che cosa sono i tipi di carattere colore?

I tipi di carattere colori, detti anche tipi di carattere a colori o tipi di carattere cromatici, rappresentano una tecnologia per i tipi di carattere che consente ai progettisti di utilizzare più colori all'interno di ogni glifo. I tipi di carattere colori consentono scenari di testo multicolore in app e siti Web con meno codice e un supporto più affidabile del sistema operativo rispetto alle tecniche ad hoc implementate sopra il sistema di rendering del testo.

I tipi di carattere con cui si conosce probabilmente non sono tipi di carattere colore. Questi tipi di carattere definiscono solo la forma dei glifi che contengono, sia con le linee di vettore sia con le bitmap monocromatiche. In fase di disegnare, un renderer di testo riempie la forma del glifo usando un solo colore (il colore del carattere) specificato dall'app o dal documento sottoposto a rendering. I tipi di carattere colore, d'altra parte, contengono informazioni sui colori, oltre alle informazioni sulla forma. Alcuni approcci consentono ai progettisti di tipi di carattere di offrire più tavolozze dei colori, offrendo la flessibilità artistica del tipo di carattere.

Nell'esempio seguente viene illustrato un glifo del tipo di carattere del colore Segoe UI emoji. Il rendering del glifo viene eseguito in monocromia a sinistra e in colore a destra.

![Mostra i glifi affiancati, il glifo di sinistra di cui è stato eseguito il rendering in monocromatico, il diritto nel tipo di carattere colore Segoe U I emoji.](images/color-font-cat.png)

I tipi di carattere dei colori includono in genere informazioni di fallback per le piattaforme che non supportano i tipi di carattere colori o per scenari in cui la funzionalità dei colori è stata disabilitata Su queste piattaforme, i tipi di carattere colore vengono visualizzati come tipi di carattere monocromatici regolari.

## <a name="why-use-color-fonts"></a>Perché usare i tipi di carattere colore?

Storicamente, i progettisti e gli sviluppatori hanno usato diverse tecniche per ottenere testo multicolore. Ad esempio, i siti web usano spesso immagini raster anziché testo per visualizzare intestazioni avanzate. Questo approccio consente la flessibilità artistica, ma la grafica raster non è scalabile correttamente per tutte le dimensioni di visualizzazione, né fornisce le stesse funzionalità di accessibilità del testo reale. Un'altra tecnica comune è quella di sovrapporre più tipi di carattere monocromatici con diversi colori dei tipi di carattere, ma questo in genere richiede un codice di layout aggiuntivo da gestire.

I tipi di carattere colore offrono un modo per ottenere questi effetti visivi con tutta la semplicità e la funzionalità dei tipi di carattere normali. Il testo di cui è stato eseguito il rendering in un tipo di carattere è identico a quello di un altro testo: può essere copiato e incollato, può essere analizzato dagli strumenti di accessibilità e così via.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Quali tipi di tipi di carattere colori supporta Windows?

La [specifica OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definisce diversi modi per incorporare le informazioni sui colori in un tipo di carattere. A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite e Direct2D (e i Framework Windows basati su di essi) supportano tutti questi approcci. Sono riepilogati nella tabella seguente:



| Tecnica                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Colr](/typography/opentype/spec/colr) / Tabelle [CPAL](/typography/opentype/spec/cpal) | USA i livelli di vettori colorati, le cui forme sono definite nello stesso modo dei profili di glifo a colore singolo. **Nota:** Supportato a partire da Windows 8.1. <br/>                                                                                                                                                 |
| Tabella [SVG](/typography/opentype/spec/svg)                                                                 | Usa immagini vettoriali create nel formato di grafica vettoriale scalabile. **Nota:** A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite supporta un subset della specifica SVG completa. Non tutto il contenuto SVG è garantito per il rendering in un tipo di carattere SVG OpenType. Per altri dettagli, vedere [supporto per SVG](../direct2d/svg-support.md) . <br/> |
| [CBDT](/typography/opentype/spec/cbdt) / Tabelle [cblC](/typography/opentype/spec/cblc) | Usa immagini bitmap a colori incorporati.                                                                                                                                                                                                                                                                                |
| tabella [sbix](/typography/opentype/spec/sbix)                                                               | Usa immagini bitmap a colori incorporati.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Uso di tipi di carattere colori

Dal punto di vista dell'utente, i tipi di carattere dei colori sono solo tipi di carattere. Ad esempio, possono in genere essere installate e disinstallate dal sistema in modo analogo ai tipi di carattere monocromatici e vengono visualizzate come testo normale e selezionabile.

Dal punto di vista dello sviluppatore, i tipi di carattere colorati vengono in genere utilizzati allo stesso modo dei tipi di carattere monocromatici. Nei framework XAML e Microsoft Edge è possibile applicare uno stile al testo con i tipi di carattere di colore nello stesso modo dei tipi di carattere normali e, per impostazione predefinita, il rendering del testo verrà eseguito in colore. Tuttavia, se l'app chiama direttamente le API Direct2D (o API Win2D) per eseguire il rendering del testo, deve richiedere esplicitamente il rendering del tipo di carattere colore.

### <a name="using-color-fonts-in-a-xaml-app"></a>Uso di tipi di carattere a colori in un'app XAML

Gli elementi di testo della piattaforma XAML, ad esempio [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon), supportano i tipi di carattere colore per impostazione predefinita. È sufficiente applicare uno stile al testo con un tipo di carattere colore. verrà eseguito il rendering di qualsiasi glifo di colore a colori. L'esempio di codice seguente illustra un modo per applicare uno stile a un TextBlock con un tipo di carattere di colore incluso nell'app. La stessa tecnica si applica ai normali tipi di carattere.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Se non si vuole mai che l'elemento di testo XAML esegua il rendering del testo multicolore, impostare la relativa proprietà [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) su false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Uso di tipi di carattere a colori in Microsoft Edge

Per impostazione predefinita, il rendering dei tipi di carattere di colore viene eseguito in siti Web e app Web in esecuzione su Microsoft Edge, incluso il controllo [WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML. È sufficiente usare HTML e CSS per applicare uno stile al testo con un tipo di carattere colore e qualsiasi glifo di colore verrà sottoposto a rendering in colore.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Uso dei tipi di carattere colori con DirectWrite e Direct2D

L'app può usare i metodi di disegno del testo di livello superiore di Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) oppure può usare tecniche di basso livello per disegnare direttamente le esecuzioni di glifi. In entrambi i casi, l'app richiede modifiche al codice per gestire correttamente i glifi dei colori. Se l'app usa le API **DrawText** e **DrawTextLayout** di Direct2D, si noti che per impostazione predefinita non viene eseguito il rendering delle icone dei colori. In questo modo si evitano modifiche impreviste del comportamento nelle app per il rendering del testo progettate prima del supporto dei tipi di carattere colori.

Per acconsentire esplicitamente al rendering del glifo dei colori, passare le opzioni di testo di disegno d2d1 Abilita il flag opzioni del [**\_ tipo di \_ \_ \_ \_ \_ carattere colore**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) al metodo di disegno. Nell'esempio di codice seguente viene illustrato come chiamare il metodo DrawText di Direct2D per eseguire il rendering di una stringa in un tipo di carattere di colore:


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



Se l'app usa le API di livello inferiore per gestire le esecuzioni di glifi direttamente, continuerà a funzionare in presenza di tipi di carattere di colore, ma non sarà in grado di creare icone dei colori senza logica aggiuntiva.

Per gestire correttamente i glifi dei colori, l'app deve:

1.  Passare le informazioni di esecuzione del glifo a [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), insieme a un parametro dei [**formati di \_ \_ immagine \_ del glifo DWrite**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) che indica i tipi di glifo del colore che l'app è preparata a gestire. Se sono presenti glifi di colore (in base al tipo di carattere e ai **\_ formati di \_ immagine \_ del glifo DWrite** richiesti), DirectWrite suddividerà il glifo primario in esecuzioni di glifi di colore individuali a cui è possibile accedere tramite l'oggetto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) restituito nel passaggio 4.
2.  Controllare HRESULT restituito da [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) per determinare se sono state rilevate esecuzioni di glifi di colore. Un valore **HRESULT** di **DWrite \_ E \_ nocolor** indica che non è stata eseguita alcuna icona dei colori applicabile.
3.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) non ha segnalato l'esecuzione di un glifo dei colori (restituendo **DWrite \_ E \_ nocolor**), l'intera esecuzione del glifo viene considerata come monocromatico e l'app deve essere disegnato come desiderato (ad esempio, usando [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) segnala la presenza delle esecuzioni del glifo dei colori, l'app deve ignorare l'esecuzione del glifo principale e usare invece le esecuzioni del glifo dei colori restituite da TranslateColorGlyphRun. A tale scopo, eseguire l'iterazione dell'oggetto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) restituito, recuperare ogni icona del colore e disegnarla come appropriato per il formato dell'immagine del glifo. ad esempio, è possibile usare [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) per disegnare rispettivamente i glifi di bitmap di colore e i glifi svg.

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



### <a name="using-color-fonts-with-win2d"></a>Uso dei tipi di carattere colore con Win2D

Analogamente a Direct2D, le API di disegno del testo di Win2D non eseguono il rendering delle icone dei colori per impostazione predefinita. Per acconsentire esplicitamente al rendering del glifo dei colori, impostare il flag delle opzioni [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) nell'oggetto formato testo che l'app passa al metodo di disegno del testo. Nell'esempio di codice seguente viene illustrato come eseguire il rendering di una stringa in un tipo di carattere colore utilizzando Win2D:


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

[Esempio di glifo colorato DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interfaccia IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Metodo IDWriteFactory4:: TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4::D Metodo rawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

