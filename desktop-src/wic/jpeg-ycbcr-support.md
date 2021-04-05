---
description: A partire da Windows 8.1, il codec JPEG di Windows Imaging Component (WIC) supporta la lettura e la scrittura di dati immagine nel formato YCbCr nativo.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Supporto di YCbCr JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967568"
---
# <a name="jpeg-ycbcr-support"></a>Supporto di YCbCr JPEG

A partire da Windows 8.1, il codec JPEG di [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) supporta la lettura e la scrittura di dati immagine nel formato nativo YC<sub>b</sub>C<sub>r</sub> . Il supporto di WIC YC<sub>b</sub>c<sub>r</sub> può essere usato insieme a [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering dei dati di YC<sub>b</sub>c<sub>r</sub> pixel con effetto immagine. Inoltre, il codec JPEG di WIC può utilizzare i dati di YC<sub>b</sub>C<sub>r</sub> pixel prodotti da determinati driver della fotocamera tramite Media Foundation.

I dati di YC<sub>b</sub>C<sub>r</sub> pixel utilizzano una quantità di memoria significativamente inferiore rispetto ai formati BGRA pixel standard. Inoltre, l'accesso ai dati di YC<sub>b</sub>C<sub>r</sub> consente di eseguire l'offload di alcune fasi della pipeline di decodifica/codifica JPEG in Direct2D con accelerazione GPU. Con YC<sub>b</sub>C<sub>r</sub>, l'app può ridurre il consumo di memoria JPEG e i tempi di caricamento per le stesse immagini di dimensioni e qualità. In alternativa, l'app può usare immagini JPEG di risoluzione più elevata senza subire penalizzazioni delle prestazioni.

In questo argomento viene descritto il funzionamento<sub>dei dati</sub> di YC<sub>b</sub>C e viene illustrato come utilizzarlo in WIC e Direct2D.

-   [Informazioni sui dati JPEG YC<sub>b</sub>C<sub>r</sub>](#about-jpeg-ycbcr-data)
    -   [Modello colori YC<sub>b</sub>C<sub>r</sub>](#ycbcr-color-model)
    -   [Layout di memoria planare e Interleaved](#planar-versus-interleaved-memory-layouts)
    -   [Sottocampionamento Chroma](#chroma-subsampling)
    -   [Utilizzo JPEG di YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Uso dei dati JPEG YC<sub>b</sub>C<sub>r</sub>](#using-jpeg-ycbcr-data)
    -   [Uso delle immagini JPEG di YC<sub>b</sub>C<sub>r</sub>](#using-ycbcr-jpeg-images)
    -   [API componenti Windows Imaging](#windows-imaging-component-apis)
    -   [API Direct2D](#direct2d-apis)
    -   [Determinazione della configurazione di YC<sub>b</sub>C<sub>r</sub> supportata](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decodifica dei dati di YC<sub>b</sub>C<sub>r</sub> pixel](#decoding-ycbcr-pixel-data)
    -   [Trasformazione dei dati di YC<sub>b</sub>C<sub>r</sub> pixel](#transforming-ycbcr-pixel-data)
    -   [Codifica dei dati dei pixel di YC<sub>b</sub>C<sub>r</sub>](#encoding-ycbcr-pixel-data)
    -   [Decodifica dei dati di YC<sub>b</sub>C<sub>r</sub> pixel in Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Argomenti correlati](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Informazioni sui dati JPEG YC<sub>b</sub>C<sub>r</sub>

In questa sezione vengono illustrati alcuni concetti chiave necessari per comprendere in che modo il supporto di YC<sub>b</sub>C<sub>r</sub> in WIC funziona e i vantaggi principali.

### <a name="ycsubbsubcsubrsub-color-model"></a>Modello colori YC<sub>b</sub>C<sub>r</sub>

WIC in Windows 8 e versioni precedenti supporta quattro diversi [modelli di colore](-wic-codec-native-pixel-formats.md), il più comune dei quali è RGB/BGR. Questo modello di colori definisce i dati dei colori utilizzando i componenti rosso, verde e blu; è possibile utilizzare anche un quarto componente alfa.

Ecco un'immagine scomposta nei relativi componenti rosso, verde e blu.

![immagine scomposta nei relativi componenti rosso, verde e blu.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> è un modello di colore alternativo che definisce i dati di colore utilizzando un componente di luminanza (Y) e due componenti cromatura (c<sub>b</sub> e c<sub>r</sub>). Viene in genere usato in scenari di imaging digitale e video. Il termine YC<sub>b</sub>C<sub>r</sub> viene spesso usato in modo interscambiabile con YUV, sebbene i due siano tecnicamente distinti.

Sono disponibili diverse varianti di YC<sub>b</sub>c<sub>r</sub> che differiscono nello spazio dei colori e nelle definizioni di intervallo dinamico: WIC supporta specificamente i dati JPEG JFIF YC<sub>b</sub>c<sub>r</sub> . Per ulteriori informazioni, vedere la [specifica di JPEG ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

Ecco un'immagine scomposta nei componenti Y, C<sub>b</sub>e c<sub>r</sub> .

![immagine scomposta nei componenti y, CB e CR.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Layout di memoria planare e Interleaved

In questa sezione vengono descritte alcune differenze tra l'accesso e l'archiviazione dei dati pixel RGB in memoria rispetto ai dati YC<sub>b</sub>C<sub>r</sub> .

I dati pixel RGB vengono in genere archiviati usando un layout di memoria con interfoliazione. Ciò significa che i dati per un singolo componente a colori sono interfogliati tra i pixel e ogni pixel viene archiviato in modo contiguo nella memoria.

Ecco una figura che mostra i dati pixel RGBA archiviati in un layout di memoria interleaved.

![figura che mostra i dati pixel RGBA archiviati in un layout di memoria interleaved.](graphics/ycbcr3.png)

I dati YC<sub>b</sub>C<sub>r</sub> vengono in genere archiviati usando un layout di memoria planare. Ciò significa che ogni componente colore viene archiviato separatamente nel proprio piano contiguo, per un totale di tre piani. In un'altra configurazione comune, i componenti C<sub>b</sub> e c<sub>r</sub> vengono Interleaved e archiviati insieme, mentre il componente Y rimane nel proprio piano, per un totale di due piani.

Ecco una figura che mostra i dati planari Y e Interleaved C<sub>b</sub>c<sub>r</sub> pixel, un layout comune YC<sub>b</sub>c<sub>r</sub> Memory.

![figura che mostra i dati planari y e CbCr con interfoliazione pixel, un layout comune della memoria YCbCr.](graphics/ycbcr4.png)

In WIC e Direct2D ogni piano di colore viene considerato come un oggetto distinto ( [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)) e collettivamente questi piani formano i dati di supporto per un'immagine YC <sub>b</sub>C <sub>r</sub> .

Mentre WIC supporta l'accesso<sub>ai dati YC</sub> <sub>b</sub>C in entrambe le configurazioni del piano 2 e 3, Direct2D supporta solo la prima (Y e c<sub>b</sub>c<sub>r</sub>). Pertanto, quando si utilizzano WIC e Direct2D insieme, è necessario utilizzare sempre la configurazione 2 del piano YC<sub>b</sub>C<sub>r</sub> .

### <a name="chroma-subsampling"></a>Sottocampionamento Chroma

Il modello di colore YC<sub>b</sub>C<sub>r</sub> è particolarmente adatto per scenari di imaging digitale, in quanto può trarre vantaggio da determinati aspetti del sistema visivo umano. In particolare, gli utenti sono più sensibili alle modifiche apportate alla luminanza (luminosità) di un'immagine e meno sensibili a cromatura (Color). Suddividendo i dati dei colori in componenti di luminanza e cromatura distinti, è possibile comprimere selettivamente solo i componenti cromatura per ottenere risparmi di spazio con una perdita minima di qualità.

Una tecnica per eseguire questa operazione è detta sottocampionatura Chroma. I piani C<sub>b</sub> e c<sub>r</sub> sono sottocampionati (downscaling) in una o in entrambe le dimensioni orizzontali e verticali. Per motivi cronologici, a ogni modalità di sottocampionamento Chroma viene comunemente fatto riferimento utilizzando un rapporto in tre parti J:a: b.



| Modalità sottocampionamento | Downscaling orizzontale | Downscaling verticali | Bit per pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Include i dati Y.

Dalla tabella precedente, se si usa YC<sub>b</sub>C<sub>r</sub> per archiviare i dati di immagine non compressi, è possibile ottenere un risparmio di memoria del 25% 32 rispetto al 62,5% rispetto ai dati RGBA di bit per pixel, a seconda della modalità di campionamento secondario Chroma.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Utilizzo JPEG di YC<sub>b</sub>C<sub>r</sub>

A un livello elevato, la pipeline di decompressione JPEG è costituita dalle seguenti fasi:

1.  Eseguire la decompressione entropia (ad esempio, Huffman)
2.  Esegui dequantizzazione
3.  Esegui trasformazione coseno discreta inversa
4.  Eseguire il campionamento di crominanza sui dati C<sub>b</sub>c<sub>r</sub>
5.  Convertire i dati YC<sub>b</sub>C<sub>r</sub> in RGBA (se necessario)

Con il codec JPEG che produce i dati di YC<sub>b</sub>C<sub>r</sub> , è possibile evitare i due passaggi finali del processo di decodifica oppure rinviarli alla GPU. Oltre ai risparmi di memoria elencati nella sezione precedente, questo riduce in modo significativo il tempo complessivo necessario per decodificare l'immagine. Lo stesso risparmio si applica quando si codificano i dati YC<sub>b</sub>C<sub>r</sub> .

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Uso dei dati JPEG YC<sub>b</sub>C<sub>r</sub>

In questa sezione viene illustrato come utilizzare WIC e Direct2D per operare sui dati di YC<sub>b</sub>C<sub>r</sub> .

Per visualizzare le indicazioni fornite in questo documento, vedere l'esempio relativo alle [ottimizzazioni JPEG YCbCr in Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , che illustra tutti i passaggi necessari per decodificare e eseguire il rendering del contenuto YC<sub>b</sub>C<sub>r</sub> in un'app Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Uso delle immagini JPEG di YC<sub>b</sub>C<sub>r</sub>

La maggior parte delle immagini JPEG viene archiviata come YC<sub>b</sub>C<sub>r</sub>. Alcuni file JPEG contengono dati CMYK o in scala di grigi e non utilizzano YC<sub>b</sub>C<sub>r</sub>. Ciò significa che in genere, ma non sempre, può usare direttamente il contenuto JPEG preesistente senza alcuna modifica.

WIC e Direct2D non supportano tutte le<sub>possibili configurazioni di</sub> YC<sub>b</sub>c e il supporto di YC<sub>b</sub>c<sub>r</sub> in Direct2D dipende dall'hardware e dal driver grafici sottostanti. Per questo motivo, una pipeline di imaging generica deve essere affidabile per le immagini che non usano YC<sub>b</sub>c<sub>r</sub> (inclusi altri formati di immagine comuni come PNG o BMP) oppure nei casi in cui il supporto di YC<sub>b</sub>c<sub>r</sub> non è disponibile. Si consiglia di proteggere la pipeline di imaging basata su BGRA esistente e di abilitare YC<sub>b</sub>C<sub>r</sub> come ottimizzazione delle prestazioni, se disponibile.

### <a name="windows-imaging-component-apis"></a>API componenti Windows Imaging

WIC in Windows 8.1 aggiunge tre nuove interfacce per fornire l'accesso ai dati JPEG YC<sub>b</sub>C<sub>r</sub> .

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) è analogo a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), ad eccezione del fatto che produce pixel in una configurazione planare, inclusi i dati di YC <sub>b</sub>C <sub>r</sub> . È possibile ottenere questa interfaccia chiamando QueryInterface su un'implementazione di [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) che supporta l'accesso planare. Ciò include l'implementazione del codec JPEG di [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) , nonché [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) offre la possibilità di codificare i dati planari dei pixel, inclusi i dati di YC <sub>b</sub>C <sub>r</sub> . È possibile ottenere questa interfaccia chiamando QueryInterface sull'implementazione del codec JPEG di [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) consente a [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) di utilizzare dati planari in pixel, tra cui YC <sub>b</sub>C <sub>r</sub>, e di convertirli in un formato pixel Interleaved. Non è in grado di convertire i dati dei pixel con interfoliazione in un formato planare. È possibile ottenere questa interfaccia chiamando QueryInterface sull'implementazione di **IWICFormatConverter** fornita da Windows.

### <a name="direct2d-apis"></a>API Direct2D

Direct2D in Windows 8.1 supporta i dati in pixel planari di YC<sub>b</sub>c<sub>r</sub> con il nuovo effetto immagine YC<sub>b</sub>c<sub>r</sub> . Questo effetto fornisce la possibilità di eseguire il rendering dei dati di YC<sub>b</sub>C<sub>r</sub> . L'effetto accetta come input due interfacce [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) : una contenente i dati planari Y nel formato \_ DXGI \_ R8 \_ UNORM e l'altra che contiene dati CbCr con interfoliazione nel formato \_ \_ DXGI R8G8 \_ formato UNORM. Questo effetto viene in genere usato al posto di **ID2D1Bitmap** che contenevano dati BGRA pixel.

L'effetto immagine YC<sub>b</sub>c<sub>r</sub> deve essere usato insieme alle API WIC YC<sub>b</sub>c<sub>r</sub> che forniscono i dati di YC<sub>b</sub>c<sub>r</sub> . Questo agisce efficacemente per eseguire l'offload di parte del lavoro di decodifica dalla CPU alla GPU, dove può essere elaborato molto più rapidamente e in parallelo.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Determinazione della configurazione di YC<sub>b</sub>C<sub>r</sub> supportata

Come indicato in precedenza, l'app deve essere affidabile nei casi in cui il supporto di YC<sub>b</sub>C<sub>r</sub> non è disponibile. Questa sezione illustra le condizioni che l'app deve verificare. Se uno dei controlli seguenti ha esito negativo, l'app deve eseguire il fallback a una pipeline basata su BGRA standard.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Il componente WIC supporta l'accesso ai dati YC<sub>b</sub>C<sub>r</sub> ?

Solo il codec JPEG fornito da Windows e alcune trasformazioni WIC supportano l'accesso ai dati YC<sub>b</sub>C<sub>r</sub> . Per un elenco completo, vedere la sezione [API componenti Windows Imaging](#windows-imaging-component-apis) .

Per ottenere una delle interfacce planare YC<sub>b</sub>C<sub>r</sub> , chiamare QueryInterface sull'interfaccia originale. Questa operazione avrà esito negativo se il componente non supporta l'accesso ai dati YC<sub>b</sub>C<sub>r</sub> .

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>La trasformazione WIC richiesta è supportata per YC<sub>b</sub>C<sub>r</sub>?

Dopo aver ottenuto un [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform), è necessario prima chiamare [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Questo metodo accetta come parametri di input il set completo di trasformazioni che si vuole applicare ai dati planare YC<sub>b</sub>C<sub>r</sub> e restituisce un valore booleano che indica il supporto, nonché le dimensioni più vicine alle dimensioni richieste che possono essere restituite. È consigliabile controllare tutti e tre i valori prima di accedere ai dati pixel con [**IWICPlanarBitmapSourceTransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Questo modello è simile al modo in cui viene usato [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Il driver di grafica supporta le funzionalità necessarie per usare YC<sub>b</sub>C<sub>r</sub> con Direct2D?

Questo controllo è necessario solo se si usa l'effetto Direct2D YC<sub>b</sub>c<sub>r</sub> per il rendering del contenuto YC<sub>b</sub>c<sub>r</sub> . Direct2D archivia i dati di YC<sub>b</sub>C<sub>r</sub> usando \_ i \_ formati DXGI R8 \_ UNORM e DXGI \_ Format \_ R8G8 \_ UNORM pixel, che non sono disponibili da tutti i driver grafici.

Prima di usare l'effetto immagine YC <sub>b</sub>C <sub>r</sub> , è necessario chiamare [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) per assicurarsi che entrambi i formati siano supportati dal driver.

### <a name="sample-code"></a>Codice di esempio

Di seguito è riportato un esempio di codice che illustra i controlli consigliati. Questo esempio è stato ricavato dalle [ottimizzazioni JPEG YCbCr nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decodifica dei dati di YC<sub>b</sub>C<sub>r</sub> pixel

Se si desidera ottenere i dati di YC <sub>b</sub>C <sub>r</sub> pixel, è necessario chiamare [**IWICPlanarBitmapSourceTransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Questo metodo copia i dati pixel in una matrice di strutture [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) compilate, una per ogni piano di dati desiderato, ad esempio Y e c <sub>b</sub>c <sub>r</sub>. Un **WICBitmapPlane** contiene informazioni sui dati pixel e punta al buffer di memoria che riceverà i dati.

Se si desidera usare i dati di YC <sub>b</sub>c <sub>r</sub> pixel con altre API WIC, è necessario creare un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)configurato in modo appropriato, chiamare [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) per ottenere il buffer di memoria sottostante e associare il buffer al [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) usato per ricevere i dati YC <sub>b</sub>C <sub>r</sub> pixel. È quindi possibile usare [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) in genere.

Infine, se si desidera eseguire il rendering dei dati YC <sub>b</sub>c <sub>r</sub> in Direct2D, è necessario creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da ogni [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e utilizzarli come origine per l'effetto immagine YC <sub>b</sub>c <sub>r</sub> . WIC consente di richiedere più configurazioni planari. Quando si interopera con Direct2D è necessario richiedere due piani, uno con GUID \_ WICPixelFormat8bppY e l'altro usando GUID \_ WICPixelFormat16bppCbCr, in quanto questa è la configurazione prevista da Direct2D.

### <a name="code-sample"></a>Codice di esempio

Di seguito è riportato un esempio di codice che illustra i passaggi per decodificare ed eseguire il rendering dei dati YC<sub>b</sub>C<sub>r</sub> in Direct2D. Questo esempio è stato ricavato dalle [ottimizzazioni JPEG YCbCr nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Trasformazione dei dati di YC<sub>b</sub>C<sub>r</sub> pixel

La trasformazione dei dati di YC <sub>b</sub>C <sub>r</sub> è quasi identica alla decodifica, perché entrambi coinvolgono [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). L'unica differenza è rappresentata dall'oggetto WIC da cui è stata ottenuta l'interfaccia. Il scaler fornito da Windows, Flip rotatorio and Color Transform All supporta YC<sub>b</sub>C<sub>r</sub> Access.

### <a name="chaining-transforms-together"></a>Concatenamento di trasformazioni

WIC supporta la nozione di concatenamento di più trasformazioni. Ad esempio, è possibile creare la pipeline WIC seguente:

![diagramma di una pipeline WIC che inizia con un decodificatore JPEG.](graphics/ycbcr5.png)

È quindi possibile chiamare QueryInterface su [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) per ottenere [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La trasformazione colore può comunicare con le trasformazioni precedenti e può esporre le funzionalità di aggregazione di ogni fase della pipeline. WIC garantisce che i dati YC<sub>b</sub>C<sub>r</sub> vengano conservati nell'intero processo. Questo concatenamento funziona solo quando si usano componenti che supportano l'accesso a YC<sub>b</sub>C<sub>r</sub> .

### <a name="jpeg-codec-optimizations"></a>Ottimizzazioni del codec JPEG

Analogamente all'implementazione di decodifica del frame JPEG di [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), l'implementazione di decodifica del frame JPEG di [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) supporta la scalabilità e la rotazione del dominio DCT JPEG nativo. È possibile richiedere una potenza di due downscaling o una rotazione direttamente dal decodificatore JPEG. Ciò comporta in genere una maggiore qualità e prestazioni rispetto all'uso delle trasformazioni discrete.

Inoltre, quando si concatenano una o più trasformazioni WIC dopo il decodificatore JPEG, è possibile sfruttare la scala e la rotazione JPEG native per soddisfare l'operazione di aggregazione richiesta.

### <a name="format-conversions"></a>Conversioni di formato

Usare [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) per convertire i dati Planar YC <sub>b</sub>C <sub>r</sub> pixel in un formato pixel Interleaved, ad esempio GUID \_ WICPixelFormat32bppPBGRA. WIC in Windows 8.1 non offre la possibilità di eseguire la conversione in un formato planare YC<sub>b</sub>C<sub>r</sub> pixel.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codifica dei dati dei pixel di YC<sub>b</sub>C<sub>r</sub>

Usare [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) per codificare i dati di YC <sub>b</sub>C <sub>r</sub> pixel nel codificatore JPEG. La codifica YC <sub>b</sub>C <sub>r</sub> data **IWICPlanarBitmapFrameEncode** è simile, ma non identica, per la codifica di dati con interfoliazione con [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). L'interfaccia planare espone solo la possibilità di scrivere dati di immagini di frame planari ed è necessario continuare a usare l'interfaccia di codifica dei frame per impostare i metadati o un'anteprima e per eseguire il commit al termine dell'operazione.

Per il caso tipico, attenersi alla procedura seguente:

1.  Ottenere il [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) come di consueto. Se si vuole configurare il campionamento secondario Chroma, impostare l'opzione del codificatore [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) durante la creazione del frame.
2.  Se è necessario impostare metadati o un'anteprima, usare [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) come di consueto.
3.  QueryInterface per [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Impostare i dati di YC <sub>b</sub>C <sub>r</sub> pixel usando [**IWICPlanarBitmapFrameEncode:: WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) o [**IWICPlanarBitmapFrameEncode:: WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). A differenza delle rispettive controparti [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , è possibile fornire questi metodi con una matrice di [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) o [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) che contengono i piani di YC <sub>b</sub>C <sub>r</sub> pixel.
5.  Al termine, chiamare [**IWICBitmapFrameEncode:: commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decodifica dei dati di YC<sub>b</sub>C<sub>r</sub> pixel in Windows 10

A partire da Windows 10 Build 1507, Direct2D fornisce [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), un modo più semplice per decodificare i file JPEG in Direct2D sfruttando al tempo stesso le ottimizzazioni YC <sub>b</sub>C <sub>r</sub> . **ID2D1ImageSourceFromWic** esegue automaticamente tutte le necessarie verifiche della funzionalità YC <sub>b</sub>C <sub>r</sub> . Usa il percorso di codeoptimize ottimizzato quando possibile e usa un fallback in caso contrario. Consente inoltre nuove ottimizzazioni, ad esempio la memorizzazione nella cache delle sottoaree dell'immagine necessarie alla volta.

Per altre informazioni sull'uso di [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), vedere l' [esempio](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)dell'SDK per la regolazione della foto Direct2D.

## <a name="related-topics"></a>Argomenti correlati

* [Ottimizzazioni di YCbCr JPEG nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
