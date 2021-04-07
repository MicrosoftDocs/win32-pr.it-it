---
description: Informazioni sui colori estesi
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Informazioni sui colori estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ba43180a0f1e5253540088c1638f59d52380c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749242"
---
# <a name="extended-color-information"></a>Informazioni sui colori estesi

Se si conoscono i colori RGB, si sa che (255, 255, 255) è la tripletta RGB a 8 bit per il colore *bianco*. Ma qual è il *colore* effettivo definito da questo tripletta?

La risposta potrebbe essere sorprendente: senza informazioni aggiuntive, questo tripletta non definisce alcun colore specifico. Il significato di qualsiasi valore RGB dipende dallo spazio dei *colori*. Se non si conosce lo spazio colore, significa che il colore non è noto.

Uno spazio colore definisce il modo in cui la rappresentazione numerica di un determinato valore di colore deve essere riprodotta come luce fisica. Quando il video è codificato in uno spazio di colore, ma viene visualizzato in un altro, produce colori distorti, a meno che il video non venga corretto a colori. Per ottenere una fedeltà cromatica accurata, è quindi fondamentale comprendere lo spazio dei colori del video di origine. In precedenza, la pipeline video in Windows non portava informazioni sullo spazio di colore previsto. A partire da Windows Vista, sia DirectShow che Media Foundation supportano le informazioni estese sui colori nel tipo di supporto. Queste informazioni sono disponibili anche per l'accelerazione video DirectX (DXVA).

Il modo standard per descrivere lo spazio dei colori in modo matematico consiste nell'usare lo spazio dei colori CIE XYZ, definito da International Commission on illuminazione (CIE). Non è pratico usare i valori di CIE XYZ direttamente nei video, ma lo spazio dei colori CIE XYZ può essere usato come rappresentazione intermedia quando si esegue la conversione tra gli spazi dei colori.

Per riprodurre i colori in modo accurato, sono necessarie le informazioni seguenti:

-   Colori primari. Le primarie colore definiscono il modo in cui i valori dei tristimoli CIE XYZ sono rappresentati come componenti RGB. In effetti, le primarie colore definiscono il "significato" di un valore RGB specificato.
-   Funzione transfer. La funzione Transfer è una funzione che converte i valori RGB lineari in valori SOTTOCAMPIONATURA non lineari. Questa funzione viene anche chiamata *correzione gamma*.
-   Matrice di traslazione. La matrice di trasferimento definisce la modalità di conversione di SOTTOCAMPIONATURA in Y'PbPr.
-   Campionamento Chroma. La maggior parte dei video YUV viene trasmessa con una minore risoluzione nei componenti croma rispetto a Luma. Il campionamento Chroma è indicato dal FOURCC del formato video. Ad esempio, YUY2 è un formato 4:2:2, ovvero gli esempi di Chroma vengono campionati orizzontalmente in base a un fattore di 2.
-   Ubicazione Chroma. Quando il Chroma viene campionato, la posizione degli esempi di croma rispetto agli esempi Luma determina la modalità di interpolazione degli esempi mancanti.
-   Intervallo nominale. L'intervallo nominale definisce il modo in cui i valori di Y'PbPr vengono ridimensionati in CbCr.

## <a name="color-space-in-media-types"></a>Spazio colore nei tipi di supporto

DirectShow, Media Foundation e DirectX Video Acceleration (DXVA) hanno tutti diversi modi per rappresentare i formati video. Fortunatamente, è facile tradurre le informazioni sullo spazio dei colori da una a un'altra, perché le enumerazioni rilevanti sono le stesse.

-   DXVA 1,0: le informazioni sullo spazio colore sono specificate nella [**struttura \_ ExtendedFormat di DXVA**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) .
-   DXVA 2,0: le informazioni sullo spazio colore sono specificate nella struttura della struttura [**\_ ExtendedFormat DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) . Questa struttura è identica alla struttura DXVA 1,0 e il significato dei campi è lo stesso.
-   DirectShow: le informazioni sullo spazio colore sono fornite nella struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Le informazioni vengono archiviate nei 24 bit superiori del campo **dwControlFlags** . Se sono presenti informazioni sullo spazio colore, impostare il flag **AMCONTROL \_ COLORINFO \_ present** in **dwControlFlags**. Quando questo flag è impostato, il campo **dwControlFlags** deve essere interpretato come una [**struttura \_ ExtendedFormat di DXVA**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) , ad eccezione del fatto che gli 8 bit inferiori della struttura sono riservati per i flag **AMCONTROL \_ xxx** .
-   Driver di acquisizione video: le informazioni sullo spazio colore sono fornite nella struttura [**KS \_ VIDEOINFOHEADER2**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) . Questa struttura è identica alla struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) e il significato dei campi è lo stesso.
-   Media Foundation: le informazioni sullo spazio dei colori vengono archiviate come attributi nel tipo di supporto:

    

    | Informazioni sui colori  | Attributo                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Colori primari    | [**\_ \_ principali video MF \_ mt**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Funzione Transfer  | [**\_funzione di \_ trasferimento MF mt \_**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matrice di trasferimento    | [**\_ \_ matrice YUV MF \_ mt**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Sottocampionamento Chroma | [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)<br/> (Dato da FOURCC, archiviato nel primo **DWORD** del GUID del sottotipo).<br/> |
    | Ubicazione Chroma      | [**posizione \_ di \_ Chroma del video MF mt \_ \_**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Intervallo nominale      | [**\_ \_ \_ intervallo nominale video MF \_ mt**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversione dello spazio colore

La conversione da uno spazio CbCr a un altro richiede i passaggi seguenti.

1.  Quantizzazione inversa: converte la rappresentazione CbCr in una rappresentazione Y'PbPr usando l'intervallo nominale di origine.
2.  Campionamento: converte i valori Chroma campionati in 4:4:4 mediante l'interpolazione dei valori di Chroma.
3.  Conversione da YUV a RGB: conversione da Y'PbPr a SOTTOCAMPIONATURA non lineare, usando la matrice di trasferimento di origine.
4.  Funzione di trasferimento inversa: converte SOTTOCAMPIONATURA non lineari in RGB lineare, usando l'inverso della funzione di trasferimento.
5.  Conversione dello spazio dei colori RGB: usare le primarie di colore per convertire lo spazio RGB di origine nello spazio RGB di destinazione.
6.  Funzione Transfer: converte RGB lineare in SOTTOCAMPIONATURA non lineari, usando la funzione di trasferimento di destinazione.

7.  Conversione da RGB a YUV: converte SOTTOCAMPIONATURA in Y'PbPr usando la matrice di trasferimento di destinazione.
8.  Sottocampionando: converte 4:4:4 in 4:2:2, 4:2:0 o 4:1:1 filtrando i valori di Chroma.
9.  Quantizzazione: converte Y'PbPr in CbCr, usando l'intervallo nominale di destinazione.

I passaggi da 1 a 4 si verificano nello spazio colore di origine e i passaggi 6-9 si verificano nello spazio dei colori di destinazione. Nell'implementazione effettiva, i passaggi intermedi possono essere approssimati e i passaggi adiacenti possono essere combinati. Esiste in genere un compromesso tra accuratezza e costo computazionale.

Per eseguire la conversione da RT. 601 a RT. 709, ad esempio, sono necessarie le fasi seguenti:

-   Quantizzazione inversa: CbCr (601) a Y'PbPr (601)
-   Campionamento: Y'PbPr (601)
-   Da YUV a RGB: Y'PbPr (601) a SOTTOCAMPIONATURA ' (601)
-   Funzione di trasferimento inversa: SOTTOCAMPIONATURA ' (601) a RGB (601)
-   Conversione dello spazio colore RGB: RGB (601) a RGB (709)
-   Funzione Transfer: RGB (709) a SOTTOCAMPIONATURA ' (709)
-   Da RGB a YUV: SOTTOCAMPIONATURA ' (709) a Y'PbPr (709)
-   Sottocampionando: Y'PbPr (709)

-   Quantizzazione: Y'PbPr (709) a CbCr (709)

## <a name="using-extended-color-information"></a>Utilizzo di informazioni estese sui colori

Per mantenere la fedeltà dei colori in tutta la pipeline, le informazioni sullo spazio colore devono essere introdotte nell'origine o nel decodificatore e trasmesse attraverso la pipeline al sink.

### <a name="video-capture-devices"></a>Dispositivi di acquisizione video

La maggior parte dei dispositivi di acquisizione analoghi usa uno spazio di colore ben definito durante l'acquisizione di video. I driver di acquisizione devono offrire un formato con un blocco di formato **KS \_ VIDEOINFOHEADER2** che contiene le informazioni sul colore. Per compatibilità con le versioni precedenti, il driver deve accettare formati che non contengono le informazioni sul colore. Ciò consentirà al driver di funzionare con i componenti che non accettano le informazioni estese sui colori.

### <a name="file-based-sources"></a>Origini basate su file

Quando si analizza un file video, l'origine multimediale (o filtro parser, in DirectShow) potrebbe essere in grado di fornire alcune informazioni sui colori. Il navigatore DVD può ad esempio determinare lo spazio del colore in base al contenuto del DVD. Altre informazioni sul colore potrebbero essere disponibili per il decodificatore. Ad esempio, un flusso video elementare MPEG-2 fornisce le informazioni sul colore nel \_ \_ campo estensione visualizzazione sequenza. Se le informazioni sul colore non sono descritte in modo esplicito nell'origine, possono essere definite in modo implicito in base al tipo di contenuto. Ad esempio, le varietà NTSC e PAL di video DV utilizzano ognuno spazi colore diversi. Infine, il decodificatore può usare tutte le informazioni sul colore ottenute dal tipo di supporto di origine.

### <a name="other-components"></a>Altri componenti

Altri componenti potrebbero dover usare le informazioni sullo spazio di colore in un tipo di supporto:

-   Per la selezione di un algoritmo di conversione, è necessario che i convertitori di spazio del software usino le informazioni sullo spazio colore.
-   I mixer video, ad esempio il mixer EVR (Enhanced video renderer), devono usare le informazioni sui colori per combinare flussi video da diversi tipi di contenuto.
-   Le API di elaborazione video DXVA e DDIs consentono al chiamante di specificare le informazioni relative allo spazio colore. La GPU deve usare queste informazioni quando esegue la combinazione di video hardward.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
