---
description: Il codec XR JPEG nativo è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR supportato dal codec è progettato per la fotografia digitale consumer e professionale.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Panoramica del codec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444463"
---
# <a name="jpeg-xr-codec-overview"></a>Panoramica del codec JPEG XR

Il codec XR JPEG nativo è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR supportato dal codec è progettato per la fotografia digitale consumer e professionale.

Il formato JPEG XR può ottenere fino al doppio dell'efficienza di compressione del formato JPEG originale, con artefatti di compressione meno evidenti. Le funzionalità di JPEG XR includono:

-   Supporto per immagini monocroma, RGB, CMYK e n canali
-   Formati integer a 8, 16 e 32 bit
-   Intervallo dinamico elevato, formati wide gamut, con valori di colore a virgola fissa o a virgola mobile
-   Decodifica progressiva
-   Codifica senza perdita di dati con lo stesso algoritmo di compressione
-   Supporto per la decodifica di aree di interesse in immagini di grandi dimensioni

Il formato JPEG XR è definito nei documenti standard seguenti:

-   ITU-T T.832: *Information technology – Jpeg XR image coding system – Image coding specification*
-   ISO/IEC 29199-2:2010: *Information technology — Jpeg XR image coding system — Part 2: Image coding specification*

Lo standard JPEG XR è in gran parte basato sul formato [HD Photo,](hdphoto-format-overview.md) ma esistono alcune differenze tra i due formati. In Windows 8, il codec HD Photo è stato aggiornato per supportare JPEG XR. Il codificatore ora restituisce sempre un flusso di bit conforme a JPEG XR. Il decodificatore può decodificare immagini JPEG XR e HD Photo.

Sono stati apportati notevoli miglioramenti delle prestazioni, in relazione al codec HD Photo, al codec JPEG XR. Ad esempio, la decodifica delle immagini con risoluzione secondaria, ad esempio la generazione di anteprime, è stata migliorata, nonché la decodifica delle immagini a bassa risoluzione. È consigliabile usare il formato JPEG XR invece del formato HD Photo.

## <a name="codec-information"></a>Informazioni sui codec



|      Componente      |    Descrizione                                                          |
|---------------------|-------------------------------------------------------------------------|
| Estensione del file | "jxr" e "wdp"                                                         |
| GUID contenitore      | **GUID \_ ContainerFormatWmp**                                            |
| GUID decodificatore        | **CLSID \_ WICWmpDecoder**                                                |
| GUID del codificatore        | **CLSID \_ WICWmpEncoder**                                                |
| Supporto dei profili     | Il codificatore e il decodificatore supportano fino al profilo principale e fino al livello 128. |



 

## <a name="codec-features"></a>Funzionalità dei codec

### <a name="high-dynamic-range"></a>High Dynamic Range

JPEG XR supporta immagini a intervalli dinamici elevati, usando colori a virgola mobile o a virgola fissa. In questi formati di colore l'intervallo numerico di un pixel è maggiore dell'intervallo visibile, quindi è possibile regolare i colori al di sopra o al di sotto dell'intervallo visibile durante le fasi di elaborazione intermedie.

-   A virgola fissa: in una rappresentazione a virgola fissa, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima. Il codec JPEG XR supporta sia i formati a virgola fissa a 16 che a 32 bit. Per 16 bit, 1,0 = 0x2000h, che fornisce 13 bit per l'intervallo \[ visibile 0...1. \] L'intervallo totale è compreso tra -4,0 e +3,999 e viene mappato in modo lineare. Per 32 bit, 1,0 = 0x01000000h, l'intervallo visibile è 24 bit e l'intervallo totale è compreso tra -128 e +127,999.
-   Virgola mobile: in una rappresentazione a virgola mobile, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima. Il codec JPEG XR supporta sia i formati a virgola mobile a 16 bit che a 32 bit.

### <a name="tiles"></a>Riquadri

Un frame può essere partizionato in sottoaree rettangolari denominate *riquadri.* Un riquadro è un'area di un'immagine che contiene matrici rettangolari di macroblock. I riquadri consentono di decodificare le aree dell'immagine senza elaborare l'intera immagine.

Durante la codifica, selezionare il numero di riquadri impostando le **proprietà HorizontalTileSlices** e **VerticalTileSlices.** Le dimensioni minime del riquadro sono 16 × 16 pixel. Il codificatore regola il numero di riquadri per mantenere questa restrizione. Esiste un sovraccarico di archiviazione ed elaborazione associato a ogni riquadro, pertanto è consigliabile considerare il numero di riquadri necessari per scenari specifici.

### <a name="image-stream-output"></a>Output del flusso di immagini

Lo standard JPEG-XR definisce due parti di un file JPEG-XR:

-   Flusso di bit dell'immagine, definito nel corpo dello standard.
-   Contenitore di immagini. Il file contiene metadati Exif e XMP ed è definito nell'allegato A dello standard.

È possibile, e consentito dallo standard, incorporare il flusso di immagini all'interno di un altro tipo di contenitore di file. Il codificatore supporta una modalità solo flusso, che restituisce il flusso di bit dell'immagine non elaborata senza contenitore di immagini. Un'applicazione può archiviare il flusso di bit in un altro formato di contenitore.

Per abilitare la modalità solo flusso, impostare la **proprietà StreamOnly.**

### <a name="image-quality-settings"></a>Impostazioni di qualità dell'immagine

Diverse proprietà del codec controllano la qualità dell'immagine di output dal codificatore.

-   [ImageQuality](#imagequality) è una proprietà comune nei codec WIC. Specifica la qualità dell'immagine come singolo valore a virgola mobile compreso tra 0,0 e 1,0,
-   Le [proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling](#subsampling) offrono un maggiore controllo sulle impostazioni di qualità.

Per usare [le proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling,](#subsampling) impostare la [proprietà UseCodecOptions](#usecodecoptions) su VARIANT **\_ TRUE.**

Se [UseCodecOptions è](#usecodecoptions) **VARIANT \_ FALSE** (l'impostazione predefinita **è VARIANT \_ FALSE),** il codificatore usa la [proprietà ImageQuality.](#imagequality) Il codificatore esegue il mapping del valore di ImageQuality a [Quality,](#image-quality-settings) [Overlap](#overlap)e [Subsampling](#subsampling) tramite una tabella di ricerca.

Il codificatore non supporta la **proprietà CompressionQuality.**

### <a name="compressed-domain-transcode"></a>Transcodifica di dominio compresso

Il codec JPEG XR può eseguire determinate trasformazioni delle immagini senza decodificare effettivamente i dati compressi e ri-codificarlo. Le operazioni di dominio compresso sono molto efficienti ed evitano qualsiasi perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine compressa con perdita.

Sono supportate le operazioni di dominio compresso seguenti:

-   Ritagliare un'area dell'immagine.
-   Ruotare o capovolgere l'immagine.
-   Eliminare i dati relativi alla frequenza per creare un file di immagine più piccolo.
-   Riorganizzare l'immagine tra l'ordine spaziale e quello di frequenza.

Il codificatore JPEG XR usa la transcodella di dominio compressa, se possibile, quando l'immagine di origine è un'immagine XR JPEG. Quando il codificatore esegue un'operazione di dominio compresso, ignora le proprietà del codec seguenti: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)e [Quality.](#image-quality-settings) Se le [proprietà HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) sono presenti, è necessario impostarle su zero. Non è possibile modificare le dimensioni del riquadro di un'immagine come parte di una transcodifica di dominio compressa.

L'elenco seguente descrive come eseguire le trasformazioni delle immagini.

-   Per ritagliare l'immagine, impostare l'area desiderata nel [**parametro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del **metodo WriteSource.**
-   Per ruotare o capovolgere l'immagine, impostare la [proprietà BitmapTransform.](#bitmaptransform)
-   Per eliminare i dati relativi alla frequenza nell'immagine, impostare la [proprietà ImageDataDiscard.](#imagedatadiscard) Per eliminare i dati relativi alla frequenza nel canale alfa, impostare la [proprietà AlphaDataDiscard.](#alphadatadiscard) La rimozione dei dati relativi alla frequenza riduce le dimensioni del file codificato e può ridurre la risoluzione.
-   Per modificare l'organizzazione dell'immagine tra la frequenza e l'ordinamento spaziale, impostare la [proprietà FrequencyOrdering.](/windows)

Per disabilitare la transcodifica del dominio compresso e forzare la ricodifica dell'immagine da parte del codificatore, impostare [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE** e [impostare CompressedDomainTranscode](#compresseddomaintranscode) su **VARIANT \_ FALSE.**

## <a name="encoder-options"></a>Opzioni del codificatore

Per impostare le proprietà di codifica, usare [**l'interfaccia IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) Per altre informazioni, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).

L'elenco seguente specifica le opzioni del codificatore.

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
-   [Modalità progressiva](#progressivemode)
-   [Qualità](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Sottocampionamento](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Imposta la quantità di dati di frequenza alfa da eliminare durante la transcodifica di un dominio compresso.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | Nessuno    |



 

Questa proprietà si applica solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE** e l'immagine contiene un canale alfa planare o un canale alfa interleaved; in caso contrario, viene ignorata.

Per le immagini che contengono un canale alfa planare, sono validi i valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | I flexbit vengono eliminati. In questo modo si riduce arbitrariamente la qualità del canale alfa planare per l'immagine transcodificata. , senza alcuna modifica nella risoluzione effettiva. La riduzione esatta delle dimensioni e della qualità del file dipende da numerosi fattori e non può essere specificata esattamente.                                                                                                                                                                                           |
| 2     | La banda di dati a frequenza elevata viene eliminata, inclusi i flexbit. Ciò riduce in modo efficace la risoluzione del canale alfa planare di un fattore di 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco 4x4 di pixel del canale alfa. In genere, è consigliabile impostare questo valore solo quando la [proprietà ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.                            |
| 3     | Entrambe le bande dati con frequenza high pass e low-pass vengono eliminate, inclusi i flexbit. Questo riduce in modo ffectiva la risoluzione del canale alfa planare di un fattore di 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni macroblocco 16x16 di pixel del canale alfa. In genere, è consigliabile impostare questo valore solo quando la [proprietà ImageDataDiscard](#imagedatadiscard) ha lo stesso valore. |
| 4     | Il canale alfa viene eliminato completamente. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.                                                                                                                                                                                                                                                                                                                                |



 

Per le immagini che contengono un canale alfa interleaved, il valore seguente è valido.



| Valore | Descrizione                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Il canale alfa viene eliminato completamente. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa. |



 

Per i valori alfa interleaved, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato come i dati dell'immagine, in base al valore della [proprietà ImageDataDiscard.](#imagedatadiscard)

### <a name="alphaquality"></a>AlphaQuality

Imposta la qualità di compressione per l'immagine del canale alfa planare.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

Questa proprietà si applica quando l'immagine ha un canale alfa e la [proprietà InterleavedAlpha](#interleavedalpha) è **VARIANT \_ FALSE.** Il valore 1 indica la modalità senza perdita di dati. L'aumento dei valori comporta rapporti di compressione più elevati e una qualità dell'immagine inferiore.

### <a name="bitmaptransform"></a>BitmapTransform

Specifica se l'immagine viene ruotata o capovolta quando viene decodificata.



| Tipo di dati | VARTYPE     | Intervallo                                                                     | Predefinito                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **VT \_ UI1** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Abilita o disabilita la transcoding di domini compressi.



| Tipo di dati         | VARTYPE      | Predefinito           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

Per disabilitare le operazioni di dominio compresso, impostare questa proprietà su **VARIANT \_ FALSE.**

### <a name="frequencyorder"></a>FrequencyOrder

Abilita la codifica nell'ordine di frequenza. Le implementazioni dei dispositivi dei codificatori JPEG XR possono organizzare un file in ordine spaziale per ridurre la memoria necessaria durante la codifica.



| Tipo di dati         | VARTYPE      | Predefinito           |
|-------------------|--------------|-------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ TRUE** |



 

-   **VARIANT \_ TRUE:** ordine della frequenza. I dati con la frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla frequenza anziché all'orientamento spaziale. L'organizzazione di un file in base all'ordine di frequenza offre prestazioni ottimali per qualsiasi decodifica basata sulla frequenza.
-   **VARIANT \_ FALSE:** ordine spaziale. L'ordine spaziale riduce la memoria necessaria durante la codifica

L'ordine di frequenza è consigliato a meno che non si abbia un motivo specifico per le prestazioni o l'applicazione per usare l'ordine spaziale.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Imposta il numero di riquadri orizzontali.



| Tipo di dati  | VARTYPE     | Intervallo  | Predefinito                      |
|------------|-------------|--------|------------------------------|
| **Ushort** | **Interfaccia utente \_ VT 2** | 0–4095 | (larghezza immagine - 1) >> 8 |



 

Il valore è il numero di suddivisioni orizzontali. cio, il numero di riquadri orizzontali - 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Specifica il modo in cui il codificatore gestisce i limiti del riquadro durante una transcodifica di dominio compressa.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

Questa proprietà viene applicata solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE** e viene eseguita una transcodifica di sottoarea di esattamente uno o più riquadri.

L'operazione predefinita per una transcodifica di area è espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area. Se questa proprietà è impostata su **VARIANT \_ TRUE,** il codec ignora i pixel circostanti e vengono estratti solo il riquadro o i riquadri selezionati. Se l'immagine di origine non è affiancata o se l'area richiesta include riquadri parziali, questo parametro viene ignorato.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Imposta la quantità di dati di frequenza delle immagini da eliminare durante la transcodifica di un dominio compresso.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 0       |



 

Questa proprietà si applica solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE;** in caso contrario, viene ignorata.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | I flexbit vengono eliminati. In questo modo si riduce arbitrariamente la qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine. La riduzione esatta delle dimensioni e della qualità del file dipende da numerosi fattori e non può essere specificata esattamente. Questo valore restituisce un errore specificato per un canale alfa interleaved.                                                                                |
| 2     | La banda di dati a frequenza elevata viene eliminata, inclusi i flexbit. In questo modo si riduce la risoluzione dell'immagine transcodificata di un fattore 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco di pixel 4x4. Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata.                             |
| 3     | Entrambe le bande di dati con frequenza high pass e low-pass vengono eliminate, inclusi i flexbit. In questo modo si riduce la risoluzione dell'immagine transcodificata di un fattore di 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni macroblock di pixel 16x16. Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata. |



 

Se l'immagine contiene un canale alfa interleaved, il valore di [ImageDataDiscard](#imagedatadiscard) viene applicato al canale alfa a meno che la proprietà [AlphaDataDiscard](#alphadatadiscard) non sia impostata su 4, nel qual caso il canale alfa viene eliminato.

Per il valore alfa planare, i dati di frequenza che vengono eliminati sono controllati dalla [proprietà AlphaDataDiscard.](#alphadatadiscard)

### <a name="imagequality"></a>ImageQuality

Imposta la qualità dell'immagine.



| Tipo di dati | VARTYPE    | Intervallo | Predefinito |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0–1.0 | 0.9     |



 

Il livello 1.0 offre una compressione matematicamente senza perdita di dati.

Livello 0.0 è l'impostazione di qualità più bassa.

### <a name="interleavedalpha"></a>InterleavedAlpha

Specifica se codificare alfa interleaved o alfa planare.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

-   **VARIANT \_ TRUE:** alfa interleaved. Le informazioni sul canale alfa vengono codificate come canale interleaved aggiuntivo, senza correlazione con i canali di contenuto dell'immagine. Questa modalità è utile per decodificare alfa contemporaneamente all'immagine quando l'immagine è in streaming.
-   VARIANT \_ FALSE: alfa planare. Un canale alfa planare viene codificato come immagine separata. I dati dell'immagine e il canale alfa vengono decodificati in modo indipendente. Facoltativamente, è possibile impostare il livello di qualità del canale alfa impostando la [proprietà AlphaQuality.](#alphaquality)

L'alfa interfoliato è supportato solo per determinati formati di pixel RGB. Planare alpha è supportato per qualsiasi formato di immagine che definisce un canale alfa.

### <a name="lossless"></a>Lossless

Abilita la compressione delle perdite.



| Tipo di dati         | VARTYPE      | Predefinito        |
|-------------------|--------------|----------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | VARIANT \_ FALSE |



 

Se il valore è **VARIANT \_ TRUE,** il codificatore usa la compressione senza perdita di dati. Se impostata **su VARIANT \_ TRUE,** questa proprietà esegue l'override [della proprietà ImageQuality.](#imagequality)

### <a name="overlap"></a>Overlap

Imposta il livello di filtro di sovrapposizione. Con il filtro di sovrapposizione, i coefficienti di trasformazione vengono applicati attraverso i limiti dei blocchi e dei macroblock. Ciò può ridurre gli artefatti di blocco.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 0–4   | 1       |



 



| Valore | Descrizione                                   |
|-------|-----------------------------------------------|
| 0     | Nessuna sovrapposizione.                                   |
| 1     | Un livello di sovrapposizione, soft-tiling. (impostazione predefinita). |
| 2     | Due livelli di sovrapposizione, soft-tiling.           |
| 3     | Un livello di sovrapposizione, tinte rigide             |
| 4     | Due livelli di sovrapposizione, hard-tiling.           |



 

Definizioni:

-   Un livello di sovrapposizione: i valori codificati dei blocchi 4x4 vengono modificati in base ai blocchi adiacenti.
-   Due livelli di sovrapposizione: viene applicato il primo livello di sovrapposizione. Inoltre, i valori codificati dei macroblock 16x16 vengono modificati in base ai macroblock adiacenti.
-   Affiancamento a soffio: il filtro delle sovrapposizioni viene applicato tra i limiti del riquadro.
-   Hard-tiling: il filtro di sovrapposizione non viene applicato tra i limiti del riquadro. I riquadri rigidi possono introdurre alcuni artefatti visivi lungo i limiti dei riquadri.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**

### <a name="progressivemode"></a>Modalità progressiva

Abilita o disabilita la codifica progressiva.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Valore              | Descrizione                |
|--------------------|----------------------------|
| **VARIANT \_ TRUE**  | Modalità sequenziale (impostazione predefinita). |
| **VARIANT \_ FALSE** | Modalità progressiva.          |



 

### <a name="quality"></a>Qualità

Imposta la qualità di compressione.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito |
|-----------|-------------|-------|---------|
| **UCHAR** | **VT \_ UI1** | 1–255 | 1       |



 

Il valore 1 indica la modalità senza perdita di dati. L'aumento dei valori comporta rapporti di compressione più elevati e una qualità dell'immagine inferiore.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**

### <a name="streamonly"></a>StreamOnly

Abilita o disabilita la modalità solo flusso.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 



| Valore              | Descrizione                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | Il codificatore restituisce il flusso di immagini non elaborato senza metadati.             |
| **VARIANT \_ FALSE** | Il codificatore restituisce il formato del contenitore (flusso di immagini e metadati). |



 

### <a name="subsampling"></a>Sottocampionamento

Imposta il sottocampionamento della chroma. Questa proprietà si applica solo alle immagini RGB.



| Tipo di dati | VARTYPE     | Intervallo | Predefinito                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **VT \_ UI1** | 0–3   | 3 se [ImageQuality](#imagequality) > 0.8; in caso contrario, 1 |



 



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
<td>Codifica 4:4:4. Mantiene la risoluzione chroma completa.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Codifica 4:2:2. La risoluzione della luminazione è di 1/2.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>Codifica 4:2:0. La risoluzione della luminazione è di 1/4.</td>
</tr>
<tr class="even">
<td>0</td>
<td>Codifica 4:0:0. Rimuove tutti i valori chroma e mantiene solo la luminance.
<blockquote>
[!Note]<br />
Questa modalità non è consigliata perché il codec usa una definizione di luminance leggermente modificata per migliorare le prestazioni. È invece meglio convertire l'immagine in monocromatica prima della codifica.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 e 4:2:0 conservano i dettagli della luminazione a scapito dei dettagli del colore.

Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**

### <a name="usecodecoptions"></a>UseCodecOptions

Specifica se usare le [proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling](#subsampling) anziché la [proprietà ImageQuality](#imagequality) generica.



| Tipo di dati         | VARTYPE      | Predefinito            |
|-------------------|--------------|--------------------|
| **VARIANT \_ BOOL** | **VT \_ BOOL** | **VARIANT \_ FALSE** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Imposta il numero di riquadri orizzontali.



| Tipo di dati  | VARTYPE     | Intervallo  | Predefinito                       |
|------------|-------------|--------|-------------------------------|
| **Ushort** | **Interfaccia utente \_ VT 2** | 0–4095 | (altezza immagine - 1) >> 8 |



 

Il valore è il numero di suddivisioni verticali. cio, il numero di riquadri verticali - 1.

## <a name="supported-color-formats"></a>Formati di colore supportati

Per altre informazioni su questi formati, vedere [Native Pixel Formats](-wic-codec-native-pixel-formats.md).

-   **Formati RGB integer**
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
-   **Formati in scala di grigi**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **Formati imballati**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **Formati CMYK**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
-   **Formati a N canali**
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
    -   GUID \_ WICPixelFormat1444bpp8ChannelsAlpha

 

 
