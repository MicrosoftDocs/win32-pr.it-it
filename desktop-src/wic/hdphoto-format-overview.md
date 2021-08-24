---
description: Questo argomento fornisce informazioni sul codec HD Photo nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Panoramica del formato foto HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 772c295051186069dd7be1a3efa3bfbb4e6ea919b2ab9fbe77ffd52cad1676a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881951"
---
# <a name="hd-photo-format-overview"></a>Panoramica del formato foto HD

Questo argomento fornisce informazioni sul codec HD Photo nativo disponibile tramite Windows Imaging Component (WIC).

> [!IMPORTANT]
>
> Il formato HD Photo è un'implementazione pre-standard del formato JPEG XR. Il formato JPEG XR è stato completamente implementato in Windows 8. Per altre [informazioni, vedere Jpeg XR Codec Overview](jpeg-xr-codec.md) (Panoramica del codec JPEG XR).

 

In questo argomento sono contenute le sezioni seguenti.

-   [Codec Identity](#codec-identity)
-   [Encoding](#encoding)
    -   [Opzioni del codificatore](#encoder-options)
-   [Decodifica](#decoding)
    -   [Supporto di IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Codec Identity

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|   Componente            | Descrizione                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Nomi formali         | HD Photo, Windows Media Photo                                                   |
| Estensioni di file | Wdp                                                                             |
| tipo MIME              | image/vnd.ms-photo                                                              |
| Firme di file      | Primi quattro byte: 0x4949bc00 (versione 0; versione non definitiva), 0x4949bc01 (versione 1.0) |



 

La tabella seguente elenca i GUID usati per identificare i componenti nativi del codec HD Photo.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Decodificatore          | CLSID \_ WICWmpDecoder     | a26cec36-234c-4950-ae16e34aace71d0d |
| Codificatore          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec di formato immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)

Il codec HD Photo usa entrambe le opzioni WIC di base e offre diverse opzioni di codifica specifiche di HD Photo. La tabella seguente elenca le opzioni del codificatore supportate dal codec HD Photo nativo.

Opzioni di base del codificatore WIC

| Nome della proprietà | VARTYPE | Gamma valori | Valore predefinito |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0 - 1.0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | VT \_ UI1 | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Opzioni del codificatore specifico di foto HD

| Nome della proprietà | VARTYPE | Gamma valori | Valore predefinito |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [Qualità](#quality-option) | VT \_ UI1 | 1 - 255 | 10 |
| [Overlap](#overlap-option) | VT \_ UI1 | 0 - 2 | 1 |
| [Sottocampionamento](#subsampling-option) | VT \_ UI1 | 0 - 3 | 3 se ImageQuality > 0.8; in caso contrario, 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | Interfaccia utente \_ VT2 | 0 - 4095 | (larghezza immagine - 1) >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | Interfaccia utente \_ VT2 | 0 - 4095 | (altezza immagine - 1) >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ BOOL | **TRUE,** **FALSE** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | VT \_ UI1 | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ BOOL | **TRUE,** **FALSE** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | VT \_ UI1 | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | VT \_ UI1 | 0 - 4 | non usata. |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ BOOL | **TRUE,** **FALSE** | **FALSE** |


Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.

### <a name="imagequality-option"></a>Opzione ImageQuality

Specifica la fedeltà dell'immagine desiderata. 0.0 indica la fedeltà più bassa possibile e 1.0 specifica la massima fedeltà. Per il formato immagine HD Photo, un valore 1.0 comporta una compressione matematicamente senza perdita.

Il valore predefinito è 0,9.

### <a name="compressionquality-option"></a>Opzione CompressionQuality

Specifica la qualità di compressione desiderata. 0.0 indica lo schema di compressione efficiente disponibile. In genere, questo schema produce una codifica più veloce ma un output più grande. Il valore 1.0 specifica lo schema di compressione più efficiente disponibile, che in genere produce una codifica più lunga ma un output più piccolo.

HD Photo non supporta questa opzione del codificatore. Questo valore viene ignorato se presente nell'elenco di parametri [**IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))

### <a name="lossless-option"></a>Opzione senza perdita di dati

Specifica se utilizzare la modalità di compressione delle perdite. Per il formato immagine HD Photo, questo valore esegue l'override [del valore dell'opzione ImageQuality.](#imagequality-option)

Il valore predefinito è **FALSE.**

### <a name="bitmaptransform-option"></a>Opzione BitmapTransform

Specifica la modalità di trasformazione dell'immagine durante la decodifica dell'immagine. È necessario impostare questa opzione su uno dei valori di [**enumerazione WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

Il valore predefinito è [**WICBitmapTransformOptions::WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>Opzione UseCodecOptions

Se il valore è VARIANT \_ TRUE, [le opzioni Quality](#quality-option), [Overlap](#overlap-option)e [Subsampling](#subsampling-option) invece del valore dell'opzione .

Il valore predefinito è **FALSE.**

### <a name="quality-option"></a>Opzione Di qualità

Specifica la qualità di compressione per l'immagine. Il valore 1 indica la modalità senza perdita di dati. L'aumento dei valori comporta un rapporto di compressione più elevato e una qualità dell'immagine inferiore.

Il valore predefinito è 10.

### <a name="overlap-option"></a>Opzione Di sovrapposizione

Specifica il livello di elaborazione della sovrapposizione.

Nella tabella seguente sono elencati i livelli di elaborazione delle sovrapposizioni disponibili.



| Valore | Descrizione                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nessuna elaborazione della sovrapposizione attivata.                                                                                                                                                           |
| 1     | È abilitato un livello di elaborazione della sovrapposizione, modificando i valori codificati in blocchi 4x4 in base ai valori dei blocchi adiacenti.                                                                       |
| 2     | Sono attivati due livelli di elaborazione della sovrapposizione. Oltre all'elaborazione di primo livello, i valori codificati dei blocchi macro 16x16 vengono modificati in base ai valori dei blocchi macro adiacenti. |



 

Il valore predefinito è 1.

### <a name="subsampling-option"></a>Opzione di sottocampionamento

Specifica una compressione aggiuntiva nello spazio chroma. In questo modo, è possibile mantenere i dettagli della luminanza a scapito dei dettagli dei colori. Questa opzione si applica solo alle immagini RGB.

Nella tabella seguente sono elencate le opzioni di subsampling disponibili.



| Valore | Descrizione                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | La codifica 4:4:4 mantiene la risoluzione chroma completa.                                                                                                                                                                                                                                            |
| 2     | La codifica 4:2:2 riduce la risoluzione della chroma a 1/2 della risoluzione della luminanza.                                                                                                                                                                                                                      |
| 1     | La codifica 4:2:0 riduce la risoluzione della chroma a 1/4 di risoluzione della luminanza.                                                                                                                                                                                                                      |
| 0     | La codifica 4:0:0 rimuove tutto il contenuto di chroma e mantiene solo la luminanza. Poiché il codec usa una definizione di luminance leggermente modificata per migliorare le prestazioni, è consigliabile convertire un'immagine RGB in monocromatica prima della codifica anziché usare questa modalità di sottocampionamento chroma. |



 

Il valore predefinito è 3 se [ImageQuality](#imagequality-option) > 0,8; in caso contrario, 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>Opzioni HorizontalTileSlices, VerticalTileSlices

Specificare il tiling orizzontale e verticale dell'immagine prima di eseguire la codifica di compressione per ottenere prestazioni ottimali della decodifica dell'area . Dividendo l'immagine in riquadri rettangolari durante la codifica, è possibile decodificare le aree dell'immagine senza elaborare l'intero flusso di dati compressi. Il valore predefinito 0 non specifica alcuna suddivisione, quindi l'intera immagine viene considerata come un singolo riquadro. Il valore 1 per ogni parametro crea una singola divisione orizzontale e una singola divisione verticale, dividendo in modo efficace l'immagine in quattro riquadri di dimensioni uguali. Il valore massimo di 4095 per ogni parametro divide l'immagine in 4096 righe del riquadro con 4096 riquadri per riga. In altre parole, i valori dei parametri sono uguali al numero di riquadri orizzontali e verticali (rispettivamente) meno 1. Un riquadro non può mai essere inferiore a 16 pixel in larghezza o altezza, quindi il codificatore HD Photo potrebbe modificare questo parametro per mantenere le dimensioni minime richieste del riquadro. Poiché a ogni riquadro sono associati costi di archiviazione ed elaborazione, è consigliabile scegliere questi valori con attenzione per soddisfare lo scenario specifico.

[HorizontalTileSlices:](/windows)il valore predefinito è (Larghezza immagine - 1) >> 8.

[VerticalTileSlices:](/windows)il valore predefinito è (Altezza immagine - 1) >> 8.

### <a name="frequencyorder-option"></a>Opzione FrequencyOrder

Specifica che l'immagine deve essere codificata nell'ordine di frequenza. I dati sulla frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla frequenza anziché all'orientamento spaziale. L'organizzazione di un file in base all'ordine di frequenza offre prestazioni ottimali per qualsiasi decodifica basata sulla frequenza, pertanto è consigliabile. Le implementazioni dei dispositivi dei codificatori HD Photo possono organizzare un file in ordine spaziale per ridurre il footprint di memoria necessario durante la codifica.

Il valore predefinito è **TRUE** ed è consigliabile che le applicazioni e i dispositivi usino sempre l'ordine di frequenza, a meno che non si abbia un motivo specifico per le prestazioni o l'uso dell'ordine spaziale.

### <a name="interleavedalpha-option"></a>Opzione InterleavedAlpha

L'impostazione di questa opzione su **TRUE** indica al codec di codificare le informazioni del canale alfa come canale interleaved aggiuntivo, senza correlazione con i canali di contenuto dell'immagine. Questa modalità è utile quando è necessario decodificare alpha contemporaneamente con l'immagine in uno scenario di streaming.

L'impostazione di questo parametro su **FALSE** comporta un canale alfa planare, codificato come immagine separata con il proprio valore qualitativo facoltativo. Usando un canale alfa planare è possibile decodificare i dati dell'immagine e il canale alfa in modo indipendente. I canali alfa interleaved sono supportati solo per determinati formati di pixel RGB. È possibile associare un canale alfa planare a qualsiasi formato di immagine che definisce un canale alfa.

Il valore predefinito è **FALSE.**

### <a name="alphaquality-option"></a>Opzione AlphaQuality

Specifica la qualità di compressione per l'immagine del canale alfa planare. Il valore 1 imposta la modalità senza perdita di dati. L'aumento dei valori comporta un rapporto di compressione più elevato e una qualità dell'immagine inferiore.

Il valore predefinito è 1.

### <a name="compresseddomaintranscode-option"></a>Opzione CompressedDomainTranscode

Con HD Photo è possibile eseguire una serie di operazioni di trasformazione dei file senza decodificare effettivamente i dati compressi e ri-codificarlo nel file di destinazione. Le operazioni di dominio compresso sono molto efficienti ed evitano qualsiasi perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine con perdita di dati.

Sono supportate le operazioni di dominio compresso seguenti:

-   Ritagliare un'area dell'immagine.
-   Eseguire una trasformazione di rotazione/capovolgimento.
-   Eliminare i dati relativi alla frequenza (rendendo possibile la creazione di un file di immagine più piccolo).
-   Riorganizzare l'immagine tra ordine sequenziale spaziale e frequenza.

Il codificatore HD Photo esegue un'operazione di transcodifica di dominio compresso quando codifica un'immagine HD Photo usando un decodificatore HD Photo come origine dell'immagine. A seconda delle opzioni di codifica selezionate, il codec usa un'operazione di dominio compresso, se possibile. Se un'applicazione sceglie di impedire in modo esplicito qualsiasi operazione di transcodifica di dominio compresso, è necessario impostare l'opzione *UseCodecOptions* su **TRUE** e l'opzione *CompressedDomainTranscode* su **FALSE.**

Quando il codec esegue un'operazione di dominio compresso, sono consentite solo determinate impostazioni di proprietà e parametri del codificatore.

-   Le opzioni del codificatore di base [ImageQuality,](#imagequality-option) [CompressionQuality](/windows) [e Lossless](#lossless-option) vengono ignorate.
-   Le opzioni del codificatore HD Photo specifiche [di Quality,](#quality-option) [Overlap,](#overlap-option) [InterleavedAlpha](#interleavedalpha-option) e [AlphaQuality](#alphaquality-option) vengono ignorate.
-   Se presenti, [le opzioni HorizontalTileSlices](/windows) [e VerticalTileSlices](/windows) devono essere impostate su zero. Le dimensioni del riquadro di un'immagine non possono essere modificate come parte di una transcodifica di dominio compressa.
-   È possibile modificare l'organizzazione dell'immagine tra frequenza e ordinamento spaziale specificando il valore appropriato delle [opzioni FrequencyOrdering.](/windows)
-   È possibile eseguire un'operazione di rotazione cardinale e/o capovolgimento orizzontale/verticale in base al valore specificato nell'opzione del codificatore [BitmapTransform.](#bitmaptransform-option)
-   L'immagine può essere ritagliata specificando l'area desiderata usando il [**parametro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del metodo del codificatore **WriteSource.**
-   I dati immagine e/o alfa possono essere eliminati specificando i valori appropriati nelle opzioni [ImageDataDiscard](#imagedatadiscard-option) e/o [AlphaDataDiscard,](#alphadatadiscard-option) riducendo le dimensioni del file codificato e riducendo in modo efficace la risoluzione della nuova immagine.

Il valore predefinito è **TRUE** ed è consigliabile che le applicazioni e i dispositivi usino sempre l'ordine di frequenza, a meno che non si abbia un motivo specifico per le prestazioni o l'applicazione per usare l'ordine spaziale.

### <a name="imagedatadiscard-option"></a>Opzione ImageDataDiscard

Questo parametro è valido solo se [l'opzione CompressedDomainTranscode](#compresseddomaintranscode-option) è **TRUE.** in caso contrario, viene ignorato. [ImageDataDiscard specifica la](#imagedatadiscard-option) quantità di dati immagine da eliminare durante una transcodifica di dominio compressa. Se l'immagine contiene un canale alfa interleaved, questa eliminazione dei dati si applica anche al canale alfa, con le eccezioni descritte più avanti in questa sezione.

Sono consentiti i valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | I FlexBit vengono eliminati, con una riduzione arbitraria della qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine. La riduzione esatta delle dimensioni dei file o la riduzione della qualità specifica dipende da numerosi fattori e non possono essere specificati o stimati. Questo valore restituirà un errore se viene specificato per un canale alfa interleaved.                                                    |
| 2     | La banda di dati di frequenza HighPass viene eliminata (che include anche i FlexBit), riducendo in modo efficace la risoluzione dell'immagine transcodificata di un fattore di 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma perdono tutti i dettagli in ogni blocco di pixel 4x4. Pertanto, è consigliabile eseguire il down-sample dell'immagine transcodificata di conseguenza ogni volta che la si decodifica.                            |
| 3     | Entrambe le bande di dati di frequenza HighPass e LowPass vengono eliminate (che include anche i FlexBit), riducendo in modo efficace la risoluzione dell'immagine transcodificata di un fattore di 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma perdono tutti i dettagli in ogni macroblock di pixel 16x16. Pertanto, è consigliabile eseguire il down-sample dell'immagine transcodificata di conseguenza ogni volta che la si decodifica. |



 

Il valore predefinito è 0.

### <a name="alphadatadiscard-option"></a>Opzione AlphaDataDiscard

Questa opzione è valida solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode-option) è **TRUE** e l'immagine contiene un canale alfa planare o interleaved. in caso contrario, viene ignorato. Specifica la quantità di dati di frequenza alfa da eliminare durante la transcodifica di un dominio compresso. Per un canale alfa planare sono consentiti i valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | I FlexBit vengono eliminati, con una riduzione arbitraria della qualità del canale alfa planare per l'immagine transcodificata senza modificare la risoluzione effettiva. La riduzione esatta delle dimensioni dei file o la riduzione della qualità specifica dipende da numerosi fattori e non possono essere specificati o stimati.                                                                                                                                                                                                                                                |
| 2     | La banda di dati della frequenza HighPass viene eliminata (che include anche i FlexBit), riducendo in modo efficace la risoluzione del canale alfa planare dell'immagine transcodificata di un fattore di 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli del canale alfa planare in ogni blocco di pixel 4x4. Pertanto, l'immagine transcodificata deve essere campionata di conseguenza ogni volta che viene decodificata. In genere, è consigliabile impostare questo valore solo quando si imposta la proprietà ImageDataDiscard sullo stesso valore. |
| 3     | Entrambe le bande di dati di frequenza HighPass e LowPass vengono eliminate (che include anche i FlexBit), riducendo in modo efficace la risoluzione dell'immagine transcodificata di un fattore di 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni macroblock di pixel 16x16. Pertanto, l'immagine transcodificata deve essere campionata di conseguenza ogni volta che viene decodificata. In genere, è consigliabile impostare questo valore solo quando si imposta la proprietà ImageDataDiscard sullo stesso valore.               |
| 4     | Il canale Alpha viene completamente eliminato. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Per le immagini che contengono canali alfa interleaved, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato come i dati dell'immagine, in base al valore della proprietà ImageDataDiscard. Se questa proprietà è impostata su 4, il canale alfa interfoliato viene completamente eliminato e il formato pixel dell'immagine transcodificata viene modificato di conseguenza.

Nessun valore predefinito.

### <a name="ignoreoverlap-option"></a>Opzione IgnoreOverlap

Questa opzione è valida solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode-option) è **IMPOSTATA** SU TRUE e viene richiesta una transcodifica di area secondaria di esattamente uno o più riquadri. L'operazione predefinita per una transcodifica di area (o decodifica) è espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area. Quando questo parametro è impostato su **TRUE,** i pixel circostanti vengono ignorati e vengono estratti solo il riquadro o i riquadri selezionati. Anche in questo caso, è necessario che l'area richiesta corrisponda esattamente alle coordinate di uno o più riquadri. Se l'immagine di origine non è affiancata o se l'area richiesta specifica riquadri parziali, questo parametro viene ignorato.

Il valore predefinito è **FALSE.**

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa. Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md) Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Supporto di IWICBitmapSourceTransform

Oltre alle interfacce necessarie per essere un codec abilitato per WIC, il decodificatore HD Photo nativo supporta anche [**IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) **L'interfaccia IWICBitmapSourceTransform** offre un'opzione avanzata per decodificare un flusso di bit dell'immagine. Anziché restituire un'immagine completa usando [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) **l'interfaccia IWICBitmapSourceTransform** abilita le opzioni del decodificatore seguenti.

-   Decodificare una sottoarea rettangolare dell'immagine.
-   Decodificare a una risoluzione inferiore
-   Decodificare in un formato pixel diverso
-   Eseguire una trasformazione (rotazione/capovolgimento) durante la decodifica

Il codec HD Photo nativo offre il livello di supporto seguente per [**l'interfaccia IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="doessupporttransform"></a>DoesSupportTransform

L'implementazione nativa supporta [**tutte le trasformazioni WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="getclosestsize"></a>GetClosestSize

Per le richieste che sono inferiori a 1/2 della dimensione dell'immagine di origine in entrambe le dimensioni, HD Photo restituisce le dimensioni dell'immagine integer più grandi che sono divisibile uniformemente per un fattore di due. Per tutte le altre dimensioni richieste, HD Photo restituisce le dimensioni dell'immagine originale.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

HD Photo restituisce il formato pixel dell'immagine codificata.

### <a name="copypixels"></a>CopyPixels

HD Photo accetta qualsiasi area richiesta specificata dal [**parametro WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) e restituisce tale parte dell'immagine.

I *parametri uiWidth* *e uiHeight* devono specificare le dimensioni come restituito dalla [**funzione GetClosestSize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) Qualsiasi altro valore restituisce un errore.

Il *parametro pguidDstFormat* deve specificare il formato pixel restituito dalla [**funzione GetClosestPixelFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) Qualsiasi altro valore restituisce un errore.

HD Photo accetta qualsiasi valore consentito per il *parametro dstTransform.* Si noti che i valori consentiti da WIC per questo parametro sono diversi dai valori usati da HD Photo per il tag di metadati Transformation.

 

 
