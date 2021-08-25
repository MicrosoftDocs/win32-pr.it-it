---
title: Uso di Direct2D per Server-Side rendering
description: Descrive l'uso di Direct2D per il rendering lato server.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, rendering lato server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65991d2437939ce7f1d218022e0c3c57649405a18e2c1b9d073635b5b37d1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917216"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Uso di Direct2D per Server-Side rendering

Direct2D è particolarmente adatto per le applicazioni grafiche che richiedono il rendering lato server in Windows Server. Questa panoramica descrive le nozioni di base sull'uso di Direct2D per il rendering lato server. Contiene le sezioni seguenti:

-   [Requisiti per Server-Side rendering](#requirements-for-server-side-rendering)
-   [Opzioni per le API disponibili](#options-for-available-apis)
    -   [Gdi](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Come usare Direct2D per Server-Side rendering](#how-to-use-direct2d-for-server-side-rendering)
    -   [Software Rendering](#software-rendering)
    -   [Multithreading](#multithreading)
    -   [Generazione di un file bitmap](#generating-a-bitmap-file)
-   [Conclusione](#conclusion)
-   [Argomenti correlati](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Requisiti per Server-Side rendering

Di seguito è riportato uno scenario tipico per un server grafico: il rendering di grafici e grafica viene eseguito su un server e recapitato come bitmap in risposta alle richieste Web. Il server potrebbe essere dotato di una scheda grafica di fascia bassa o di nessuna scheda grafica.

Questo scenario presenta tre requisiti dell'applicazione. In primo luogo, l'applicazione deve gestire in modo efficiente più richieste simultanee, in particolare nei server multicore. In secondo piano, l'applicazione deve usare il rendering software quando è in esecuzione su server con una scheda grafica di fascia bassa o senza scheda grafica. Infine, l'applicazione deve essere eseguita come servizio in sessione 0 in modo che non richieda l'accesso di un utente. Per altre informazioni sui sessione 0, vedere [Impatto dell'isolamento](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx)sessione 0 su servizi e driver in Windows .

## <a name="options-for-available-apis"></a>Opzioni per le API disponibili

Per il rendering lato server sono disponibili tre opzioni: GDI, GDI+ e Direct2D. Come GDI e GDI+, Direct2D è un'API di rendering 2D nativa che offre alle applicazioni un maggiore controllo sull'uso di dispositivi grafici. Inoltre, Direct2D supporta in modo univoco una factory a thread singolo e una factory multithreading. Le sezioni seguenti confrontano ogni API in termini di qualità di disegno e rendering lato server multithreading.

### <a name="gdi"></a>GDI

A differenza di Direct2D e GDI+, GDI non supporta funzionalità di disegno di alta qualità. Ad esempio, GDI non supporta l'antialiasing per la creazione di linee smussate e ha solo un supporto limitato per la trasparenza. In base ai risultati dei test delle prestazioni grafiche in Windows 7 e Windows Server 2008 R2, Direct2D viene ridimensionato in modo più efficiente rispetto a GDI, nonostante la riprogettazione dei blocchi in GDI. Per altre informazioni su questi risultati dei test, vedere [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Inoltre, le applicazioni che usano GDI sono limitate a 10240 handle GDI per processo e 65536 handle GDI per sessione. Il motivo è che internamente Windows un word a 16 bit per archiviare l'indice degli handle per ogni sessione.

### <a name="gdi"></a>GDI+

Sebbene GDI+ supporti l'antialiasing e la fusione alfa per il disegno di alta qualità, il problema principale di GDI+ per gli scenari server è che non supporta l'esecuzione in sessione 0. Poiché sessione 0 supporta solo funzionalità non interattive, le funzioni che interagiscono direttamente o indirettamente con i dispositivi di visualizzazione riceveranno quindi errori. Esempi specifici di funzioni includono non solo quelli che gestiscono i dispositivi di visualizzazione, ma anche quelli che gestiscono indirettamente i driver di dispositivo.

Analogamente a GDI, GDI+ è limitato dal meccanismo di blocco. I meccanismi di blocco in GDI+ sono gli stessi in Windows 7 e Windows Server 2008 R2 come nelle versioni precedenti.

### <a name="direct2d"></a>Direct2D

Direct2D è un'API grafica 2D in modalità immediata e accelerata dall'hardware che offre prestazioni elevate e rendering di alta qualità. Offre una factory a thread singolo e multithreading e il ridimensionamento lineare del rendering software con granularità corrente.

A tale scopo, Direct2D definisce un'interfaccia factory radice. Di norma, un oggetto creato in una factory può essere usato solo con altri oggetti creati dalla stessa factory. Il chiamante può richiedere una factory a thread singolo o multithread al momento della creazione. Se viene richiesta una factory a thread singolo, non viene eseguito alcun blocco dei thread. Se il chiamante richiede una factory multithreading, viene acquisito un blocco di thread a livello di factory ogni volta che viene effettuata una chiamata in Direct2D.

Inoltre, il blocco dei thread in Direct2D è più granulare rispetto a GDI e GDI+, in modo che l'aumento del numero di thread abbia un impatto minimo sulle prestazioni.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Come usare Direct2D per Server-Side rendering

Le sezioni seguenti descrivono come usare il rendering software, come usare in modo ottimale una factory a thread singolo e multithreading e come disegnare e salvare un disegno complesso in un file.

### <a name="software-rendering"></a>Software Rendering

Le applicazioni lato server usano il rendering software creando una destinazione di rendering [IWICBitmap,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) con il tipo di destinazione di rendering impostato su D2D1 RENDER TARGET TYPE SOFTWARE o \_ \_ \_ \_ D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT. Per altre informazioni sulle destinazioni di rendering [IWICBitmap,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) vedere il [**metodo ID2D1Factory::CreateWicBitmapRenderTarget.**](id2d1factory-createwicbitmaprendertarget.md) Per altre informazioni sui tipi di destinazione di rendering, vedere [**D2D1 \_ RENDER \_ TARGET \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

La conoscenza di come creare e condividere factory ed eseguire il rendering delle destinazioni tra thread può influire in modo significativo sulle prestazioni di un'applicazione. Le tre figure seguenti mostrano tre approcci diversi. L'approccio ottimale è illustrato nella figura 3.

![Diagramma del multithreading direct2d con una singola destinazione di rendering.](images/server-side-rendering-1.png)

Nella figura 1, thread diversi condividono la stessa factory e la stessa destinazione di rendering. Questo approccio può causare risultati imprevedibili nei casi in cui più thread modificano contemporaneamente lo stato della destinazione di rendering condivisa, ad esempio impostando contemporaneamente la matrice di trasformazione. Poiché il blocco interno in Direct2D non sincronizza una risorsa condivisa, ad esempio le destinazioni di rendering, questo approccio può causare l'esito negativo della chiamata [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) nel thread 1, perché nel thread 2 la chiamata **BeginDraw** sta già usando la destinazione di rendering condivisa.

![Diagramma del multithreading direct2d con più destinazioni di rendering.](images/server-side-rendering-2.png)

Per evitare i risultati imprevedibili rilevati nella figura 1, la figura 2 mostra una factory multithreading con ogni thread con una propria destinazione di rendering. Questo approccio funziona ma funziona in modo efficace come un'applicazione a thread singolo. Il motivo è che il blocco a livello di factory si applica solo al livello di operazione di disegno e tutte le chiamate di disegno nella stessa factory vengono di conseguenza serializzate. Di conseguenza, il thread 1 viene bloccato quando si tenta di immettere una chiamata di disegno, mentre il thread 2 è nel mezzo dell'esecuzione di un'altra chiamata di disegno.

![Diagramma del multithreading direct2d con più factory e più destinazioni di rendering.](images/server-side-rendering-3.png)

La figura 3 illustra l'approccio ottimale, in cui vengono usate una factory a thread singolo e una destinazione di rendering a thread singolo. Poiché non viene eseguito alcun blocco quando si usa una factory a thread singolo, le operazioni di disegno in ogni thread possono essere eseguite contemporaneamente per ottenere prestazioni ottimali.

### <a name="generating-a-bitmap-file"></a>Generazione di un file bitmap

Per generare un file bitmap usando il rendering software, usare una destinazione di rendering [IWICBitmap.](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) Usare un [flusso IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) per scrivere la bitmap in un file. Usare [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap in un formato di immagine specificato. Nell'esempio di codice seguente viene illustrato come disegnare e salvare l'immagine seguente in un file.

![immagine di output di esempio.](images/saveasimagefile-sample.png)

Questo esempio di codice crea innanzitutto una destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) e una destinazione di rendering [IWICBitmap.](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) Esegue quindi il rendering di un disegno con testo, una geometria di percorso che rappresenta un'ora e un'ora trasformata in una bitmap WIC. Usa quindi [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) per salvare la bitmap in un file. Se l'applicazione deve salvare la bitmap in memoria, usare [invece IWICStream::InitializeFromMemory.](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) Infine, usa [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap.


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

Come illustrato in precedenza, l'uso di Direct2D per il rendering lato server è semplice e semplice. Offre inoltre un rendering di alta qualità e altamente parallelizzabile che può essere eseguito in ambienti con privilegi minimi del server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 