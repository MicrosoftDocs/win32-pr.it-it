---
description: A partire Windows 8.1, il codec JPEG WIC (Windows Imaging Component) supporta la lettura e la scrittura di dati di immagini nel formato YCbCr nativo.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Supporto di JPEG YCbCr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f8548a458f70265d248e1d686ad3bc300d7cfee2bc1e0ab2262ee652f0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086802"
---
# <a name="jpeg-ycbcr-support"></a>Supporto di JPEG YCbCr

A partire Windows 8.1, il codec [JPEG WIC (Windows Imaging Component)](-wic-about-windows-imaging-codec.md) supporta la lettura e la scrittura di dati di immagini nel formato R nativo YC<sub>b</sub><sub>C.</sub> Il supporto di WIC YC<sub>b</sub>C<sub>r</sub> può essere usato in combinazione con [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering dei dati pixel di YC<sub>b</sub>C<sub>r</sub> con un effetto immagine. Inoltre, il codec JPEG WIC può utilizzare i dati pixel YC<sub>b</sub>C<sub>r</sub> generati da determinati driver della fotocamera tramite Media Foundation.

I dati in pixel di YC<sub>b</sub>C<sub>r</sub> consumano una quantità di memoria significativamente inferiore rispetto ai formati di pixel BGRA standard. Inoltre, l'accesso ai dati di YC<sub>b</sub>C<sub>r</sub> consente di eseguire l'offload di alcune fasi della pipeline di decodifica/codifica JPEG in Direct2D con accelerazione GPU. Usando YC<sub>b</sub>C<sub>r,</sub>l'app può ridurre il consumo di memoria JPEG e i tempi di caricamento per le stesse immagini di dimensioni e qualità. In caso contrario, l'app può usare più immagini JPEG con risoluzione più elevata senza subire penalità in termini di prestazioni.

Questo argomento descrive il funzionamento dei dati di YC<sub>b</sub>C<sub>r</sub> e come usarli in WIC e Direct2D.

-   [Informazioni su JPEG YC<sub>b</sub>C<sub>r</sub> Data](#about-jpeg-ycbcr-data)
    -   [Modello colori YC<sub>b</sub>C<sub>r</sub>](#ycbcr-color-model)
    -   [Layout di memoria planare e interleaved](#planar-versus-interleaved-memory-layouts)
    -   [Sottocampionamento chroma](#chroma-subsampling)
    -   [Utilizzo JPEG di YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Uso di JPEG YC<sub>b</sub>C<sub>r</sub> Data](#using-jpeg-ycbcr-data)
    -   [Uso di immagini JPEG<sub>YC b</sub>C<sub>r</sub>](#using-ycbcr-jpeg-images)
    -   [Windows API del componente di creazione dell'immagine](#windows-imaging-component-apis)
    -   [API Direct2D](#direct2d-apis)
    -   [Determinare se la configurazione di YC<sub>b</sub>C<sub>r</sub> è supportata](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decodifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub>](#decoding-ycbcr-pixel-data)
    -   [Trasformazione dei dati pixel di YC<sub>b</sub>C<sub>r</sub>](#transforming-ycbcr-pixel-data)
    -   [Codifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub>](#encoding-ycbcr-pixel-data)
    -   [Decodifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub> in Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Argomenti correlati](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Informazioni su JPEG YC<sub>b</sub>C<sub>r</sub> Data

Questa sezione illustra alcuni concetti chiave necessari per comprendere il funzionamento del supporto di YC<sub>b</sub>C<sub>r</sub> in WIC e i relativi vantaggi principali.

### <a name="ycsubbsubcsubrsub-color-model"></a>Modello colori YC<sub>b</sub>C<sub>r</sub>

WIC in Windows 8 e versioni precedenti supporta quattro modelli di [colore diversi,](-wic-codec-native-pixel-formats.md)il più comune dei quali è RGB/BGR. Questo modello di colore definisce i dati relativi ai colori usando componenti rosso, verde e blu. È anche possibile usare un quarto componente alfa.

Ecco un'immagine scomposti nei componenti rosso, verde e blu.

![un'immagine scomposa nei componenti rosso, verde e blu.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> è un modello di colore alternativo che definisce i dati dei colori usando un componente di luminance (Y) e due componenti di crominanza (C<sub>b</sub> e C<sub>r).</sub> Viene comunemente usato negli scenari di creazione di immagini digitali e video. Il termine YC<sub>b</sub>C<sub>r</sub> viene spesso usato in modo intercambiabile con YUV, anche se i due termini sono tecnicamente distinti.

Esistono diverse varianti di YC<sub>b</sub>C<sub>r</sub> che differiscono per lo spazio colore e le definizioni di intervalli dinamici: WIC supporta in modo specifico i dati JFIF JFIF YC<sub>b</sub>C<sub>r</sub> JPEG. Per altre informazioni, vedere la [specifica JPEG ITU-T81.](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)

Ecco un'immagine scomposa nei relativi componenti Y, C<sub>b</sub>e C<sub>r.</sub>

![un'immagine scomposa nei relativi componenti y, cb e cr.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Layout di memoria planare e interleaved

Questa sezione descrive alcune differenze tra l'accesso e l'archiviazione dei dati in pixel RGB in memoria rispetto ai dati R R di YC<sub>b</sub><sub>C.</sub>

I dati in pixel RGB vengono in genere archiviati usando un layout di memoria interleaved. Ciò significa che i dati per un singolo componente di colore vengono interfoliati tra pixel e ogni pixel viene archiviato in modo contiguo in memoria.

Di seguito è riportata una figura che mostra i dati pixel RGBA archiviati in un layout di memoria interleaved.

![Figura che mostra i dati di pixel rgba archiviati in un layout di memoria interleaved.](graphics/ycbcr3.png)

I dati di YC<sub>b</sub>C<sub>r</sub> vengono in genere archiviati usando un layout di memoria planare. Ciò significa che ogni componente del colore viene archiviato separatamente nel proprio piano contiguo, per un totale di tre piani. In un'altra configurazione comune, i componenti C<sub>b</sub> e C<sub>r</sub> sono interleaved e archiviati insieme, mentre il componente Y rimane nel proprio piano, per un totale di due piani.

Di seguito è riportata una figura che mostra i dati planari Y e I dati interleaved C<sub>b</sub>C<sub>r</sub> pixel, un layout di memoria comune di YC<sub>b</sub>C<sub>r.</sub>

![figura che mostra i dati planari y e i dati in pixel interleaved cbcr, un layout di memoria ycbcr comune.](graphics/ycbcr4.png)

Sia in WIC che in Direct2D, ogni piano colori viene considerato come un oggetto distinto [(IWICBitmapSource](-wic-imp-iwicbitmapsource.md) o [**ID2D1Bitmap)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e collettivamente questi piani formano i dati di supporto per un'immagine R YC <sub>b</sub><sub>C.</sub>

Mentre WIC supporta l'accesso ai dati di YC<sub>b</sub>C<sub>r</sub> in entrambe le configurazioni a 2 e 3 piani, Direct2D supporta solo il primo (Y e C<sub>b</sub>C<sub>r).</sub> Pertanto, quando si usano WIC e Direct2D insieme, è consigliabile usare sempre la configurazione A 2 piano<sub>YC b</sub>C<sub>r.</sub>

### <a name="chroma-subsampling"></a>Sottocampionamento chroma

Il modello a colori YC<sub>b</sub>C<sub>r</sub> è particolarmente adatto per scenari di creazione di immagini digitali perché può sfruttare determinati aspetti del sistema visivo umano. In particolare, gli esseri umani sono più sensibili ai cambiamenti nella luminosità di un'immagine e meno sensibili alla crominanza (colore). Suddividendo i dati di colore in componenti di luminance e chrominance separati, è possibile comprimere in modo selettivo solo i componenti di crominanza per ottenere un risparmio di spazio con una perdita minima di qualità.

Una tecnica per eseguire questa operazione è denominata sottocampionamento della chroma. I piani C<sub>b</sub> e C<sub>r</sub> vengono sottocampionati (ridimensionati) in una o entrambe le dimensioni orizzontale e verticale. Per motivi cronologici, ogni modalità di sottocampionamento della chroma viene comunemente definita con un rapporto J:a:b in tre parti.



| Modalità di sottocampionamento | Scalabilità orizzontale | Scalabilità verticale | Bit per pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Include i dati Y.

Dalla tabella precedente, se si usa YC<sub>b</sub>C<sub>r</sub> per archiviare dati immagine non compressi, è possibile ottenere un risparmio di memoria dal 25% al 62,5% rispetto ai dati RGBA a 32 bit per pixel, a seconda della modalità di sottocampionamento chroma usata.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Utilizzo JPEG di YC<sub>b</sub>C<sub>r</sub>

A livello elevato, la pipeline di decompressione JPEG è costituita dalle fasi seguenti:

1.  Eseguire la decompressione dell'entropia (ad esempio Huffman)
2.  Eseguire la dequantizzazione
3.  Eseguire la trasformazione del coseno discreto inverso
4.  Eseguire l'upsampling chroma sui dati C<sub>b</sub>C<sub>r</sub>
5.  Convertire i dati di YC<sub>b</sub>C<sub>r</sub> in RGBA (se necessario)

Facendo in modo che il codec JPEG produca dati YC<sub>b</sub>C<sub>r,</sub> è possibile evitare i due passaggi finali del processo di decodifica o rinviarli alla GPU. Oltre ai risparmi di memoria elencati nella sezione precedente, questo riduce significativamente il tempo complessivo necessario per decodificare l'immagine. Gli stessi risparmi si applicano quando si codificano i<sub>dati di</sub>YC b C<sub>r.</sub>

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Uso di JPEG YC<sub>b</sub>C<sub>r</sub> Data

Questa sezione illustra come usare WIC e Direct2D per operare sui dati di YC<sub>b</sub>C<sub>r.</sub>

Per visualizzare le linee guida di questo documento usate in pratica, vedere l'esempio [jpeg YCbCr optimizations in Direct2D and WIC (Ottimizzazioni di JPEG YCbCr in Direct2D e WIC)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) che illustra tutti i passaggi necessari per decodificare ed eseguire il rendering del contenuto R di YC<sub>b</sub><sub>C</sub> in un'app Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Uso di immagini JPEG<sub>YC b</sub>C<sub>r</sub>

La maggior parte delle immagini JPEG viene archiviata come YC<sub>b</sub>C<sub>r</sub>. Alcuni JPEG contengono dati CMYK o in scala di grigi e non usano YC<sub>b</sub>C<sub>r</sub>. Ciò significa che in genere, ma non sempre, è possibile usare direttamente contenuto JPEG preesistnte senza alcuna modifica.

WIC e Direct2D non supportano tutte le possibili configurazioni di YC<sub>b</sub>C<sub>r</sub> e il supporto di YC<sub>b</sub>C<sub>r</sub> in Direct2D dipende dall'hardware grafico e dal driver sottostanti. Per questo motivo, una pipeline di creazione dell'immagine per utilizzo generico deve essere affidabile per le immagini che non usano YC<sub>b</sub>C<sub>r</sub> (inclusi altri formati di immagine comuni, ad esempio PNG o BMP) o per i casi in cui il supporto di YC<sub>b</sub>C<sub>r</sub> non è disponibile. È consigliabile mantenere la pipeline di creazione dell'immagine basata su BGRA esistente e abilitare YC<sub>b</sub>C<sub>r</sub> come ottimizzazione delle prestazioni quando disponibile.

### <a name="windows-imaging-component-apis"></a>Windows API del componente di creazione dell'immagine

WIC in Windows 8.1 aggiunge tre nuove interfacce per fornire l'accesso ai dati JPEG YC<sub>b</sub>C<sub>r.</sub>

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) è analogo a [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)ad eccezione del fatto che produce pixel in una configurazione planare, inclusi i dati R di YC <sub>b</sub><sub>C.</sub> È possibile ottenere questa interfaccia chiamando QueryInterface su un'implementazione di [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) che supporta l'accesso planare. Ciò include l'implementazione del codec JPEG [**di IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) nonché [**IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICColorTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) consente di codificare dati di pixel planari, inclusi i dati R di YC <sub>b</sub><sub>C.</sub> È possibile ottenere questa interfaccia chiamando QueryInterface sull'implementazione del codec JPEG [**di IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) consente a [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) di utilizzare dati pixel planari, tra cui YC <sub>b</sub>C <sub>r,</sub>e di convertirli in un formato pixel interleaved. Non espone la possibilità di convertire i dati pixel interleaved in un formato planare. È possibile ottenere questa interfaccia chiamando QueryInterface nell'Windows'implementazione fornita di **IWICFormatConverter.**

### <a name="direct2d-apis"></a>API Direct2D

Direct2D in Windows 8.1 supporta i dati pixel planari di YC<sub>b</sub>C<sub>r</sub> con il nuovo effetto immagine YC<sub>b</sub>C<sub>r</sub> . Questo effetto consente di eseguire il rendering dei dati di YC<sub>b</sub>C<sub>r.</sub> L'effetto accetta come input due interfacce [**ID2D1Bitmap:**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) una contenente dati Y planari nel formato DXGI FORMAT R8 UNORM e una contenente dati \_ \_ \_ CbCr interleaved nel formato DXGI \_ FORMAT \_ R8G8 \_ UNORM. In genere si usa questo effetto al posto **dell'oggetto ID2D1Bitmap** che contiene dati pixel BGRA.

L'effetto immagine YC<sub>b</sub>C<sub>r</sub> deve essere usato in combinazione con le API WIC YC<sub>b</sub>C<sub>r</sub> che forniscono i dati di YC<sub>b</sub>C<sub>r.</sub> Ciò consente di eseguire l'offload di parte del lavoro di decodifica dalla CPU alla GPU, dove può essere elaborato molto più rapidamente e in parallelo.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Determinare se la configurazione di YC<sub>b</sub>C<sub>r</sub> è supportata

Come notato in precedenza, l'app deve essere affidabile nei casi in cui il supporto di YC<sub>b</sub>C<sub>r</sub> non è disponibile. Questa sezione illustra le condizioni che l'app deve verificare. Se uno dei controlli seguenti ha esito negativo, l'app deve eseguire il fall back a una pipeline standard basata su BGRA.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Il componente WIC supporta l'accesso ai dati di YC<sub>b</sub>C<sub>r?</sub>

Solo il Windows codec JPEG fornito e alcune trasformazioni WIC supportano l'accesso ai dati<sub>YC b</sub>C<sub>r.</sub> Per un elenco completo, vedere la sezione Windows [Imaging Component APIs (API](#windows-imaging-component-apis) del componente di creazione dell'immagine).

Per ottenere una delle interfacce planari YC<sub>b</sub>C<sub>r,</sub> chiamare QueryInterface sull'interfaccia originale. Questa operazione avrà esito negativo se il componente non supporta l'accesso ai dati di YC<sub>b</sub>C<sub>r.</sub>

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>La trasformazione WIC richiesta è supportata per YC<sub>b</sub>C<sub>r</sub>?

Dopo aver ottenuto un [**oggetto IWICPlanarBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)è necessario chiamare [**prima DoesSupportTransform.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform) Questo metodo accetta come parametri di input il set completo di trasformazioni da applicare ai dati planari YC<sub>b</sub>C<sub>r</sub> e restituisce un valore booleano che indica il supporto, nonché le dimensioni più vicine alle dimensioni richieste che possono essere restituite. È necessario controllare tutti e tre i valori prima di accedere ai dati pixel con [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Questo modello è simile a come [**viene usato IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Il driver di grafica supporta le funzionalità necessarie per usare YC<sub>b</sub>C<sub>r</sub> con Direct2D?

Questo controllo è necessario solo se si usa l'effetto Direct2D YC<sub>b</sub>C<sub>r</sub> per eseguire il rendering del contenuto di YC<sub>b</sub>C<sub>r.</sub> Direct2D archivia i dati YC<sub>b</sub>C<sub>r</sub> usando i formati di pixel DXGI \_ FORMAT R8 UNORM e \_ \_ DXGI \_ FORMAT \_ R8G8 \_ UNORM, che non sono disponibili in tutti i driver di grafica.

Prima di usare l'effetto immagine YC <sub>b</sub>C <sub>r,</sub> è necessario chiamare [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) per assicurarsi che entrambi i formati siano supportati dal driver.

### <a name="sample-code"></a>Codice di esempio

Di seguito è riportato un esempio di codice che illustra i controlli consigliati. Questo esempio è stato tratto dalle [ottimizzazioni JPEG YCbCr nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decodifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub>

Per ottenere i dati pixel di YC <sub>b</sub>C <sub>r,</sub> è necessario chiamare [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Questo metodo copia i dati pixel in una matrice di strutture [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) compilate, una per ogni piano di dati desiderato (ad esempio, Y e C <sub>b</sub>C <sub>r).</sub> **WiCBitmapPlane contiene** informazioni sui dati pixel e punta al buffer di memoria che riceverà i dati.

Se si vogliono usare i dati pixel di YC <sub>b</sub>C <sub>r</sub> con altre API WIC, è necessario creare un [**oggetto IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)configurato in modo appropriato, chiamare [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) per ottenere il buffer di memoria sottostante e associare il buffer al [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) usato per ricevere i dati pixel di YC <sub>b</sub>C <sub>r.</sub> È quindi possibile usare normalmente [IWICBitmap.](-wic-imp-iwicbitmapdecoder.md)

Infine, se si vuole eseguire il rendering dei dati YC <sub>b</sub>C <sub>r</sub> in Direct2D, è necessario creare un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da ogni [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e usarli come origine per l'effetto immagine YC <sub>b</sub>C <sub>r.</sub> WIC consente di richiedere più configurazioni planari. Quando si interagisce con Direct2D, è necessario richiedere due piani, uno con GUID \_ WICPixelFormat8bppY e l'altro con GUID \_ WICPixelFormat16bppCbCr, perché questa è la configurazione prevista da Direct2D.

### <a name="code-sample"></a>Codice di esempio

Di seguito è riportato un esempio di codice che illustra i passaggi per decodificare ed eseguire il rendering dei dati YC<sub>b</sub>C<sub>r</sub> in Direct2D. Questo esempio è stato tratto dalle [ottimizzazioni JPEG YCbCr nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Trasformazione dei dati pixel di YC<sub>b</sub>C<sub>r</sub>

La trasformazione dei dati di YC <sub>b</sub>C <sub>r</sub> è quasi identica alla decodifica, perché entrambe coinvolgono [**IWICPlanarBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) L'unica differenza è l'oggetto WIC da cui è stata ottenuta l'interfaccia. Il Windows scaler, il ruotatore capovolgimento e la trasformazione dei colori supportano tutti l'accesso<sub>AC b</sub>C<sub>r.</sub>

### <a name="chaining-transforms-together"></a>Concatenamento di trasformazioni

WIC supporta il concetto di concatenamento di più trasformazioni. Ad esempio, è possibile creare la pipeline WIC seguente:

![diagramma di una pipeline wic che inizia con un decodificatore jpeg.](graphics/ycbcr5.png)

È quindi possibile chiamare QueryInterface su [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) per ottenere [**IWICPlanarBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) La trasformazione colore può comunicare con le trasformazioni precedenti ed esporre le funzionalità di aggregazione di ogni fase della pipeline. WIC garantisce che i dati di YC<sub>b</sub>C<sub>r</sub> siano conservati durante l'intero processo. Questo concatenamento funziona solo quando si usano componenti che supportano l'accesso<sub>AC b</sub>C<sub>r.</sub>

### <a name="jpeg-codec-optimizations"></a>Ottimizzazioni del codec JPEG

Analogamente all'implementazione della decodifica dei fotogrammi JPEG di [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)l'implementazione della decodifica dei fotogrammi JPEG di [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) supporta il ridimensionamento e la rotazione nativi del dominio JPEG DCT. È possibile richiedere una potenza di due ridimensionamento o una rotazione direttamente dal decodificatore JPEG. Ciò comporta in genere prestazioni e qualità superiori rispetto all'uso delle trasformazioni discrete.

Inoltre, quando si concatenano una o più trasformazioni WIC dopo il decodificatore JPEG, può sfruttare il ridimensionamento e la rotazione JPEG nativi per soddisfare l'operazione di aggregazione richiesta.

### <a name="format-conversions"></a>Conversioni di formato

Usare [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) per convertire i dati planari YC <sub>b</sub>C <sub>r</sub> pixel in un formato pixel interleaved, ad esempio GUID \_ WICPixelFormat32bppPBGRA. WiC in Windows 8.1 non offre la possibilità di eseguire la conversione in un formato planare YC<sub>b</sub>C<sub>r</sub> pixel.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub>

Usare [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) per codificare i dati pixel di YC <sub>b</sub>C <sub>r</sub> nel codificatore JPEG. Encoding YC <sub>b</sub>C <sub>r</sub> data **IWICPlanarBitmapFrameEncode** is similar but not identical to encoding interleaved data using [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). L'interfaccia planare espone solo la possibilità di scrivere dati di immagine dei fotogrammi planari ed è consigliabile continuare a usare l'interfaccia di codifica dei fotogrammi per impostare i metadati o un'anteprima ed eseguire il commit al termine dell'operazione.

Nel caso tipico, è necessario seguire questa procedura:

1.  Ottenere [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) come di consueto. Se si vuole configurare il sottosampling chroma, impostare l'opzione del codificatore [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) durante la creazione del frame.
2.  Se è necessario impostare metadati o un'anteprima, eseguire questa operazione usando [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) come di consueto.
3.  QueryInterface per [**IWICPlanarBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)
4.  Impostare i dati pixel di YC <sub>b</sub>C <sub>r</sub> usando [**IWICPlanarBitmapFrameEncode::WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) o [**IWICPlanarBitmapFrameEncode::WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). A differenza delle controparti [**IWICBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) questi metodi vengono forniti con una matrice di [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) o [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) che contengono i piani YC <sub>b</sub>C <sub>r</sub> pixel.
5.  Al termine, chiamare [**IWICBitmapFrameEncode::Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decodifica dei dati pixel di YC<sub>b</sub>C<sub>r</sub> in Windows 10

A partire Windows 10 build 1507, Direct2D fornisce [**ID2D1ImageSourceFromWic,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)un modo più semplice per decodificare JPEG in Direct2D sfruttando al tempo stesso le ottimizzazioni R di YC <sub>b</sub><sub>C.</sub> **ID2D1ImageSourceFromWic** esegue automaticamente tutti i controlli delle funzionalità R di YC <sub>b</sub><sub>C</sub> necessari. usa il percorso di codice ottimizzato quando possibile e in caso contrario usa un fallback. Consente anche nuove ottimizzazioni, ad esempio la memorizzazione nella cache solo delle sottoaree dell'immagine necessarie alla volta.

Per altre informazioni sull'uso [**di ID2D1ImageSourceFromWic,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)vedere l'esempio SDK Direct2D Photo [Adjustment.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)

## <a name="related-topics"></a>Argomenti correlati

* [Ottimizzazioni di JPEG YCbCr nell'esempio Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
