---
title: Compressione a blocchi
description: Descrive il funzionamento della compressione a blocchi e come usarla in WIC e Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8ee83911cc7be1ab6e611a735a7a5b3a7397c472b78e3192468d2e323ed0c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331765"
---
# <a name="block-compression"></a>Compressione a blocchi

A partire Windows 8.1, Direct2D supporta diversi formati di pixel compressi a blocchi. Inoltre, Windows 8.1 contiene un nuovo codec DDS wic (Windows Imaging Component) per consentire il caricamento e l'archiviazione di immagini compresse a blocchi nel formato di file DDS. La compressione a blocchi è una tecnica per ridurre la quantità di memoria grafica utilizzata dal contenuto bitmap. Usando la compressione a blocchi, l'app può ridurre il consumo di memoria e i tempi di caricamento per le stesse immagini di risoluzione. In caso contrario, l'app può usare più immagini con risoluzione maggiore o superiore pur continuando a usare lo stesso footprint di memoria GPU.

La compressione a blocchi è stata usata da molto tempo dalle applicazioni Direct3D e con Windows 8.1 è disponibile anche per gli sviluppatori di applicazioni Mainstream e Direct2D.

Questo argomento descrive il funzionamento della compressione a blocchi e come usarla in WIC e Direct2D.

## <a name="about-block-compression"></a>Informazioni sulla compressione a blocchi

[Per compressione a](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) blocchi si intende una classe di tecniche di compressione per ridurre le dimensioni delle trame. Direct3D 11 supporta fino a 7 formati BC diversi a seconda del livello di funzionalità. In Windows 8.1 Direct2D introduce il supporto per i formati BC1, BC2 e BC3 disponibili in tutti i livelli di funzionalità.

### <a name="how-block-compression-works"></a>Funzionamento della compressione a blocchi

I formati compressi a blocchi usano tutti la stessa tecnica di base per ridurre lo spazio utilizzato dai dati di colore. Questa sezione riepiloga l'algoritmo più semplice, BC1. Per una spiegazione più dettagliata, vedere [Compressione a blocchi.](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11)

In primo luogo, l'immagine è divisa in blocchi di 4 per 4 pixel. Ogni blocco viene compresso separatamente.

> [!Note]  
> Ciò significa che la larghezza e l'altezza di un'immagine devono essere un multiplo di 4 pixel per essere compressa in blocchi.

 

Questa immagine di esempio mostra un blocco di 4x4 pixel all'interno di un'immagine.

![Un'immagine di esempio mostra un blocco di 4x4 pixel all'interno di un'immagine.](images/dds1.png)

Successivamente, all'interno di un blocco 4 per 4, vengono selezionati due colori di "riferimento" e vengono codificati come due valori a 16 bit (rosso a 5 bit, verde a 6 bit, blu a 5 bit). La scelta di questi colori influisce in modo significativo sulla qualità dell'immagine ed è nontriviale. Due colori intermedi vengono calcolati tramite l'interpolazione lineare tra i due colori di riferimento nello spazio colore RGB. Ciò produce un totale di 4 diversi colori possibili. a ogni colore viene assegnato un valore di indice a due bit. Si noti tuttavia che solo i due colori dell'endpoint devono essere archiviati perché l'interpolazione è fissa.

In questa figura i colori 0 e 3 vengono selezionati come colori di "riferimento" per il blocco, mentre i colori 1 e 2 vengono calcolati usando l'interpolazione lineare.

![Diagramma che mostra il calcolo di 4 valori di colore per rappresentare il blocco.](images/dds2.png)

Infine, viene eseguito il mapping di ogni pixel del blocco a uno dei quattro colori calcolati in precedenza e ogni pixel viene codificato usando il valore di indice a due bit.

La quantità totale di dati usata per rappresentare questi 16 pixel è:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Il risultato è una densità media di 4 bit per pixel. Per il confronto, il formato pixel DXGI \_ FORMAT \_ B8G8R8A8 UNORM comune utilizza \_ 32 bit per pixel.

Questo diagramma mostra che ogni pixel è codificato come indice a 2 bit. L'intero blocco viene codificato a 64 bit.

![calcolando 4 valori di colore per rappresentare il blocco.](images/dds3.png)

Sono disponibili varianti per supportare i dati alfa e un numero variabile di canali di colore. BC6H e BC7 usano algoritmi significativamente diversi per supportare il contenuto HDR (High Dynamic Range) e aumentare rispettivamente la qualità delle immagini.

### <a name="directdraw-surface-dds-file-format"></a>Formato di file DDS (DirectDraw Surface)

I dati compressi a blocchi vengono in genere archiviati in file [DDS (DirectDraw Surface).](/windows/desktop/direct3ddds/dx-graphics-dds-reference) È possibile che si abbia familiarità con i file DDS se si è uno sviluppatore Direct3D. Si noti che Direct2D supporta solo determinate funzionalità DDS. Per altre informazioni, vedere [Requisiti DDS.](#dds-requirements)

### <a name="advantages-of-block-compression"></a>Vantaggi della compressione a blocchi

I formati compressi a blocchi differiscono dai formati comuni di compressione delle immagini del settore, ad esempio JPEG, in quanto i formati BC sono supportati in modo nativo dalle GPU moderne. Ciò significa che è possibile caricare direttamente un'immagine compressa in blocchi nella GPU senza decodifica o decompressione. I formati BC utilizzano in media da 4 a 8 bit per pixel; Rispetto a una tipica bitmap BGRA a 32 bit per pixel non compressa, ciò comporta un risparmio di memoria dal 75% all'87,5%. Inoltre, poiché non è presente alcun passaggio di decodifica, il tempo necessario per caricare un'immagine BC è notevolmente ridotto rispetto ai formati come JPEG.

### <a name="when-to-use-block-compression"></a>Quando usare la compressione a blocchi

È consigliabile usare immagini compresse a blocchi nell'app invece di altri formati, ad esempio JPEG, se si vuole ridurre il consumo di memoria delle bitmap o ridurre i tempi di decodifica e caricamento.

Tuttavia, la compressione dei blocchi non è appropriata per tutti i casi e richiede alcuni compromessi. In primo luogo, gli algoritmi di compressione a blocchi sono persi. La compressione a blocchi funziona bene con contenuto naturale, ma può introdurre artefatti visivi indesiderati in immagini con limiti a contrasto elevato e appuntiti, ad esempio screenshot generati dal computer. Prima di usarle, è necessario assicurarsi che gli asset di immagini compresse in blocchi siano di qualità accettabile.

In secondo piano, i file DDS compressi in blocchi in genere utilizzano più spazio su disco rispetto alle immagini JPEG confrontabili. Ciò aumenterà a sua volta le dimensioni del pacchetto dell'app e i requisiti di larghezza di banda di rete.

## <a name="using-block-compression"></a>Uso della compressione a blocchi

Questa sezione illustra come generare e usare asset compressi a blocchi in un'app Direct2D.

### <a name="overview"></a>Panoramica

I file DDS compressi a blocchi sono un formato ottimizzato per il runtime, ovvero sono ottimizzati in modo specifico per prestazioni ottimali in fase di esecuzione dell'app. È consigliabile continuare a usare la pipeline di creazione e modifica di asset esistente e convertire in un formato compresso a blocchi solo quando vengono importati nel progetto dell'applicazione o in fase di compilazione.

### <a name="dds-requirements"></a>Requisiti DDS

Il formato di file DDS è stato progettato per supportare un'ampia gamma di funzionalità usate in Direct3D. Direct2D usa solo un subset di queste funzionalità. Pertanto, quando si creano immagini DDS da usare con Direct2D, è necessario tenere presenti le restrizioni seguenti:

-   Sono consentiti [**solo i valori \_ DXGI FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) seguenti:
    -   FORMATO DXGI \_ \_ BC1 \_ UNORM
    -   FORMATO DXGI \_ \_ BC2 \_ UNORM
    -   FORMATO DXGI \_ \_ BC3 \_ UNORM
-   È necessario usare dati alfa premoltiliati. Sono inclusi i file DDS legacy che usano formati che definiscono in modo esplicito i valori alfa premoltilied (DXT1, DXT2, DXT4), nonché i file DDS che usano la struttura DDS HEADER DX10 con i valori \_ \_ \_ DDS ALPHA \_ MODE OPAQUE e \_ DDS ALPHA MODE \_ \_ \_ PREMULTIPLIED.
-   Le dimensioni X e Y devono essere multipli di 4 pixel.
-   Le trame di volume, le mappe cubi, le mipmap o le matrici di trame non sono consentite. È consigliabile usare solo immagini di origine con frame singolo.

### <a name="generating-block-compressed-assets"></a>Generazione di asset compressi in blocchi

Sono disponibili diversi strumenti di creazione DDS per creare o convertire file DDS compressi a blocchi. Si noti che non tutti gli strumenti supportano i requisiti per l'uso di file DDS con Direct2D, come descritto nella sezione precedente.

A partire da Visual Studio 2013, è possibile fare in modo che Visual Studio gli asset visivi esistenti, ad esempio JPEG e PNG, nel formato compresso a blocchi DDS corretto come parte automatica del processo di compilazione. Questa operazione viene eseguita usando l'istruzione di compilazione personalizzata Attività Contenuto immagine.

Per informazioni su come configurare questa funzionalità per il progetto, vedere Procedura: Esportare una trama per l'uso con [App Direct2D o Java.](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))

### <a name="direct2d-apis"></a>API Direct2D

Direct2D viene aggiornato in Windows 8.1 per supportare i formati pixel seguenti:

-   FORMATO DXGI \_ \_ BC1 \_ UNORM
-   FORMATO DXGI \_ \_ BC2 \_ UNORM
-   FORMATO DXGI \_ \_ BC3 \_ UNORM

Per i formati precedenti, è necessario usare alfa premoltilied. Inoltre, questi formati sono validi solo per l'uso come origine, non come destinazione. Ciò significa, ad esempio, che è possibile creare una bitmap Direct2D usando BC1, ma non un contesto di dispositivo.

I metodi seguenti vengono aggiornati in Windows 8.1 per supportare i formati BC:

-   [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget::CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Si noti [**che CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) accetta [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) come interfaccia. tuttavia in Windows 8.1 WIC non supporta il recupero di dati compressi in blocchi da **IWICBitmapSource** e non esiste alcun formato pixel WIC corrispondente a DXGI \_ FORMAT BC1 UNORM e così \_ \_ via. **CreateBitmapFromWicBitmap** determina invece se **IWICBitmapSource** è un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) DDS valido e carica direttamente i dati compressi del blocco. È possibile specificare in modo esplicito il formato pixel nello struct [**D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) o consentire a Direct2D di determinare automaticamente il formato corretto.

### <a name="windows-imaging-component-apis"></a>Windows API del componente di creazione dell'immagine

Il Windows Imaging Component (WIC) aggiunge un nuovo codec DDS in Windows 8.1. Aggiunge inoltre nuove interfacce che supportano l'accesso a dati specifici di DDS, inclusi i dati pixel compressi in blocchi:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Formati di pixel WIC compressi a blocchi

Non sono disponibili nuovi formati di pixel compressi in blocchi WIC in Windows 8.1. Se invece si ottiene un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) dal decodificatore DDS e si chiama [**CopyPixels,**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)si riceveranno pixel non compressi standard, ad esempio WICPixelFormat32bppPBGRA. È possibile usare [**IWICDdsFrameDecode::CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) per ottenere i dati compressi in blocchi non elaborati sotto forma di buffer di memoria da un file DDS.

### <a name="multi-frame-dds-access"></a>Accesso DDS multi-frame

Il formato di file DDS consente di archiviare più immagini correlate in un singolo file. Ad esempio, un file DDS può contenere una mappa cubo, una trama del volume o una matrice di trame, che possono essere tutte mipmapped. In Direct3D queste immagini multiple vengono esposte come sottorisorse. In WIC più immagini vengono esposte come frame ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) [**e IWICBitmapFrameEncode).**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)

WIC supporta solo la nozione di matrice unidimensionale di frame, mentre DDS supporta tre dimensioni indipendenti (anche se solo due possono essere usate in qualsiasi file). WIC offre metodi pratici per facilitare il mapping tra una sottorisorsa DDS e un frame WIC. Per la decodifica, [**IWICDdsDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) consente di specificare l'indice di matrice, il livello mip e l'indice di sezione della sottorisorsa e restituisce il frame WIC corretto.

Per la codifica, [**IWICDdsEncoder::CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) calcola l'indice di matrice risultante, il livello mip e l'indice della sezione quando si crea un nuovo frame. È necessario aver prima chiamato [**IWICDdsEncoder::SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) per definire i parametri di file specifici di DDS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: Esportare una trama da usare con app Direct2D o Javascript](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Informazioni di riferimento per DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compressione a blocchi](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 