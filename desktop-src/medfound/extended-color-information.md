---
description: Informazioni estese sui colori
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Informazioni estese sui colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ffce83acccd2004156d55c0711836271d9ad5cfe7a6ac395e0d9fcbb418142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466371"
---
# <a name="extended-color-information"></a>Informazioni estese sui colori

Se si conoscono i colori RGB, si sa che (255, 255, 255) è la tripletta RGB a 8 bit per il colore *bianco.* Ma qual è il *colore effettivo* definito da questa tripletta?

La risposta può essere sorprendente: senza alcune informazioni aggiuntive, questa tripletta non definisce alcun colore particolare. Il significato di qualsiasi valore RGB dipende dallo spazio *colore*. Se non si conosce lo spazio colore, in senso stretto non si conosce il colore.

Uno spazio colore definisce il modo in cui la rappresentazione numerica di un determinato valore di colore deve essere riprodotta come luce fisica. Quando il video viene codificato in uno spazio colori ma viene visualizzato in un altro, si verifica una distorsione dei colori, a meno che il video non sia con correzione del colore. Per ottenere una fedeltà dei colori accurata, è quindi fondamentale conoscere lo spazio colore del video di origine. In precedenza, la pipeline video Windows non aveva informazioni sullo spazio colore previsto. A partire da Windows Vista, sia DirectShow che Media Foundation supportano informazioni estese sul colore nel tipo di supporto. Queste informazioni sono disponibili anche per DirectX Video Acceleration (DXVA).

Il modo standard per descrivere matematicamente uno spazio colori è usare lo spazio colori CIE XYZ, definito dalla International Commission on Illumination (CIE). Non è pratico usare i valori CIE XYZ direttamente nel video, ma lo spazio colore CIE XYZ può essere usato come rappresentazione intermedia durante la conversione tra spazi colori.

Per riprodurre i colori in modo accurato, sono necessarie le informazioni seguenti:

-   Primarie di colore. Le primarie di colore definiscono il modo in cui i valori tristimuli CIE XYZ vengono rappresentati come componenti RGB. In effetti, le primarie di colore definiscono il "significato" di un valore RGB specificato.
-   Funzione transfer. La funzione di trasferimento è una funzione che converte i valori RGB lineari in valori R'G'B non lineari. Questa funzione è detta anche *correzione gamma.*
-   Matrice di trasferimento. La matrice di trasferimento definisce la modalità di conversione di R'G'B in Y'PbPr.
-   Campionamento di chroma. La maggior parte dei video YUV viene trasmessa con una risoluzione inferiore nei componenti chroma rispetto a luma. Il campionamento di chroma è indicato dal valore FOURCC del formato video. Ad esempio, YUY2 è un formato 4:2:2, vale a dire che i campioni di chroma vengono campionati orizzontalmente da un fattore di 2.
-   Siting di chroma. Quando la chroma viene campionata, la posizione dei campioni di chroma rispetto ai campioni di luma determina il modo in cui i campioni mancanti devono essere interpolati.
-   Intervallo nominale. L'intervallo nominale definisce il modo in cui i valori Y'PbPr vengono ridimensionati in Y'CbCr.

## <a name="color-space-in-media-types"></a>Spazio colore nei tipi di supporti

DirectShow, Media Foundation e DirectX Video Acceleration (DXVA) hanno modi diversi per rappresentare i formati video. Fortunatamente, è facile tradurre le informazioni sullo spazio colore da una all'altra, perché le enumerazioni pertinenti sono le stesse.

-   DXVA 1.0: le informazioni sullo spazio dei colori vengono fornite nella [**struttura DXVA \_ ExtendedFormat.**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat)
-   DXVA 2.0: le informazioni sullo spazio colore vengono fornite nella [**struttura della struttura DXVA2 \_ ExtendedFormat.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) Questa struttura è identica alla struttura DXVA 1.0 e il significato dei campi è lo stesso.
-   DirectShow: le informazioni sullo spazio colore vengono fornite nella [**struttura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Le informazioni vengono archiviate nei 24 bit superiori del **campo dwControlFlags.** Se sono presenti informazioni sullo spazio colore, impostare il flag **AMCONTROL \_ COLORINFO \_ PRESENT** in **dwControlFlags**. Quando questo flag è impostato, il **campo dwControlFlags** deve essere interpretato come una struttura [**\_ DXVA ExtendedFormat,**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) ad eccezione del fatto che gli 8 bit inferiori della struttura sono riservati per i flag **AMCONTROL \_ xxx.**
-   Driver di acquisizione video: le informazioni sullo spazio colore sono fornite nella [**struttura \_ VIDEOINFOHEADER2 di KS.**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) Questa struttura è identica alla [**struttura VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) e il significato dei campi è lo stesso.
-   Media Foundation: le informazioni sullo spazio colore vengono archiviate come attributi nel tipo di supporto:

    

    | Informazioni sui colori  | Attributo                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Color primaries (Primarie colori)    | [**PRIMARIE \_ VIDEO MF MT \_ \_**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Funzione Transfer  | [**FUNZIONE MF \_ MT \_ TRANSFER \_**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matrice di trasferimento    | [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Sottocampionamento chroma | [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)<br/> Dato da FOURCC, archiviato nel primo **valore DWORD** del GUID del sottotipo.<br/> |
    | Siting chroma      | [**MF \_ MT \_ VIDEO \_ CHROMA \_ SITING**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Intervallo nominale      | [**MF \_ MT \_ VIDEO \_ NOMINAL \_ RANGE**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversione dello spazio colore

La conversione da uno spazio Y'CbCr a un altro richiede i passaggi seguenti.

1.  Quantizzazione inversa: convertire la rappresentazione Y'CbCr in una rappresentazione Y'PbPr, usando l'intervallo nominale di origine.
2.  Upsampling: converte i valori della croma campionata in 4:4:4 interpolando i valori della chroma.
3.  Conversione da YUV a RGB: conversione da Y'PbPr a R'G'B non lineare, usando la matrice di trasferimento di origine.
4.  Funzione di trasferimento inversa: converte R'G'B' non lineare in RGB lineare, usando l'inverso della funzione di trasferimento.
5.  Conversione dello spazio colore RGB: usare le primarie di colore per eseguire la conversione dallo spazio RGB di origine allo spazio RGB di destinazione.
6.  Funzione di trasferimento: convertire RGB lineare in R'G'B non lineare, usando la funzione di trasferimento di destinazione.

7.  Conversione da RGB a YUV: convertire R'G'B' in Y'PbPr usando la matrice di trasferimento di destinazione.
8.  Downsampling: convertire 4:4:4 in 4:2:2, 4:2:0 o 4:1:1 filtrando i valori chroma.
9.  Quantizzazione: convertire Y'PbPr in Y'CbCr, usando l'intervallo nominale di destinazione.

I passaggi da 1 a 4 si verificano nello spazio colore di origine e i passaggi da 6 a 9 si verificano nello spazio colore di destinazione. Nell'implementazione effettiva i passaggi intermedi possono essere approssimati e i passaggi adiacenti possono essere combinati. In genere esiste un compromesso tra accuratezza e costo di calcolo.

Ad esempio, per la conversione da RT.601 a RT.709 sono necessarie le fasi seguenti:

-   Quantizzazione inversa: da Y'CbCr(601) a Y'PbPr(601)
-   Upsampling: Y'PbPr(601)
-   Da YUV a RGB: da Y'PbPr(601) a R'G'B'(601)
-   Funzione di trasferimento inversa: da R'G'B'(601) a RGB(601)
-   Conversione dello spazio colore RGB: da RGB(601) a RGB (709)
-   Funzione di trasferimento: da RGB(709) a R'G'B'(709)
-   Da RGB a YUV: da R'G'B' (709) a Y'PbPr(709)
-   Downsampling: Y'PbPr(709)

-   Quantizzazione: da Y'PbPr(709) a Y'CbCr(709)

## <a name="using-extended-color-information"></a>Uso di informazioni estese sui colori

Per mantenere la fedeltà dei colori in tutta la pipeline, le informazioni sullo spazio dei colori devono essere introdotte nell'origine o nel decodificatore e trasmesse fino al sink attraverso la pipeline.

### <a name="video-capture-devices"></a>Dispositivi di acquisizione video

La maggior parte dei dispositivi di acquisizione analogico usa uno spazio colore ben definito per l'acquisizione di video. I driver di acquisizione devono offrire un formato con **un blocco di formato \_ KS VIDEOINFOHEADER2** che contiene le informazioni sul colore. Per compatibilità con le versioni precedenti, il driver deve accettare formati che non contengono informazioni sul colore. In questo modo il driver funzionerà con i componenti che non accettano le informazioni estese sul colore.

### <a name="file-based-sources"></a>Origini basate su file

Durante l'analisi di un file video, l'origine multimediale (o il filtro del parser, in DirectShow) potrebbe essere in grado di fornire alcune informazioni sul colore. Ad esempio, lo Strumento di navigazione DVD può determinare lo spazio dei colori in base al contenuto del DVD. Altre informazioni sul colore potrebbero essere disponibili per il decodificatore. Ad esempio, un flusso video elementare MPEG-2 fornisce le informazioni sul colore nel campo dell'estensione di \_ visualizzazione \_ della sequenza. Se le informazioni sul colore non sono descritte in modo esplicito nell'origine, potrebbero essere definite in modo implicito dal tipo di contenuto. Ad esempio, i tipi di video DV NTSC e PAL usano spazi colori diversi. Infine, il decodificatore può usare le informazioni sul colore che ottiene dal tipo di supporto dell'origine.

### <a name="other-components"></a>Altri componenti

Altri componenti potrebbero dover usare le informazioni sullo spazio colore in un tipo di supporto:

-   I convertitori di spazi colori software devono usare le informazioni sullo spazio colore quando si seleziona un algoritmo di conversione.
-   I mixer video, ad esempio il mixer EVR (Enhanced Video Renderer), devono usare le informazioni sui colori quando si combinano flussi video da diversi tipi di contenuto.
-   Le API di elaborazione video DXVA e le DDI consentono al chiamante di specificare informazioni sullo spazio colore. La GPU deve usare queste informazioni quando esegue la combinazione di video hardward.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file multimediali video](video-media-types.md)
</dt> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
