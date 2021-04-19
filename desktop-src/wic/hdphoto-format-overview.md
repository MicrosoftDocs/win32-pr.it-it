---
description: In questo argomento vengono fornite informazioni sul codec di foto HD nativo disponibile tramite il componente Windows Imaging Component (WIC).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Panoramica del formato foto HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9275abd4b74c7eb4be7673d85bb4eab5f45a163d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312393"
---
# <a name="hd-photo-format-overview"></a>Panoramica del formato foto HD

In questo argomento vengono fornite informazioni sul codec di foto HD nativo disponibile tramite il componente Windows Imaging Component (WIC).

> [!IMPORTANT]
>
> Il formato foto HD è un'implementazione pre-standard del formato JPEG XR. Il formato JPEG XR è stato completamente implementato in Windows 8. Per ulteriori informazioni, vedere la [Panoramica del codec JPEG XR](jpeg-xr-codec.md) .

 

In questo argomento sono contenute le sezioni seguenti.

-   [Identità codec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opzioni del codificatore](#encoder-options)
-   [Decodifica](#decoding)
    -   [Supporto di IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Identità codec

Nella tabella seguente vengono fornite informazioni di identificazione del codec.



|                        |                                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| Nome/i formale/i         | Foto HD, foto di Windows Media                                                   |
| Estensioni del nome di file | WDP                                                                             |
| tipo MIME              | image/vnd. ms-Photo                                                              |
| Firma file      | Primi quattro byte: 0x4949bc00 (versione 0; versione non definitiva), 0x4949bc01 (versione 1,0) |



 

La tabella seguente elenca i GUID usati per identificare i componenti dei codec di foto HD nativi.



| Componente        | Nome descrittivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato contenitore | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Decodificatore          | \_WICWMPDECODER CLSID     | a26cec36-234C-4950-ae16e34aace71d0d |
| Codificatore          | \_WICWMPENCODER CLSID     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Codifica

L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opzioni del codificatore

I codec abilitati per WIC differiscono a livello di opzione di codifica. Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore. Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine. Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).

Il codec foto HD usa entrambe le opzioni WIC di base e offre diverse opzioni di codifica per foto HD specifiche. La tabella seguente elenca le opzioni del codificatore supportate dal codec Photo HD nativo.

Opzioni di base del codificatore WIC

| Nome della proprietà | VARTYPE | Gamma valori | Valore predefinito |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | \_R4 VT | 0-1,0 | 0.9 |
| [Lossless](#lossless-option) | \_bool VT | **true**, **false** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | \_Ui1 VT | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Opzioni del codificatore per foto HD specifiche

| Nome della proprietà | VARTYPE | Gamma valori | Valore predefinito |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | \_bool VT | **true**, **false** | **FALSE** |
| [Qualità](#quality-option) | \_Ui1 VT | 1 - 255 | 10 |
| [Overlap](#overlap-option) | \_Ui1 VT | 0 - 2 | 1 |
| [Sottocampionamento](#subsampling-option) | \_Ui1 VT | 0 - 3 | 3 se ImageQuality > 0,8; in caso contrario, 1; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (larghezza immagine-1)  >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (altezza immagine-1)  >> 8 |
| [FrequencyOrder](#frequencyorder-option) | \_bool VT | **true**, **false** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | \_bool VT | **true**, **false** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | \_Ui1 VT | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | \_bool VT | **true**, **false** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | \_Ui1 VT | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | \_Ui1 VT | 0 - 4 | non usata. |
| [IgnoreOverlap](#ignoreoverlap-option) | \_bool VT | **true**, **false** | **FALSE** |


Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.

### <a name="imagequality-option"></a>ImageQuality-opzione

Specifica la fedeltà dell'immagine desiderata. 0,0 indica che la fedeltà più bassa possibile e 1,0 specifica la massima fedeltà. Per il formato immagine HD Photo, un valore 1,0 comporta una compressione matematicamente senza perdita di dati.

Il valore predefinito è 0,9.

### <a name="compressionquality-option"></a>CompressionQuality-opzione

Specifica la qualità di compressione desiderata. 0,0 indica lo schema di compressione efficiente disponibile. In genere, questo schema genera una codifica più veloce ma un output più grande. Il valore 1,0 specifica lo schema di compressione più efficiente disponibile, che in genere produce una codifica più lunga ma un output più piccolo.

La foto HD non supporta questa opzione del codificatore. Questo valore viene ignorato se presente nell'elenco di parametri [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .

### <a name="lossless-option"></a>Opzione Lossless

Specifica se utilizzare la modalità di compressione delle perdite. Per il formato immagine HD Photo, questo valore sostituisce il valore dell'opzione [ImageQuality](#imagequality-option) .

Il valore predefinito è **false**.

### <a name="bitmaptransform-option"></a>BitmapTransform-opzione

Specifica il modo in cui l'immagine viene trasformata durante la decodifica delle immagini. È necessario impostare questa opzione su uno dei valori di enumerazione [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

Il valore predefinito è [**WICBitmapTransformOptions:: WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>UseCodecOptions-opzione

Se il valore è VARIANT \_ true le opzioni [qualità](#quality-option), [sovrapposizione](#overlap-option)e [sottocampionamento](#subsampling-option) anziché il valore dell'opzione.

Il valore predefinito è **false**.

### <a name="quality-option"></a>Opzione qualità

Specifica la qualità di compressione per l'immagine. Il valore 1 indica la modalità lossless. L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.

Il valore predefinito è 10.

### <a name="overlap-option"></a>Opzione di sovrapposizione

Specifica il livello di elaborazione della sovrapposizione.

Nella tabella seguente sono elencati i livelli di elaborazione di sovrapposizione disponibili.



| Valore | Descrizione                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Nessuna elaborazione della sovrapposizione attivata.                                                                                                                                                           |
| 1     | È abilitato un livello di elaborazione della sovrapposizione, che modifica i valori con codifica del blocco 4x4 in base ai valori dei blocchi adiacenti.                                                                       |
| 2     | Sono attivati due livelli di elaborazione della sovrapposizione. Oltre all'elaborazione di primo livello, i valori codificati dei blocchi di macro 16x16 vengono modificati in base ai valori dei blocchi di macro adiacenti. |



 

Il valore predefinito è 1.

### <a name="subsampling-option"></a>Opzione sottocampionamento

Specifica una compressione aggiuntiva nello spazio Chroma. In questo modo, è possibile mantenere i dettagli della luminanza a scapito dei dettagli del colore. Questa opzione si applica solo alle immagini RGB.

Nella tabella seguente sono elencate le opzioni di campionamento secondario disponibili.



| Valore | Descrizione                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | la codifica 4:4:4 conserva la risoluzione Chroma completa.                                                                                                                                                                                                                                            |
| 2     | la codifica 4:2:2 riduce la risoluzione Chroma a 1/2 della risoluzione della luminanza.                                                                                                                                                                                                                      |
| 1     | la codifica 4:2:0 riduce la risoluzione Chroma a 1/4 della risoluzione della luminanza.                                                                                                                                                                                                                      |
| 0     | 4:0:0 la codifica Elimina tutto il contenuto Chroma e conserva solo la luminanza. Poiché il codec usa una definizione di luminanza leggermente modificata per migliorare le prestazioni, è consigliabile convertire un'immagine RGB in monocromatico prima della codifica anziché usare questa modalità di sottocampionamento Chroma. |



 

Il valore predefinito è 3 Se [ImageQuality](#imagequality-option) > 0,8; in caso contrario, 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>Opzioni HorizontalTileSlices, VerticalTileSlices

Specificare l'affiancamento orizzontale e verticale dell'immagine prima di eseguire la codifica della compressione per ottenere prestazioni ottimali di decodifica dell'area. Suddividendo l'immagine in riquadri rettangolari durante la codifica è possibile decodificare le aree dell'immagine senza elaborare l'intero flusso di dati compressi. Il valore predefinito 0 non specifica alcuna suddivisione, quindi l'intera immagine viene considerata come un singolo riquadro. Il valore 1 per ogni parametro crea una singola divisione orizzontale e una singola divisione verticale, dividendo in modo efficace l'immagine in quattro riquadri di dimensioni uguali. Il valore massimo di 4095 per ogni parametro divide l'immagine in righe del riquadro 4096 con 4096 riquadri per riga. In altre parole, i valori dei parametri equivalgono al numero di riquadri orizzontali e verticali (rispettivamente) meno 1. Un riquadro non può mai contenere più di 16 pixel di larghezza o altezza, quindi il codificatore di foto HD potrebbe modificare questo parametro per mantenere le dimensioni minime necessarie per il riquadro. Poiché a ogni riquadro è associato un sovraccarico di archiviazione ed elaborazione, è necessario scegliere attentamente questi valori per soddisfare lo scenario specifico.

[HorizontalTileSlices](/windows): il valore predefinito è (larghezza immagine-1)  >> 8.

[VerticalTileSlices](/windows): il valore predefinito è (altezza immagine-1)  >> 8.

### <a name="frequencyorder-option"></a>FrequencyOrder-opzione

Specifica che l'immagine deve essere codificata in ordine di frequenza. I dati con frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla relativa frequenza anziché all'orientamento spaziale. L'organizzazione di un file in base all'ordine di frequenza offre le migliori prestazioni per qualsiasi decodifica basata sulla frequenza, quindi è consigliabile. Le implementazioni del dispositivo dei codificatori di foto HD possono organizzare un file in ordine spaziale per ridurre il footprint di memoria necessario durante la codifica.

Il valore predefinito è **true** ed è consigliabile che le applicazioni e i dispositivi usino sempre l'ordine di frequenza a meno che non si abbiano motivi di prestazioni o specifici dell'applicazione per l'uso dell'ordine spaziale.

### <a name="interleavedalpha-option"></a>InterleavedAlpha-opzione

Se si imposta questa opzione su **true** , il codec codifica le informazioni del canale alfa come canale Interleaved aggiuntivo, senza correlazioni con i canali del contenuto di immagine. Questa modalità è utile quando è necessario decodificare Alpha simultaneamente con l'immagine in uno scenario di streaming.

Impostando questo parametro su **false** si ottiene un canale alfa planare, codificato come immagine separata con il proprio valore di qualità facoltativo. Utilizzando un canale alfa planare, è possibile decodificare i dati dell'immagine e il canale alfa in modo indipendente. I canali alfa con interfoliazione sono supportati solo per determinati formati pixel RGB. È possibile associare un canale alfa planare a qualsiasi formato di immagine che definisce un canale alfa.

Il valore predefinito è **false**.

### <a name="alphaquality-option"></a>AlphaQuality-opzione

Specifica la qualità di compressione per l'immagine del canale alfa planare. Il valore 1 imposta la modalità lossless. L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.

Il valore predefinito è 1.

### <a name="compresseddomaintranscode-option"></a>CompressedDomainTranscode-opzione

Con la foto HD è possibile eseguire una serie di operazioni di trasformazione dei file senza decodificare effettivamente i dati compressi e ricodificarli nel file di destinazione. Le operazioni di dominio compresso sono molto efficienti ed evitano una perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine compressa con perdite di codice.

Sono supportate le operazioni di dominio compresso seguenti:

-   Ritagliare un'area dell'immagine.
-   Eseguire una trasformazione rotazione/Capovolgi.
-   Rimuovere i dati di frequenza (rendendo possibile la creazione di un file di immagine più piccolo).
-   Riorganizzare l'immagine tra l'ordine sequenziale spaziale e di frequenza.

Il codificatore di foto HD esegue un'operazione di transcodifica del dominio compresso quando codifica un'immagine di foto HD usando un decodificatore di foto HD come origine dell'immagine. A seconda delle opzioni di codifica selezionate, il codec usa un'operazione di dominio compresso, se possibile. Se un'applicazione sceglie di inibire in modo esplicito le operazioni di transcodifica del dominio compresso, è necessario impostare l'opzione *UseCodecOptions* su **true** e l'opzione *CompressedDomainTranscode* su **false**.

Quando il codec esegue un'operazione di dominio compresso, sono consentite solo alcune impostazioni di proprietà e parametri del codificatore.

-   Le opzioni di base del codificatore [ImageQuality](#imagequality-option), [CompressionQuality](/windows) e [Lossless](#lossless-option) vengono ignorate.
-   Le [Opzioni del](#quality-option)codificatore specifiche della foto HD, [sovrapposizione](#overlap-option), [InterleavedAlpha](#interleavedalpha-option) e [AlphaQuality](#alphaquality-option) vengono ignorate.
-   Se presente, le opzioni [HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) devono essere impostate su zero. Non è possibile modificare le dimensioni del riquadro di un'immagine come parte di una transcodifica del dominio compresso.
-   È possibile modificare l'organizzazione di immagini tra frequenza e ordinamento spaziale specificando il valore appropriato per le opzioni [FrequencyOrdering](/windows) .
-   In base al valore specificato nell'opzione [BitmapTransform](#bitmaptransform-option) encoder, è possibile eseguire un'operazione di rotazione del cardinale e/o un capovolgimento orizzontale/verticale.
-   È possibile ritagliare l'immagine specificando l'area desiderata usando il parametro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del metodo del codificatore **WriteSource** .
-   I dati di immagini e/o Alpha possono essere rimossi specificando i valori appropriati nelle opzioni [ImageDataDiscard](#imagedatadiscard-option) e/o [AlphaDataDiscard](#alphadatadiscard-option) , riducendo le dimensioni del file codificato ed eseguendo una riduzione efficace della risoluzione della nuova immagine.

Il valore predefinito è **true** ed è consigliabile che le applicazioni e i dispositivi usino sempre l'ordine di frequenza, a meno che non si disponga di motivi specifici per le prestazioni o l'applicazione per l'utilizzo dell'ordine spaziale.

### <a name="imagedatadiscard-option"></a>ImageDataDiscard-opzione

Questo parametro è valido solo se l'opzione [CompressedDomainTranscode](#compresseddomaintranscode-option) è impostata su **true**. in caso contrario, viene ignorato. [ImageDataDiscard](#imagedatadiscard-option) specifica la quantità di dati immagine da eliminare durante una transcodifica del dominio compresso. Se l'immagine contiene un canale alfa con interfoliazione, questo scarto di dati si applica anche al canale alfa, con le eccezioni descritte più avanti in questa sezione.

Sono consentiti i valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | I FlexBits vengono eliminati, rendendo arbitraria una riduzione della qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine. La riduzione esatta delle dimensioni del file o la riduzione della qualità specifica dipende da numerosi fattori e non può essere specificata o stimata. Questo valuereturns un errore se viene specificato per un canale alfa con interfoliazione.                                                    |
| 2     | La banda di dati passa alto Frequency viene eliminata (che include anche il FlexBits), riducendo in modo efficace la risoluzione dell'immagine transcodificata in base a un fattore 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma perde tutti i dettagli in ogni blocco di pixel 4x4. Pertanto, è consigliabile sottocampionare l'immagine transcodificata di conseguenza ogni volta che la si decodifica.                            |
| 3     | Entrambe le bande di dati passa alto e di frequenza passa da basso sono rimosse (che includono anche FlexBits), riducendo in modo efficace la risoluzione dell'immagine transcodificata in base a un fattore pari a 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma perde tutti i dettagli in ogni 16x16 macroblocco di pixel. Pertanto, è consigliabile sottocampionare l'immagine transcodificata di conseguenza ogni volta che la si decodifica. |



 

Il valore predefinito è 0.

### <a name="alphadatadiscard-option"></a>AlphaDataDiscard-opzione

Questa opzione è valida solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode-option) è impostata su **true** e l'immagine contiene un canale alfa planare o con interfoliazione. in caso contrario, viene ignorato. Specifica la quantità di dati di frequenza alfa da eliminare durante una transcodifica del dominio compresso. Per un canale alfa planare sono consentiti i valori seguenti.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non viene eliminato nessun dato di frequenza dell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | I FlexBits vengono eliminati, rendendo arbitraria una riduzione della qualità del canale alfa planare per l'immagine transcodificata senza modificare la risoluzione effettiva. La riduzione esatta delle dimensioni del file o la riduzione della qualità specifica dipende da numerosi fattori e non può essere specificata o stimata.                                                                                                                                                                                                                                                |
| 2     | La banda di dati con frequenza passa alto viene eliminata (che include anche il FlexBits), riducendo in modo efficace la risoluzione del canale alfa planare dell'immagine transcodificata in base a un fattore pari a 4 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli del canale alfa planare in ogni blocco 4x4 di pixel. Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata. In genere, è consigliabile impostare questo valore solo quando si imposta ImageDataDiscard impostando sullo stesso valore. |
| 3     | Entrambe le bande di dati passa alto e di frequenza passa da basso sono rimosse (che includono anche FlexBits), riducendo in modo efficace la risoluzione dell'immagine transcodificata in base a un fattore pari a 16 in entrambe le dimensioni. Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni 16x16 macroblocco di pixel. Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata. In genere, è consigliabile impostare questo valore solo quando si imposta la proprietà ImageDataDiscard sullo stesso valore.               |
| 4     | Il canale alfa è stato completamente rimosso. Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Per le immagini che contengono canali alfa con interfoliazione, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato come i dati dell'immagine, in base al valore della proprietà ImageDataDiscard. Se questa proprietà è impostata su 4, il canale alfa con interfoliazione viene rimosso completamente e il formato pixel dell'immagine transcodificata viene modificato di conseguenza.

Nessun valore predefinito.

### <a name="ignoreoverlap-option"></a>IgnoreOverlap-opzione

Questa opzione è valida solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode-option) è **true** e viene richiesta una transcodifica dell'area secondaria di esattamente uno o più riquadri. L'operazione predefinita per una transcodifica di area (o decodifica) consiste nell'espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area. Quando questo parametro è impostato su **true**, i pixel circostanti vengono ignorati e vengono estratti solo il riquadro o i riquadri selezionati. Anche in questo caso, è necessario che l'area richiesta corrisponda esattamente alle coordinate di uno o più riquadri. Se l'immagine di origine non è affiancata o se l'area richiesta specifica tutti i riquadri parziali, questo parametro viene ignorato.

Il valore predefinito è **false**.

## <a name="decoding"></a>Decodifica

L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa. Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md). Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Supporto di IWICBitmapSourceTransform

Oltre alle interfacce necessarie per essere un codec abilitato per WIC, il decodificatore di foto HD nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform). L'interfaccia **IWICBitmapSourceTransform** fornisce un'opzione avanzata per la decodifica di un flusso di bit di immagine. Anziché restituire semplicemente un'immagine completa usando [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), l'interfaccia **IWICBitmapSourceTransform** Abilita le opzioni di decodificatore seguenti.

-   Decodifica un'area secondaria rettangolare dell'immagine.
-   Decodifica a una risoluzione inferiore
-   Decodifica in un formato pixel diverso
-   Eseguire una trasformazione (rotazione/capovolgimento) durante la decodifica

Il codec foto HD nativo offre il seguente livello di supporto per l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="doessupporttransform"></a>DoesSupportTransform

L'implementazione nativa supporta tutte le trasformazioni di [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

### <a name="getclosestsize"></a>GetClosestSize

Per le richieste minori di 1/2 della dimensione dell'immagine di origine in entrambe le dimensioni, la foto HD restituisce le dimensioni massime dell'immagine Integer successive divisibile in modo uniforme per un fattore di due. Per tutte le altre dimensioni richieste, la foto HD restituisce le dimensioni originali dell'immagine.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

La foto HD restituisce il formato pixel dell'immagine codificata.

### <a name="copypixels"></a>CopyPixels

La foto HD accetta qualsiasi area richiesta specificata dal parametro [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) e restituisce la parte dell'immagine.

I parametri *uiWidth* e *uiHeight* devono specificare le dimensioni restituite dalla funzione [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) . Tutti gli altri valori restituiscono un errore.

Il parametro *pguidDstFormat* deve specificare il formato pixel restituito dalla funzione [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) . Qualsiasi altro valore restituisce un errore.

La foto HD accetta qualsiasi valore consentito per il parametro *dstTransform* . Si noti che i valori consentiti da WIC per questo parametro sono diversi dai valori utilizzati dalla foto HD per il tag dei metadati della trasformazione.

 

 
