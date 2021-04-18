---
title: Esercitazione Introduzione con DirectWrite
description: Questo documento illustra come usare DirectWrite e Direct2D per creare testo semplice che contiene un singolo formato e quindi il testo che contiene più formati.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, esercitazione
- DirectWrite, esercitazione introduttiva
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interfaccia IDWriteTextLayout
- Interfaccia IDWriteTextLayout
- DirectWrite, interfaccia IDWriteTypography
- Interfaccia IDWriteTypography
- DirectWrite, interfaccia IDWriteTextFormat
- Interfaccia IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338446"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Esercitazione: Introduzione con DirectWrite

Questo documento illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) per creare testo semplice che contiene un singolo formato e quindi il testo che contiene più formati.

Questa esercitazione contiene le parti seguenti:

-   [Codice sorgente](#source-code)
-   [Disegno di testo semplice](#drawing-simple-text)
    -   [Parte 1: dichiarare le risorse DirectWrite e Direct2D.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Parte 2: creare risorse indipendenti dal dispositivo.](#part-2-create-device-independent-resources)
    -   [Parte 3: creare Device-Dependent risorse.](#part-3-create-device-dependent-resources)
    -   [Parte 4: creare il testo usando il metodo DrawText Direct2D.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Parte 5: rendering del contenuto della finestra tramite Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Disegno di testo con più formati.](#drawing-text-with-multiple-formats)
    -   [Parte 1: creare un'interfaccia IDWriteTextLayout.](#part-1-create-an-idwritetextlayout-interface)
    -   [Parte 2: applicazione della formattazione con IDWriteTextLayout.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Parte 3: aggiunta di funzionalità tipografiche con IDWriteTypography.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Parte 4: creare il testo usando il metodo DrawTextLayout di Direct2D.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Codice sorgente

Il codice sorgente illustrato in questa panoramica viene tratto dall' [esempio di Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples). Ogni parte è implementata in una classe separata (SimpleText e multiformattedtext) e viene visualizzata in una finestra figlio separata. Ogni classe rappresenta una finestra di Microsoft Win32. Oltre al metodo *WndProc* , ogni classe contiene i metodi seguenti:



| Funzione                              | Descrizione                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Crea risorse indipendenti dal dispositivo, in modo che possano essere riutilizzate ovunque.                      |
| **DiscardDeviceIndependentResources** | Rilascia le risorse indipendenti dal dispositivo dopo che non sono più necessarie.                          |
| **CreateDeviceResources**             | Crea risorse, ad esempio pennelli e destinazioni di rendering, associate a un determinato dispositivo.        |
| **DiscardDeviceResources**            | Rilascia le risorse dipendenti dal dispositivo dopo che non sono più necessarie.                            |
| **DrawD2DContent**                    | USA [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering sullo schermo.                              |
| **DrawText**                          | Disegna la stringa di testo tramite [Direct2D](../direct2d/direct2d-portal.md).                            |
| **OnResize**                          | Ridimensiona la destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) quando la dimensione della finestra viene modificata. |



 

È possibile utilizzare l'esempio fornito oppure utilizzare le istruzioni seguenti per aggiungere [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) alla propria applicazione Win32. Per ulteriori informazioni sull'esempio e sui file di progetto associati, vedere l' [esempio DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Disegno di testo semplice

Questa sezione illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering di un testo semplice con un solo formato, come illustrato nella schermata seguente.

![Screenshot di "Hello World using DirectWrite!" in un singolo formato](images/simplecropped.png)

Il disegno di testo semplice sullo schermo richiede quattro componenti:

-   Stringa di caratteri di cui eseguire il rendering.
-   Istanza di [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).
-   Dimensioni dell'area in cui includere il testo.
-   Oggetto in grado di eseguire il rendering del testo. In questa esercitazione. si usa una destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) .

L'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descrive il nome della famiglia di caratteri, le dimensioni, il peso, lo stile e l'estensione usati per formattare il testo e descrive le informazioni sulle impostazioni locali. **IDWriteTextFormat** definisce inoltre i metodi per l'impostazione e il recupero delle proprietà seguenti:

-   Interlinea.
-   Allineamento del testo relativo ai bordi sinistro e destro della casella di layout.
-   Allineamento del paragrafo rispetto alla parte superiore e inferiore della casella di layout.
-   Direzione di lettura.
-   Granularità del testo che ha causato l'overflow della casella di layout.
-   L'arresto della tabulazione incrementale.
-   Direzione del flusso di paragrafo.

L'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) è necessaria per il disegno di testo che usa entrambi i processi descritti in questo documento.

Prima di poter creare un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o qualsiasi altro oggetto [DirectWrite](direct-write-portal.md) , è necessaria un'istanza di [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Usare un **IDWriteFactory archiviata nei** per creare istanze di **IDWriteTextFormat** e altri oggetti DirectWrite. Per ottenere un'istanza di Factory, usare la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>Parte 1: dichiarare le risorse DirectWrite e Direct2D.

In questa parte, si dichiarano gli oggetti che verranno usati in un secondo momento per la creazione e la visualizzazione di testo come membri dati privati della classe. Tutte le interfacce, le funzioni e i tipi di DataType per [DirectWrite](direct-write-portal.md) sono dichiarati nel file di intestazione *DWrite. h* e quelli per [Direct2D](../direct2d/direct2d-portal.md) sono dichiarati in *d2d1. h*; Se questa operazione non è già stata eseguita, includere le intestazioni nel progetto.

1.  Nel file di intestazione della classe (SimpleText. h) dichiarare i puntatori alle interfacce [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) come membri privati.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Dichiarare i membri che contengono la stringa di testo di cui eseguire il rendering e la lunghezza della stringa.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Dichiarare i puntatori alle interfacce [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) per il rendering del testo con [Direct2D](../direct2d/direct2d-portal.md).
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Parte 2: creare risorse indipendenti dal dispositivo.

[Direct2D](rendering-by-using-direct2d.md) fornisce due tipi di risorse: risorse dipendenti dal dispositivo e risorse indipendenti dal dispositivo. Le risorse dipendenti dal dispositivo sono associate a un dispositivo di rendering e non funzionano più se il dispositivo è stato rimosso. Le risorse indipendenti dal dispositivo, d'altra parte, possono durare per l'ambito dell'applicazione.

Le risorse di [DirectWrite](direct-write-portal.md) sono indipendenti dal dispositivo.

In questa sezione vengono create le risorse indipendenti dal dispositivo utilizzate dall'applicazione. Queste risorse devono essere liberate con una chiamata al metodo di **rilascio** dell'interfaccia.

Alcune risorse utilizzate devono essere create solo una volta e non sono associate a un dispositivo. L'inizializzazione per queste risorse viene inserita nel metodo *SimpleText:: CreateDeviceIndependentResources* , che viene chiamato durante l'inizializzazione della classe.

1.  All'interno del metodo *SimpleText:: CreateDeviceIndependentResources* nel file di implementazione della classe (SimpleText. cpp), chiamare la funzione [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) per creare un'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , ovvero l'interfaccia Factory radice per tutti gli oggetti [Direct2D](../direct2d/direct2d-portal.md) . Si usa la stessa factory per creare un'istanza di altre risorse Direct2D.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  Chiamare la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) per creare un'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , che è l'interfaccia Factory radice per tutti gli oggetti [DirectWrite](direct-write-portal.md) . Si usa la stessa factory per creare un'istanza di altre risorse di DirectWrite.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Inizializzare la stringa di testo e archiviarne la lunghezza.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Creare un oggetto interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usando il metodo [**IDWriteFactory archiviata nei:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) . **IDWriteTextFormat** specifica il tipo di carattere, il peso, l'estensione, lo stile e le impostazioni locali che verranno utilizzati per eseguire il rendering della stringa di testo.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Centrare il testo orizzontalmente e verticalmente chiamando i metodi [**IDWriteTextFormat:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

In questa parte sono state inizializzate le risorse indipendenti dal dispositivo utilizzate dall'applicazione. Nella parte successiva si inizializzano le risorse dipendenti dal dispositivo.

### <a name="part-3-create-device-dependent-resources"></a>Parte 3: creare Device-Dependent risorse.

In questa parte viene creato un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) per il rendering del testo.

Una destinazione di rendering è un oggetto Direct2D che consente di creare risorse di disegno ed eseguire il rendering dei comandi di disegno in un dispositivo di rendering. Un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) è una destinazione di rendering che esegue il rendering in un **HWND**.

Una delle risorse di disegno che una destinazione di rendering può creare è un pennello per disegnare strutture, riempimenti e testo. Un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) disegna con un colore a tinta unita.

Entrambe le interfacce [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) sono associate a un dispositivo di rendering quando vengono create e devono essere rilasciate e ricreate se il dispositivo diventa non valido.

1.  All'interno del metodo SimpleText:: CreateDeviceResources controllare se il puntatore della destinazione di rendering è **null**. In caso contrario, recuperare le dimensioni dell'area di rendering e creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) di tale dimensione. Usare **ID2D1HwndRenderTarget** per creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  Nel metodo SimpleText::D iscardDeviceResources, rilasciare sia il pennello che la destinazione di rendering.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Ora che è stata creata una destinazione di rendering e un pennello, è possibile usarli per eseguire il rendering del testo.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Parte 4: creare il testo usando il metodo DrawText Direct2D.

1.  Nel metodo SimpleText::D rawText della classe definire l'area per il layout del testo recuperando le dimensioni dell'area di rendering e creando un rettangolo [Direct2D](../direct2d/direct2d-portal.md) con le stesse dimensioni.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Usare il metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e l'oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) per eseguire il rendering del testo sullo schermo. Il metodo **ID2D1RenderTarget::D rawtext** accetta i parametri seguenti:
    -   Stringa di cui eseguire il rendering.
    -   Puntatore a un'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Rettangolo di layout [Direct2D](../direct2d/direct2d-portal.md) .
    -   Puntatore a un'interfaccia che espone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Parte 5: rendering del contenuto della finestra tramite Direct2D

Per eseguire il rendering del contenuto della finestra tramite [Direct2D](../direct2d/direct2d-portal.md) quando viene ricevuto un messaggio di disegno, procedere come segue:

1.  Creare le risorse dipendenti dal dispositivo chiamando il metodo SimpleText:: CreateDeviceResources implementato nella parte 3.
2.  Chiamare il metodo [**ID2D1HwndRenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) della destinazione di rendering.
3.  Cancellare la destinazione di rendering chiamando il metodo [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .
4.  Chiamare il metodo SimpleText::D rawText, implementato nella parte 4.
5.  Chiamare il metodo [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) della destinazione di rendering.
6.  Se necessario, rimuovere le risorse dipendenti dal dispositivo in modo che possano essere ricreate quando la finestra viene ridisegnato.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



La classe SimpleText è implementata in SimpleText. h e SimpleText. cpp.

## <a name="drawing-text-with-multiple-formats"></a>Disegno di testo con più formati.

Questa sezione illustra come usare [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering del testo con più formati, come illustrato nella schermata seguente.

![Screenshot di "Hello World using DirectWrite!", con alcune parti di stili, dimensioni e formati diversi](images/multiformattedcropped.png)

Il codice per questa sezione viene implementato come classe multiformattedtext nell' [esempio DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples). Si basa sui passaggi della sezione precedente.

Per creare testo multiformattato, è possibile usare l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , oltre all'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introdotta nella sezione precedente. L'interfaccia **IDWriteTextLayout** descrive la formattazione e il layout di un blocco di testo. Oltre alla formattazione predefinita specificata da un oggetto **IDWriteTextFormat** , è possibile modificare la formattazione di intervalli di testo specifici utilizzando **IDWriteTextLayout**. Sono inclusi il nome della famiglia di caratteri, le dimensioni, il peso, lo stile, l'estensione, la barratura e la sottostruttura.

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fornisce anche metodi di hit testing. Le metriche di hit testing restituite da questi metodi sono relative alla casella di layout specificata quando l'oggetto interfaccia **IDWriteTextLayout** viene creato tramite il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) dell'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

L'interfaccia [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) viene utilizzata per aggiungere funzionalità tipografiche [OpenType](../intl/opentype-font-format.md) facoltative a un layout di testo, ad esempio ornati e set di testo stilistici alternativi. Le funzionalità tipografiche possono essere aggiunte a un intervallo di testo specifico all'interno di un layout di testo chiamando il metodo [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) dell'interfaccia **IDWriteTypography** . Questo metodo riceve una struttura della [**\_ \_ funzionalità del tipo di carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) come parametro che contiene una costante di enumerazione dei tag della **funzionalità del tipo di \_ carattere \_ \_ DWrite** e un parametro di esecuzione **UInt32** . Un elenco di funzionalità OpenType registrate è reperibile nel [Registro di sistema dei tag di layout OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) in Microsoft.com. Per le costanti di enumerazione DirectWrite equivalenti, **vedere \_ \_ \_ tag della funzionalità del tipo di carattere DWrite**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Parte 1: creare un'interfaccia IDWriteTextLayout.

1.  Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe multiformattedtext.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Alla fine del metodo multiformattedtext:: CreateDeviceIndependentResources, creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) . L'interfaccia **IDWriteTextLayout** fornisce funzionalità di formattazione aggiuntive, ad esempio la possibilità di applicare formati diversi alle parti di testo selezionate.
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Parte 2: applicazione della formattazione con IDWriteTextLayout.

La formattazione, ad esempio la dimensione del carattere, il peso e la sottostruttura, può essere applicata a sottostringhe del testo da visualizzare mediante l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

1.  Impostare la dimensione del carattere per la sottostringa "di" di "DirectWrite" su 100 dichiarando un [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chiamando il metodo [**IDWriteTextLayout:: sefontsize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  Sottolineare la sottostringa "DirectWrite" chiamando il metodo [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) SetValue.
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  Impostare lo spessore del carattere su grassetto per la sottostringa "DirectWrite" chiamando il metodo [**IDWriteTextLayout:: FontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Parte 3: aggiunta di funzionalità tipografiche con IDWriteTypography.

1.  Dichiarare e creare un oggetto interfaccia [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) chiamando il metodo [**IDWriteFactory archiviata nei:: CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Aggiungere una funzionalità del tipo di carattere dichiarando un oggetto della [**\_ \_ funzionalità del tipo di carattere DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) con il set stilistico 7 specificato e chiamando il metodo [**IDWriteTypography:: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Impostare il layout del testo in modo da usare la funzionalità Typography sull'intera stringa dichiarando una variabile di [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chiamando il metodo [**IDWriteTextLayout:: setypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando l'intervallo di testo.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Impostare la nuova larghezza e l'altezza per l'oggetto layout di testo nel metodo multiformattedtext:: OnResize.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Parte 4: creare il testo usando il metodo DrawTextLayout di Direct2D.

Per tracciare il testo con le impostazioni di layout del testo specificate dall'oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , modificare il codice nel metodo multiformattedtext::D rawtext per usare [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare una variabile [**d2d1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) e la imposta sul punto in alto a sinistra della finestra.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Disegnare il testo sullo schermo chiamando il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) della destinazione di rendering [Direct2D](../direct2d/direct2d-portal.md) e passando il puntatore [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

La classe multiformattedtext è implementata in multiformattedtext. h e multiformattedtext. cpp.

 

 