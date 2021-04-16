---
title: Compressione a blocchi
description: Viene descritto il funzionamento della compressione a blocchi e il modo in cui utilizzarlo in WIC e Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: aeb6ba9427a04f7a251a1d59062be508e4249b41
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530409"
---
# <a name="block-compression"></a>Compressione a blocchi

A partire da Windows 8.1, Direct2D supporta diversi formati pixel compressi in blocchi. Inoltre, Windows 8.1 contiene un nuovo codec di Windows Imaging Component (WIC) DDS per consentire il caricamento e l'archiviazione di immagini compresse a blocchi nel formato di file DDS. La compressione a blocchi è una tecnica che consente di ridurre la quantità di memoria grafica utilizzata dal contenuto bitmap. Usando la compressione a blocchi, l'app può ridurre il consumo di memoria e i tempi di caricamento per le stesse immagini di risoluzione. In alternativa, l'app può usare immagini di risoluzione più o superiore, pur continuando a usare lo stesso footprint di memoria della GPU.

La compressione a blocchi è stata usata dalle applicazioni Direct3D per molto tempo e con Windows 8.1 è disponibile anche per gli sviluppatori di applicazioni mainstream e Direct2D.

In questo argomento viene descritto il funzionamento della compressione dei blocchi e il modo in cui utilizzarlo in WIC e Direct2D.

## <a name="about-block-compression"></a>Informazioni sulla compressione dei blocchi

La [compressione dei blocchi](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) si riferisce a una classe di tecniche di compressione per ridurre le dimensioni della trama. Direct3D 11 supporta fino a 7 formati BC diversi a seconda del livello di funzionalità. In Windows 8.1 Direct2D introduce il supporto per i formati BC1, BC2 e BC3 disponibili in tutti i livelli di funzionalità.

### <a name="how-block-compression-works"></a>Funzionamento della compressione dei blocchi

I formati compressi in blocchi utilizzano tutti la stessa tecnica di base per ridurre lo spazio utilizzato dai dati di colore. In questa sezione viene riepilogato l'algoritmo più semplice, BC1. Per una spiegazione più dettagliata, vedere [compressione dei blocchi](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

In primo luogo, l'immagine è divisa in blocchi da 4 a 4 pixel. Ogni blocco viene compresso separatamente.

> [!Note]  
> Ciò significa che la larghezza e l'altezza di un'immagine devono essere un multiplo di 4 pixel affinché venga compresso in blocco.

 

Questa immagine di esempio mostra un blocco di pixel 4x4 all'interno di un'immagine.

![un'immagine di esempio mostra un blocco di pixel 4x4 all'interno di un'immagine.](images/dds1.png)

Successivamente, all'interno di un blocco 4 per 4, vengono selezionati due colori "Reference" e vengono codificati come valori di bit 2 16 (5 bit in rosso, 6 bit verde, 5 bit blu). La scelta di questi colori influiscono significativamente sulla qualità dell'immagine e non è semplice. Due colori intermedi vengono calcolati tramite l'interpolazione lineare tra i due colori di riferimento nello spazio colore RGB. Ciò produce un totale di 4 colori possibili differenti. a ogni colore viene assegnato un valore di indice a due bit. Si noti tuttavia che è necessario archiviare solo i due colori dell'endpoint durante la correzione dell'interpolazione.

In questa figura, i colori 0 e 3 vengono selezionati come colori "Reference" per il blocco, mentre i colori 1 e 2 vengono calcolati usando l'interpolazione lineare.

![Diagramma che mostra il calcolo di 4 valori di colore per rappresentare il blocco.](images/dds2.png)

Infine, ogni pixel nel blocco viene mappato a uno dei quattro colori calcolati in precedenza e ogni pixel viene codificato usando il valore di indice a due bit.

La quantità totale di dati usati per rappresentare questi 16 pixel è la seguente:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Ciò comporta una densità media di 4 bit per pixel. Per il confronto, il formato DXGI comune \_ \_ B8G8R8A8 \_ UNORM pixel utilizza 32 bit per pixel.

Questo diagramma mostra che ogni pixel è codificato come indice a 2 bit. L'intero blocco è codificato in 64 bit.

![calcolo di 4 valori di colore per rappresentare il blocco.](images/dds3.png)

Esistono varianti per supportare i dati Alpha e variare il numero di canali dei colori. BC6H e BC7 usano algoritmi significativamente diversi per supportare il contenuto HDR (High Dynamic Range) e migliorare la qualità dell'immagine, rispettivamente.

### <a name="directdraw-surface-dds-file-format"></a>Formato file DirectDraw Surface (DDS)

I dati compressi in blocchi vengono in genere archiviati in file di [Superficie DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) . Se si è uno sviluppatore Direct3D, è possibile che si abbia familiarità con i file DDS. Si noti che Direct2D supporta solo alcune funzionalità DDS; Per ulteriori informazioni, vedere [requisiti DDS](#dds-requirements).

### <a name="advantages-of-block-compression"></a>Vantaggi della compressione dei blocchi

I formati compressi in blocchi differiscono dai formati comuni di compressione delle immagini del settore, ad esempio JPEG, in quanto i formati BC sono supportati in modo nativo dalle GPU moderne. Ciò significa che è possibile caricare direttamente un'immagine compressa a blocchi sulla GPU senza alcuna decodifica o decompressione. I formati BC utilizzano la media da 4 a 8 bit per pixel; Se confrontato con una bitmap BGRA non compressa 32 bit per pixel, questo comporta un risparmio di memoria pari al 75% al 87,5%. Inoltre, poiché non è disponibile un passaggio di decodifica, il tempo necessario per il caricamento di un'immagine BC viene ridotto significativamente rispetto a formati quali JPEG.

### <a name="when-to-use-block-compression"></a>Quando usare la compressione a blocchi

È consigliabile usare le immagini compresse bloccate nell'app anziché altri formati, ad esempio JPEG, se si vuole ridurre il consumo di memoria delle bitmap o si vuole ridurre i tempi di decodifica e di caricamento.

Tuttavia, la compressione dei blocchi non è appropriata per tutti i casi e richiede alcuni compromessi. In primo luogo, gli algoritmi di compressione dei blocchi sono di perdita. La compressione dei blocchi funziona bene con contenuto fotografico naturale, ma può introdurre artefatti visivi indesiderati in immagini con limiti di contrasto elevato e nitidi, come le schermate generate dal computer. È necessario assicurarsi che la qualità dell'immagine del blocco delle immagini compresse sia accettabile prima di usarla.

In secondo luogo, i file DDS compressi utilizzano in genere più spazio sul disco rispetto alle immagini JPEG paragonabili. Ciò a sua volta aumenterà le dimensioni del pacchetto dell'app e i requisiti di larghezza di banda di rete.

## <a name="using-block-compression"></a>Uso della compressione a blocchi

Questa sezione illustra come generare e usare asset compressi in blocchi in un'app Direct2D.

### <a name="overview"></a>Panoramica

I file DDS compressi sono un formato ottimizzato per il runtime, ovvero sono ottimizzati in modo specifico per prestazioni ottimali in fase di esecuzione dell'app. Si consiglia di continuare a usare la pipeline di creazione e modifica degli asset esistente e di convertirla in un formato compresso a blocchi solo quando vengono importati nel progetto di applicazione o in fase di compilazione.

### <a name="dds-requirements"></a>Requisiti DDS

Il formato di file DDS è stato progettato per supportare un'ampia gamma di funzionalità usate in Direct3D. Direct2D utilizza solo un subset di queste funzionalità. Pertanto, quando si creano immagini DDS da usare con Direct2D, è necessario tenere presenti le restrizioni seguenti:

-   Sono consentiti solo i valori di [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) seguenti:
    -   \_Formato DXGI \_ BC1 \_ UNORM
    -   \_Formato DXGI \_ BC2 \_ UNORM
    -   \_Formato DXGI \_ BC3 \_ UNORM
-   È necessario utilizzare i dati alfa premoltiplicati. Sono inclusi i file DDS legacy che usano formati che definiscono in modo esplicito i valori alfa premoltiplicati (DXT1, DXT2, DXT4), nonché i file DDS che usano la \_ struttura dell'intestazione DDS \_ DX10 con i \_ \_ \_ \_ \_ \_ valori premoltiplicati per la modalità Alpha DDS e la modalità Alpha DDS.
-   Le dimensioni X e Y devono essere multipli di 4 pixel.
-   Non sono consentite trame del volume, CubeMaps, mipmap o matrici di trame. È consigliabile usare solo immagini di origine con singolo frame.

### <a name="generating-block-compressed-assets"></a>Generazione di asset compressi in blocchi

Sono disponibili diversi strumenti per la creazione di DDS per la creazione o la conversione di file DDS compressi in blocchi. Si noti che non tutti gli strumenti supportano i requisiti per l'uso di file DDS con Direct2D, come descritto nella sezione precedente.

A partire da Visual Studio 2013, è possibile fare in modo che Visual Studio converta gli asset visivi esistenti, ad esempio JPEG e PNG, nel formato compresso del blocco DDS corretto come parte automatica del processo di compilazione. Questa operazione viene eseguita usando l'istruzione di compilazione personalizzata dell'attività contenuto immagine.

Per informazioni su come configurare questa impostazione per il progetto, vedere [procedura: esportare una trama da usare con le app Direct2D o JavaScript](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).

### <a name="direct2d-apis"></a>API Direct2D

Direct2D viene aggiornato in Windows 8.1 per supportare i formati pixel seguenti:

-   \_Formato DXGI \_ BC1 \_ UNORM
-   \_Formato DXGI \_ BC2 \_ UNORM
-   \_Formato DXGI \_ BC3 \_ UNORM

Per i formati precedenti, è necessario usare l'alfa premoltiplicato. Inoltre, questi formati sono validi solo per l'utilizzo come origine, non come destinazione. Questo significa, ad esempio, che è possibile creare una bitmap Direct2D usando BC1, ma non un contesto di dispositivo.

I metodi seguenti vengono aggiornati in Windows 8.1 per supportare i formati BC:

-   [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext:: CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget:: CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap:: CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap:: CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1:: GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Si noti che [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) accetta [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) come interfaccia; Tuttavia, in Windows 8.1 WIC non supporta l'ottenimento di dati compressi di blocco da **IWICBitmapSource** e non esiste alcun formato pixel WIC corrispondente al \_ formato DXGI \_ BC1 UNORM e \_ così via. **CreateBitmapFromWicBitmap** determina invece se **IWICBitmapSource** è un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) DDS valido e carica direttamente i dati compressi del blocco. È possibile specificare in modo esplicito il formato pixel nello struct [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) oppure consentire a Direct2D di determinare automaticamente il formato corretto.

### <a name="windows-imaging-component-apis"></a>API componenti Windows Imaging

Windows Imaging Component (WIC) aggiunge un nuovo codec DDS in Windows 8.1. Inoltre, vengono aggiunte nuove interfacce che supportano l'accesso a dati specifici di DDS, inclusi i dati pixel compressi del blocco:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Blocca formati pixel WIC compressi

Non sono presenti nuovi formati di pixel compressi in blocchi WIC in Windows 8.1. Se invece si ottiene un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) dal decodificatore DDS e si chiama [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels), si riceveranno pixel standard non compressi, ad esempio WICPixelFormat32bppPBGRA. È possibile usare [**IWICDdsFrameDecode:: CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) per ottenere i dati compressi dei blocchi non elaborati sotto forma di buffer di memoria da un file DDS.

### <a name="multi-frame-dds-access"></a>Accesso DDS a più frame

Il formato di file DDS consente di archiviare più immagini correlate in un unico file. Un file DDS, ad esempio, può contenere una mappa cubi, una trama del volume o una matrice di trama, che può essere mipmap. In Direct3D queste più immagini sono esposte come sottorisorse. In WIC, più immagini sono esposte come frame ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

WIC supporta solo la nozione di una matrice unidimensionale di frame, mentre DDS supporta tre dimensioni indipendenti (anche se solo due possono essere utilizzate in un file qualsiasi). WIC fornisce metodi pratici per semplificare il mapping tra una sottorisorsa DDS e un frame WIC. Per la decodifica, [**IWICDdsDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) consente di specificare l'indice della matrice, il livello MIP e l'indice della sezione della sottorisorsa e restituisce il frame WIC corretto.

Per la codifica, [**IWICDdsEncoder:: CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) calcola l'indice della matrice risultante, il livello MIP e l'indice della sezione quando si crea un nuovo frame. È necessario avere prima chiamato [**IWICDdsEncoder:: Separameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) per definire i parametri del file specifici di DDS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: Esportare una trama da usare con app Direct2D o Javascript](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Informazioni di riferimento per DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compressione dei blocchi](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 