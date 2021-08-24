---
description: Questo argomento descrive come scrivere testo in un sistema operativo XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Scrivere testo in un sistema operativo XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff2c77106649960982888d7ee8d6e4b679bd62e44be1e0dc9786206261b62bbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718531"
---
# <a name="write-text-to-an-xps-om"></a>Scrivere testo in un sistema operativo XPS

Questo argomento descrive come scrivere testo in un sistema operativo XPS.

Il testo viene inserito in un OM XPS creando e formattazione [**un'interfaccia IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) e quindi aggiungendo l'interfaccia **IXpsOMGlyphs** all'elenco di oggetti visivi della pagina o dell'area di disegno. Ogni **interfaccia IXpsOMGlyphs** rappresenta un'esecuzione di glifi, ovvero un'esecuzione continua di caratteri che condividono un formato comune. Quando un elemento di formato carattere (ad esempio il tipo di carattere o la dimensione) cambia o quando si interrompe una riga, è necessario creare e aggiungere una nuova interfaccia **IXpsOMGlyphs** all'elenco di oggetti visivi.

Alcune delle proprietà di un'esecuzione di glifi possono essere impostate usando i metodi [**dell'interfaccia IXpsOMGlyphs.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) Alcune proprietà, tuttavia, interagiscono con altre e devono essere impostate tramite [**un'interfaccia IXpsOMGlyphsEditor.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).

## <a name="code-example"></a>Esempio di codice

### <a name="create-a-glyph-run-from-a-string"></a>Creare un'esecuzione di glifi da una stringa

Un'esecuzione di glifi viene in genere creata in diversi passaggi che includono il caricamento delle risorse del tipo di carattere usate dall'esecuzione del glifo, l'impostazione di un pennello di riempimento, la specifica delle dimensioni del carattere e della posizione iniziale e l'impostazione della stringa Unicode.

La sezione seguente dell'esempio di codice contiene una routine che accetta alcune variabili, tra cui la dimensione del carattere, il colore e la posizione, e i caratteri da scrivere. Il codice crea quindi un'esecuzione del glifo e quindi lo aggiunge a una pagina. L'esempio di codice presuppone che si sia verificata l'inizializzazione descritta in Inizializzare un sistema operativo [XPS](xps-object-model-initialization.md) e che il documento abbia almeno una pagina. Per altre informazioni sulla creazione di un sistema operativo XPS vuoto, vedere Creare un sistema operativo [XPS vuoto.](create-a-blank-xps-om.md)


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a>Caricare e creare risorse

La creazione di [**un'interfaccia IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) richiede una risorsa tipo di carattere. In molti casi, un blocco di testo usa lo stesso tipo di carattere e lo stesso colore. Di conseguenza, questa sezione dell'esempio di codice creerà le interfacce delle risorse del tipo di carattere che verranno usate nelle chiamate che posizionano il testo nella pagina.


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a>Disegnare testo in una pagina

La sezione finale dell'esempio di codice crea le esecuzioni di glifi per ogni esecuzione di testo formattato in modo simile. Per eseguire il codice in questa sezione finale, sono necessari l'interfaccia **xpsFactory,** nonché la risorsa carattere e un pennello per il colore del testo e devono essere state create e inizializzate istanze. In questo esempio la funzione descritta nella prima sezione viene usata per creare le esecuzioni del glifo e aggiungerle alla pagina.


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Esplorare il sistema operativo XPS](navigate-the-xps-om.md)
</dt> <dt>

[Disegnare grafica in un sistema operativo XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Inserire immagini in un sistema operativo XPS](place-images-in-an-xps-om.md)
</dt> <dt>

[Scrivere un file OM XPS in un documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Stampare un sistema operativo XPS](print-an-xps-om.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[Inizializzare un sistema operativo XPS](xps-object-model-initialization.md)
</dt> <dt>

[Informazioni di riferimento sulle API dei documenti XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
