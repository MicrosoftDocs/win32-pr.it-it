---
description: Il codec originale JPEG XR è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR, supportato dal codec, è progettato per la fotografia digitale di utenti e professionisti.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Panoramica del codec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316383"
---
# <a name="jpeg-xr-codec-overview"></a>Panoramica del codec JPEG XR

Il codec originale JPEG XR è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR, supportato dal codec, è progettato per la fotografia digitale di utenti e professionisti.

Il formato JPEG XR può ottenere fino al doppio dell'efficienza di compressione del formato JPEG originale, con elementi di compressione meno evidenti. Le funzionalità di JPEG XR includono:

-   Supporto per immagini monocromatiche, RGB, CMYK e n-Channel
-   formati Integer a 8, 16 e 32 bit
-   Intervallo dinamico elevato, formati a gamma ampia, con valori di colore a virgola mobile o punto fisso
-   Decodifica progressiva
-   Codifica con perdita di perdite o senza perdita di tempo con lo stesso algoritmo di compressione
-   Supporto per la decodifica delle aree di interesse per immagini di grandi dimensioni

Il formato JPEG XR viene definito nei documenti standard seguenti:

-   ITU-T T. 832: *Information Technology-JPEG XR Image Coding System-specifica di codifica immagini*
-   ISO/IEC 29199-2:2010: *Information Technology-JPEG XR Image Coding System-parte 2: specifica di codifica delle immagini*

Lo standard JPEG XR è in gran parte basato sul formato [foto HD](hdphoto-format-overview.md) , ma esistono alcune differenze tra i due formati. In Windows 8 il codec foto HD è stato aggiornato per supportare il formato JPEG XR. Il codificatore ora restituisce sempre un flusso di bit conforme a JPEG XR. Il decodificatore può decodificare le immagini JPEG XR e HD Photo.

Miglioramenti sostanziali in termini di prestazioni, in relazione al codec Photo HD, sono stati apportati al codec JPEG XR. Ad esempio, la decodifica delle immagini con risoluzione secondaria, ad esempio la generazione di anteprime, è stata migliorata, nonché la decodifica delle immagini a bassa risoluzione. È consigliabile usare il formato JPEG XR anziché il formato foto HD.

## <a name="codec-information"></a>Informazioni sui codec



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| Estensione del file | "JXR" e "WDP"                                                         |
| GUID contenitore      | **GUID \_ ContainerFormatWmp**                                            |
| GUID decodificatore        | **\_WICWMPDECODER CLSID**                                                |
| GUID codificatore        | **\_WICWMPENCODER CLSID**                                                |
| Supporto del profilo     | Il codificatore e il decodificatore supportano il profilo principale fino al livello 128. |



 

## <a name="codec-features"></a>Funzionalità di codec

### <a name="high-dynamic-range"></a>Intervallo dinamico elevato

Il formato JPEG XR supporta le immagini con intervallo dinamico elevato, usando i colori a virgola mobile o a virgola fissa. In questi formati di colore, l'intervallo numerico di un pixel è maggiore dell'intervallo visibile, quindi è possibile modificare i colori sopra o sotto l'intervallo visibile durante le fasi di elaborazione intermedia.

-   A virgola fissa: in una rappresentazione a virgola fissa, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima. Il codec JPEG XR supporta entrambi i formati a virgola fissa a 16 bit e a 32 bit. Per 16 bit, 1,0 = 0x2000h, che fornisce 13 bit per l'intervallo visibile \[ 0... 1 \] . L'intervallo totale è da-4,0 a + 3,999 e viene mappato in modo lineare. Per 32 bit, 1,0 = 0x01000000h, l'intervallo visibile è a 24 bit e l'intervallo totale è – 128 a + 127,999.
-   Virgola mobile: in una rappresentazione a virgola mobile, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima. Il codec JPEG XR supporta sia i formati a virgola mobile a 16 bit che quelli a 32 bit.

### <a name="tiles"></a>Riquadri

Un frame può essere partizionato in sottoaree rettangolari denominate *riquadri*. Un riquadro è un'area di un'immagine che contiene matrici rettangolari di macroblocchi. I riquadri consentono di decodificare le aree dell'immagine senza elaborare l'intera immagine.

Durante la codifica, selezionare il numero di riquadri impostando le proprietà **HorizontalTileSlices** e **VerticalTileSlices** . La dimensione minima del riquadro è 16 × 16 pixel. Il codificatore regola il numero di riquadri per mantenere questa restrizione. A ogni sezione è associato un overhead di archiviazione ed elaborazione, quindi è necessario considerare il numero di riquadri necessari per determinati scenari.

### <a name="image-stream-output"></a>Output del flusso di immagini

Lo standard JPEG-XR definisce due parti di un file JPEG-XR:

-   Flusso di bit dell'immagine, definito nel corpo dello standard.
-   Contenitore di immagini. Il file contiene i metadati EXIF e XMP ed è definito nell'allegato A dello standard.

È possibile, e consentito dallo standard, incorporare il flusso di immagini all'interno di un altro tipo di contenitore di file. Il codificatore supporta una modalità di solo flusso, che restituisce il flusso di bit dell'immagine non elaborata senza contenitore di immagini. Un'applicazione può archiviare il flusso di bit in un altro formato di contenitore.

Per abilitare la modalità solo flusso, impostare la proprietà **StreamOnly** .

### <a name="image-quality-settings"></a>Impostazioni qualità immagine

Diverse proprietà del codec controllano la qualità dell'immagine di output dal codificatore.

-   [ImageQuality](#imagequality) è una proprietà comune nei codec WIC. Specifica la qualità dell'immagine come singolo valore a virgola mobile da 0,0-1.0,
-   Le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) offrono maggiore controllo sulle impostazioni di qualità.

Per utilizzare le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) , impostare la proprietà [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.

Se [UseCodecOptions](#usecodecoptions) è **Variant \_ false** (**variante \_ false** è l'impostazione predefinita), il codificatore usa la proprietà [ImageQuality](#imagequality) . Il codificatore esegue il mapping del valore di ImageQuality alla [qualità](#image-quality-settings), alla [sovrapposizione](#overlap)e al [sottocampionamento](#subsampling) tramite una tabella di ricerca.

Il codificatore non supporta la proprietà **CompressionQuality** .

### <a name="compressed-domain-transcode"></a>Transcodifica del dominio compresso

Il codec JPEG XR può eseguire alcune trasformazioni di immagini senza decodificare effettivamente i dati compressi e ricodificarli. Le operazioni di dominio compresso sono molto efficienti ed evitano una perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine compressa con perdite di codice.

Sono supportate le operazioni di dominio compresso seguenti:

-   Ritagliare un'area dell'immagine.
-   Ruotare o capovolgere l'immagine.
-   Rimuovere i dati sulla frequenza per creare un file di immagine più piccolo.
-   Riorganizzare l'immagine tra l'ordine spaziale e quello di frequenza.

Il codificatore JPEG XR USA la transcodifica del dominio compresso, se possibile, quando l'immagine di origine è un'immagine JPEG XR. Quando il codificatore esegue un'operazione di dominio compresso, ignora le proprietà del codec seguenti: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[sovrapposizione](#overlap)senza [perdita di perdite](#lossless)e [qualità](#image-quality-settings). Se sono presenti le proprietà [HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) , è necessario impostarle su zero. Non è possibile modificare le dimensioni del riquadro di un'immagine come parte di una transcodifica del dominio compresso.

Nell'elenco seguente viene descritto come eseguire le trasformazioni di immagine.

-   Per ritagliare l'immagine, impostare l'area desiderata nel parametro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del metodo **WriteSource** .
-   Per ruotare o capovolgere l'immagine, impostare la proprietà [BitmapTransform](#bitmaptransform) .
-   Per eliminare i dati relativi alla frequenza nell'immagine, impostare la proprietà [ImageDataDiscard](#imagedatadiscard) . Per eliminare i dati relativi alla frequenza nel canale alfa, impostare la proprietà [AlphaDataDiscard](#alphadatadiscard) . L'eliminazione dei dati di frequenza riduce le dimensioni del file codificato e può ridurre la risoluzione.
-   Per modificare l'organizzazione delle immagini tra frequenza e ordinamento spaziale, impostare la proprietà [FrequencyOrdering](/windows) .

Per disabilitare la transcodifica del dominio compresso e forzare il codificatore a codificare nuovamente l'immagine, impostare [UseCodecOptions](#usecodecoptions) su **Variant \_ true** e impostare [CompressedDomainTranscode](#compresseddomaintranscode) su **Variant \_ false**.

## <a name="encoder-options"></a>Opzioni del codificatore

Per impostare le proprietà di codifica, utilizzare l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Nell'elenco seguente vengono specificate le opzioni del codificatore.

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Overlap](#overlap)
-   [Codifica](#progressivemode)
-   [Qualità](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Sottocampionamento](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Imposta la quantità di dati di frequenza alfa da eliminare durante una transcodifica del dominio compresso.



| Tipo di dati | VARTYPE     | Range | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_Ui1 VT** | 0 – 4   | nessuno    |



 

Questa proprietà si applica solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true** e l'immagine contiene un canale alfa planare o un canale alfa con interfoliazione; in caso contrario, viene ignorato.

Per le immagini che contengono un canale alfa planare, i valori seguenti sono validi.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | I FlexBits vengono eliminati. In questo modo si riduce arbitrariamente la qualità del canale alfa planare per l'immagine transcodificata. , senza una modifica nella risoluzione effettiva. La riduzione esatta delle dimensioni e della qualità dei file dipende da numerosi fattori e non può essere specificata esattamente.                                                                                                                                                                                           |
| 2     | La banda di dati con frequenza di passaggio superiore viene scartata, incluso FlexBits. Questo consente di ridurre in modo efficace la risoluzione del canale alfa planare per un fattore di 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco 4x4 di pixel del canale alfa. In genere, è consigliabile impostare questo valore solo quando la proprietà [ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.                            |
| 3     | Entrambe le bande di dati con frequenza superata e bassa passano, inclusa la FlexBits. Questo ffectively riduce la risoluzione del canale alfa planare per un fattore di 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni 16x16 macroblocco dei pixel del canale alfa. In genere, è consigliabile impostare questo valore solo quando la proprietà [ImageDataDiscard](#imagedatadiscard) ha lo stesso valore. |
| 4     | Il canale alfa viene eliminato completamente. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.                                                                                                                                                                                                                                                                                                                                |



 

Per le immagini che contengono un canale alfa con interfoliazione, il valore seguente è valido.



| Valore | Descrizione                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Il canale alfa viene eliminato completamente. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa. |



 

Per l'alfa con interfoliazione, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato allo stesso modo dei dati dell'immagine, in base al valore della proprietà [ImageDataDiscard](#imagedatadiscard) .

### <a name="alphaquality"></a>AlphaQuality

Imposta la qualità di compressione per l'immagine del canale alfa planare.



| Tipo di dati | VARTYPE     | Range | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_Ui1 VT** | da 1 a 255 | 1       |



 

Questa proprietà si applica quando l'immagine ha un canale alfa e la proprietà [InterleavedAlpha](#interleavedalpha) è **Variant \_ false**. Il valore 1 indica la modalità lossless. L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.

### <a name="bitmaptransform"></a>BitmapTransform

Specifica se l'immagine viene ruotata o capovolta quando viene decodificata.



| Tipo di dati | VARTYPE     | Range                                                                     | Predefinito                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **\_Ui1 VT** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Abilita o Disabilita la transcodifica del dominio compresso.



| Tipo di dati         | VARTYPE      | Predefinito           |
|-------------------|--------------|-------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANT \_ true** |



 

Per disabilitare le operazioni di dominio compresso, impostare questa proprietà su **Variant \_ false**.

### <a name="frequencyorder"></a>FrequencyOrder

Abilita la codifica in ordine di frequenza. Le implementazioni del dispositivo dei codificatori JPEG XR possono organizzare un file in ordine spaziale per ridurre la memoria necessaria durante la codifica.



| Tipo di dati         | VARTYPE      | Predefinito           |
|-------------------|--------------|-------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANT \_ true** |



 

-   **Variante \_ TRUE**: ordine di frequenza. I dati con frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla relativa frequenza anziché all'orientamento spaziale. L'organizzazione di un file in base all'ordine di frequenza offre le migliori prestazioni per qualsiasi decodifica basata sulla frequenza.
-   **Variante \_ FALSE**: ordine spaziale. L'ordine spaziale riduce la memoria necessaria durante la codifica

È consigliabile utilizzare l'ordine di frequenza, a meno che non si disponga di motivi di prestazioni o specifici dell'applicazione per utilizzare l'ordine spaziale.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Imposta il numero di riquadri orizzontali.



| Tipo di dati  | VARTYPE     | Range  | Predefinito                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **\_UI2 VT** | 0 – 4095 | (larghezza immagine-1)  >> 8 |



 

Il valore è il numero di suddivisioni orizzontali; ovvero il numero di riquadri orizzontali-1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Specifica il modo in cui il codificatore gestisce i limiti del riquadro durante una transcodifica del dominio compresso.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANTE \_ false** |



 

Questa proprietà viene applicata solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true** e viene eseguita una transcodifica dell'area secondaria di esattamente uno o più riquadri.

L'operazione predefinita per la transcodifica di un'area consiste nell'espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area. Se questa proprietà è impostata su **Variant \_ true**, il codec ignora i pixel circostanti e vengono estratti solo il riquadro o i riquadri selezionati. Se l'immagine di origine non è affiancata o se l'area richiesta include riquadri parziali, questo parametro viene ignorato.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Imposta la quantità di dati relativi alla frequenza delle immagini da eliminare durante una transcodifica del dominio compresso.



| Tipo di dati | VARTYPE     | Range | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_Ui1 VT** | 0 – 3   | 0       |



 

Questa proprietà viene applicata solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true**. in caso contrario, viene ignorata.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | I FlexBits vengono eliminati. In questo modo si riduce arbitrariamente la qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine. La riduzione esatta delle dimensioni e della qualità dei file dipende da numerosi fattori e non può essere specificata esattamente. Questo valore restituisce un errore specificato per un canale alfa con interfoliazione.                                                                                |
| 2     | La banda di dati con frequenza di passaggio superiore viene scartata, incluso FlexBits. In questo modo si riduce la risoluzione dell'immagine transcodificata in base a un fattore 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco di pixel 4x4. Pertanto, l'immagine transcodificata deve essere downsampling di conseguenza ogni volta che viene decodificata.                             |
| 3     | Entrambe le bande di dati con frequenza superata e bassa passano, inclusa la FlexBits. In questo modo si riduce la risoluzione dell'immagine transcodificata in base a un fattore pari a 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni 16x16 macroblocco di pixel. Pertanto, l'immagine transcodificata deve essere downsampling di conseguenza ogni volta che viene decodificata. |



 

Se l'immagine contiene un canale alfa Interleaved, il valore di [ImageDataDiscard](#imagedatadiscard) viene applicato al canale alfa, a meno che la proprietà [AlphaDataDiscard](#alphadatadiscard) sia impostata su 4, nel qual caso il canale alfa viene ignorato.

Per il piano alfa planare, i dati relativi alla frequenza eliminati sono controllati dalla proprietà [AlphaDataDiscard](#alphadatadiscard) .

### <a name="imagequality"></a>ImageQuality

Imposta la qualità dell'immagine.



| Tipo di dati | VARTYPE    | Range | Predefinito |
|-----------|------------|-------|---------|
| **FLOAT** | **\_R4 VT** | 0 – 1,0 | 0.9     |



 

Il livello 1,0 garantisce una compressione senza perdita di codici.

Il livello 0,0 è l'impostazione di qualità più bassa.

### <a name="interleavedalpha"></a>InterleavedAlpha

Specifica se codificare alfa o Planar con interfoliazione.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANTE \_ false** |



 

-   **Variante \_ TRUE**: Alfa Interleaved. Le informazioni sul canale alfa sono codificate come canale Interleaved aggiuntivo, senza correlazione con i canali del contenuto di immagine. Questa modalità è utile per la decodifica di alfa simultaneamente con l'immagine durante il flusso dell'immagine.
-   VARIANT \_ false: alfa planare. Un canale alfa planare viene codificato come immagine separata. I dati dell'immagine e il canale alfa vengono decodificati in modo indipendente. Facoltativamente, è possibile impostare il livello di qualità del canale alfa impostando la proprietà [AlphaQuality](#alphaquality) .

L'Alpha Interleaved è supportato solo per determinati formati pixel RGB. Planar Alpha è supportato per qualsiasi formato di immagine che definisce un canale alfa.

### <a name="lossless"></a>Lossless

Abilita la compressione delle perdite.



| Tipo di dati         | VARTYPE      | Predefinito        |
|-------------------|--------------|----------------|
| **\_bool Variant** | **\_bool VT** | VARIANTE \_ false |



 

Se il valore è **Variant \_ true**, il codificatore usa la compressione senza perdita di perdite. Se impostata su **Variant \_ true**, questa proprietà esegue l'override della proprietà [ImageQuality](#imagequality) .

### <a name="overlap"></a>Overlap

Imposta il livello di filtro di sovrapposizione. Con il filtro di sovrapposizione, i coefficienti di trasformazione vengono applicati tra i limiti Block e macroblocco. Questo può ridurre gli artefatti di blocco.



| Tipo di dati | VARTYPE     | Range | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_Ui1 VT** | 0 – 4   | 1       |



 



| Valore | Descrizione                                   |
|-------|-----------------------------------------------|
| 0     | Nessuna sovrapposizione.                                   |
| 1     | Un livello di sovrapposizione, affiancamento flessibile. (impostazione predefinita). |
| 2     | Due livelli di sovrapposizione, affiancamento flessibile.           |
| 3     | Un livello di sovrapposizione, rivestimento rigido             |
| 4     | Due livelli di sovrapposizione, disco rigido.           |



 

Definizioni:

-   Un livello di sovrapposizione: i valori codificati dei blocchi 4x4 vengono modificati in base ai blocchi adiacenti.
-   Due livelli di sovrapposizione: viene applicato il primo livello di sovrapposizione. Inoltre, i valori codificati di 16x16 macroblocchi vengono modificati in base ai macroblocchi adiacenti.
-   Affiancamento flessibile: i filtri sovrapposti vengono applicati tra i limiti del riquadro.
-   Affiancamento rigido: i filtri sovrapposti non vengono applicati tra i limiti dei riquadri. I riquadri rigidi possono introdurre alcuni artefatti visivi lungo i confini dei riquadri.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.

### <a name="progressivemode"></a>Codifica

Abilita o Disabilita la codifica progressiva.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANTE \_ false** |



 



| Valore              | Descrizione                |
|--------------------|----------------------------|
| **VARIANT \_ true**  | Modalità sequenziale (impostazione predefinita). |
| **VARIANTE \_ false** | Modalità progressiva.          |



 

### <a name="quality"></a>Qualità

Imposta la qualità di compressione.



| Tipo di dati | VARTYPE     | Range | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_Ui1 VT** | da 1 a 255 | 1       |



 

Il valore 1 indica la modalità lossless. L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.

### <a name="streamonly"></a>StreamOnly

Abilita o Disabilita la modalità di sola trasmissione.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANTE \_ false** |



 



| Valore              | Descrizione                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANT \_ true**  | Il codificatore restituisce il flusso dell'immagine non elaborata senza metadati.             |
| **VARIANTE \_ false** | Il codificatore restituisce il formato del contenitore (flusso di immagini e metadati). |



 

### <a name="subsampling"></a>Sottocampionamento

Imposta il sottocampionamento Chroma. Questa proprietà si applica solo alle immagini RGB.



| Tipo di dati | VARTYPE     | Range | Predefinito                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **\_Ui1 VT** | 0 – 3   | 3 Se [ImageQuality](#imagequality) > 0,8; in caso contrario, 1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>codifica 4:4:4. Conserva la risoluzione Chroma completa.</td>
</tr>
<tr class="even">
<td>2</td>
<td>codifica 4:2:2. La risoluzione Chroma è 1/2 della risoluzione della luminanza.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>codifica 4:2:0. La risoluzione Chroma è 1/4 della risoluzione della luminanza.</td>
</tr>
<tr class="even">
<td>0</td>
<td>Codifica 4:0:0. Elimina tutti i valori Chroma e conserva solo la luminanza.
<blockquote>
[!Note]<br />
Questa modalità non è consigliata, perché il codec usa una definizione di luminanza leggermente modificata per migliorare le prestazioni. È invece preferibile convertire l'immagine in monocromatico prima della codifica.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 e 4:2:0 conservano i dettagli della luminanza a scapito dei dettagli del colore.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.

### <a name="usecodecoptions"></a>UseCodecOptions

Specifica se utilizzare le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) invece della proprietà [ImageQuality](#imagequality) generica.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **\_bool Variant** | **\_bool VT** | **VARIANTE \_ false** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Imposta il numero di riquadri orizzontali.



| Tipo di dati  | VARTYPE     | Range  | Predefinito                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **\_UI2 VT** | 0 – 4095 | (altezza immagine-1)  >> 8 |



 

Il valore è il numero di suddivisioni verticali; ovvero il numero di riquadri verticali-1.

## <a name="supported-color-formats"></a>Formati di colore supportati

Per ulteriori informazioni su questi formati, vedere [formati di pixel nativi](-wic-codec-native-pixel-formats.md).

-   **Formati RGB Integer**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **Formati RGB a virgola fissa**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **Formati RGB a virgola mobile**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **Formati di scala di grigi**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **Formati compressi**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **Formati CMYK**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
-   **Formati N-Channel**
    -   GUID \_ WICPixelFormat32bpp4Channels
    -   GUID \_ WICPixelFormat40bpp5Channels
    -   GUID \_ WICPixelFormat48bpp6Channels
    -   GUID \_ WICPixelFormat56bpp7Channels
    -   GUID \_ WICPixelFormat64bpp8Channels
    -   GUID \_ WICPixelFormat32bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat40bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat56bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat64bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat72bpp8ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp3Channels
    -   GUID \_ WICPixelFormat64bpp4Channels
    -   GUID \_ WICPixelFormat80bpp5Channels
    -   GUID \_ WICPixelFormat96bpp6Channels
    -   GUID \_ WICPixelFormat128bpp8Channels
    -   GUID \_ WICPixelFormat64bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat80bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat96bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat112bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat128bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat144bpp8ChannelsAlpha

 

 
