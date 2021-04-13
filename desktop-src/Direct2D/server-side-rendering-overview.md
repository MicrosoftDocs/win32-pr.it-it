---
title: Uso di Direct2D per il rendering di Server-Side
description: Viene descritto l'utilizzo di Direct2D per il rendering lato server.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, rendering lato server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399146"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Uso di Direct2D per il rendering di Server-Side

Direct2D è particolarmente adatto per applicazioni grafiche che richiedono il rendering lato server in Windows Server. Questa panoramica descrive le nozioni di base sull'uso di Direct2D per il rendering lato server. Contiene le sezioni seguenti:

-   [Requisiti per il rendering di Server-Side](#requirements-for-server-side-rendering)
-   [Opzioni per le API disponibili](#options-for-available-apis)
    -   [GDI](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Come usare Direct2D per il rendering di Server-Side](#how-to-use-direct2d-for-server-side-rendering)
    -   [Rendering del software](#software-rendering)
    -   [Multithreading](#multithreading)
    -   [Generazione di un file bitmap](#generating-a-bitmap-file)
-   [Conclusione](#conclusion)
-   [Argomenti correlati](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Requisiti per il rendering di Server-Side

Di seguito è riportato uno scenario tipico per un server del grafico: il rendering di grafici e grafici viene eseguito in un server e recapitato come bitmap in risposta alle richieste Web. Il server potrebbe essere dotato di una scheda grafica di fascia bassa o nessuna scheda grafica.

Questo scenario rivela tre requisiti dell'applicazione. In primo luogo, l'applicazione deve gestire più richieste simultanee in modo efficiente, soprattutto nei server multicore. In secondo luogo, l'applicazione deve utilizzare il rendering del software quando viene eseguito su server con una scheda grafica di fascia bassa o senza scheda grafica. Infine, l'applicazione deve essere eseguita come servizio nella sessione 0 in modo che non richieda l'accesso di un utente. Per ulteriori informazioni sulla sessione 0, vedere [Impact of Session 0 isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).

## <a name="options-for-available-apis"></a>Opzioni per le API disponibili

Sono disponibili tre opzioni per il rendering lato server: GDI, GDI+ e Direct2D. Come GDI e GDI+, Direct2D è un'API di rendering 2D nativa che offre alle applicazioni un maggiore controllo sull'uso dei dispositivi grafici. Inoltre, Direct2D supporta in modo univoco una factory a thread singolo e con multithreading. Le sezioni seguenti confrontano ogni API in termini di qualità del disegno e rendering sul lato server multithreading.

### <a name="gdi"></a>GDI

A differenza di Direct2D e GDI+, GDI non supporta le funzionalità di disegno di alta qualità. Ad esempio, GDI non supporta l'anti-aliasing per la creazione di linee smussate e ha solo un supporto limitato per la trasparenza. In base ai risultati dei test delle prestazioni della grafica in Windows 7 e Windows Server 2008 R2, Direct2D viene ridimensionato in modo più efficiente rispetto a GDI, nonostante la riprogettazione dei blocchi in GDI. Per ulteriori informazioni su questi risultati dei test, vedere la pagina relativa alla [progettazione delle prestazioni grafiche di Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Inoltre, le applicazioni che utilizzano GDI sono limitate a 10240 handle GDI per processo e 65536 handle GDI per sessione. Il motivo è che Windows internamente utilizza una parola a 16 bit per archiviare l'indice degli handle per ogni sessione.

### <a name="gdi"></a>GDI+

Sebbene GDI+ supporti l'anti-aliasing e la fusione alfa per il disegno di alta qualità, il problema principale con GDI+ per gli scenari server è che non supporta l'esecuzione nella sessione 0. Poiché la sessione 0 supporta solo funzionalità non interattive, le funzioni che interagiscono direttamente o indirettamente con i dispositivi di visualizzazione riceveranno degli errori. Esempi specifici di funzioni includono non solo quelli che gestiscono i dispositivi di visualizzazione, ma anche quelli che gestiscono indirettamente i driver di dispositivo.

Analogamente a GDI, GDI+ è limitato dal meccanismo di blocco. I meccanismi di blocco in GDI+ sono gli stessi in Windows 7 e Windows Server 2008 R2 come nelle versioni precedenti.

### <a name="direct2d"></a>Direct2D

Direct2D è un'API grafica 2D, con accelerazione immediata e in modalità immediata, che offre prestazioni elevate e rendering di alta qualità. Offre una factory a thread singolo e una factory a thread multipli e il ridimensionamento lineare del rendering del software con granularità dei corsi.

A tale scopo, Direct2D definisce un'interfaccia Factory radice. Come regola, un oggetto creato in una factory può essere usato solo con altri oggetti creati dalla stessa factory. Il chiamante può richiedere una factory a thread singolo o con multithreading al momento della creazione. Se viene richiesta una factory a thread singolo, non viene eseguito alcun blocco dei thread. Se il chiamante richiede una factory multithreading, viene acquisito un blocco di thread a livello di Factory ogni volta che viene effettuata una chiamata a Direct2D.

Inoltre, il blocco dei thread in Direct2D è più granulare rispetto a GDI e GDI+, in modo che l'incremento del numero di thread abbia un effetto minimo sulle prestazioni.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Come usare Direct2D per il rendering di Server-Side

Le sezioni seguenti descrivono come usare il rendering del software, come usare in modo ottimale una factory a thread singolo e con multithreading e come creare e salvare un disegno complesso in un file.

### <a name="software-rendering"></a>Rendering del software

Le applicazioni lato server usano il rendering del software creando la destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , con il tipo di destinazione di rendering impostato su d2d1 \_ Render \_ target type \_ \_ software o d2d1 \_ Render \_ target \_ Type \_ default. Per ulteriori informazioni sulle destinazioni di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , vedere il metodo [**ID2D1Factory:: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) . Per ulteriori informazioni sui tipi di destinazione di rendering, [**vedere \_ \_ \_ tipo di destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

Sapere come creare e condividere le fabbriche e le destinazioni di rendering tra i thread può influire significativamente sulle prestazioni di un'applicazione. Nelle tre figure seguenti sono illustrati tre approcci diversi. L'approccio ottimale è illustrato nella figura 3.

![diagramma multithreading Direct2D con una singola destinazione di rendering.](images/server-side-rendering-1.png)

Nella figura 1, i diversi thread condividono la stessa factory e la stessa destinazione di rendering. Questo approccio può causare risultati imprevedibili nei casi in cui più thread cambiano simultaneamente lo stato della destinazione di rendering condivisa, ad esempio impostando contemporaneamente la matrice di trasformazione. Poiché il blocco interno in Direct2D non sincronizza una risorsa condivisa, ad esempio le destinazioni di rendering, questo approccio può causare il fallimento della chiamata [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) nel thread 1, perché nel thread 2 la chiamata **BeginDraw** sta già usando la destinazione di rendering condivisa.

![diagramma multithreading Direct2D con più destinazioni di rendering.](images/server-side-rendering-2.png)

Per evitare i risultati imprevedibili rilevati nella figura 1, la figura 2 Mostra una factory multithreading con ogni thread con una propria destinazione di rendering. Questo approccio funziona, ma funziona in modo efficace come applicazione a thread singolo. Il motivo è che il blocco a livello di Factory si applica solo al livello di operazione di disegno e tutte le chiamate di disegno nella stessa factory di conseguenza vengono serializzate. Di conseguenza, il thread 1 viene bloccato durante il tentativo di immissione di una chiamata di disegno, mentre il thread 2 sta per eseguire un'altra chiamata di disegno.

![diagramma multithreading Direct2D con più Factory e più destinazioni di rendering.](images/server-side-rendering-3.png)

Nella figura 3 viene illustrato l'approccio ottimale, in cui vengono utilizzate una factory a thread singolo e una destinazione di rendering a thread singolo. Poiché non viene eseguito alcun blocco quando si usa una factory a thread singolo, le operazioni di disegno in ogni thread possono essere eseguite simultaneamente per ottenere prestazioni ottimali.

### <a name="generating-a-bitmap-file"></a>Generazione di un file bitmap

Per generare un file bitmap utilizzando il rendering del software, utilizzare una destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Usare un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) per scrivere la bitmap in un file. Usare [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap in un formato di immagine specificato. Nell'esempio di codice seguente viene illustrato come creare e salvare l'immagine seguente in un file.

![esempio di immagine di output.](images/saveasimagefile-sample.png)

Questo esempio di codice crea prima un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) e una destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Viene quindi eseguito il rendering di un disegno con un testo, una geometria del percorso che rappresenta un vetro dell'ora e un vetro dell'ora trasformato in una bitmap WIC. USA quindi [IWICStream:: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) per salvare la bitmap in un file. Se l'applicazione deve salvare la bitmap in memoria, usare invece [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) . Infine, USA [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Conclusione

Come illustrato nell'esempio precedente, l'uso di Direct2D per il rendering lato server è semplice e diretto. Fornisce inoltre un rendering di elevata qualità e altamente eseguibili che può essere eseguito in ambienti con privilegi limitati del server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 