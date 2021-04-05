---
description: Formati YUV a 8 bit consigliati per il rendering video
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formati YUV a 8 bit consigliati per il rendering video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753890"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formati YUV a 8 bit consigliati per il rendering video

Gary Sullivan e Stephen Estrop

Microsoft Corporation

Aprile 2002, aggiornato il 2008 novembre

Questo argomento descrive i formati di colore YUV a 8 bit consigliati per il rendering video nel sistema operativo Windows. Questo articolo presenta le tecniche per la conversione tra formati YUV e RGB e fornisce anche tecniche per il campionamento dei formati YUV. Questo articolo è destinato agli utenti che usano la decodifica video YUV o il rendering in Windows.

## <a name="introduction"></a>Introduzione

Molti formati YUV sono definiti in tutto il settore video. Questo articolo identifica i formati YUV a 8 bit consigliati per il rendering video in Windows. I fornitori di decodificatori e i fornitori di visualizzazioni sono invitati a supportare i formati descritti in questo articolo. Questo articolo non riguarda altri usi di colore YUV, ad esempio la fotografia continua.

I formati descritti in questo articolo usano tutti la posizione di 8 bit per pixel per codificare il canale Y (detto anche canale luma) e usano 8 bit per campione per codificare ogni esempio di Chroma U o V. Tuttavia, la maggior parte dei formati YUV usa una media inferiore a 24 bit per pixel, perché contengono un minor numero di campioni di u e V rispetto a Y. Questo articolo non copre i formati YUV con canali Y a 10 bit o superiori.

> [!Note]  
> Ai fini di questo articolo, il termine U è equivalente a CB e il termine V è equivalente a CR.

 

Questo articolo include gli argomenti seguenti:

-   [Campionamento YUV](#yuv-sampling). Descrive le tecniche di campionamento YUV più comuni.
-   [Definizioni della superficie](#surface-definitions). Descrive i formati YUV consigliati.
-   [Conversioni dello spazio colore e della frequenza di campionamento Chroma](#color-space-and-chroma-sampling-rate-conversions). Fornisce alcune linee guida per la conversione tra formati YUV e RGB e per la conversione tra formati YUV diversi.
-   [Identificazione dei formati YUV in Media Foundation](#identifying-yuv-formats-in-media-foundation). Viene illustrato come descrivere i tipi di formato YUV in Media Foundation.

## <a name="yuv-sampling"></a>Campionamento YUV

I canali Chroma possono avere una frequenza di campionamento inferiore rispetto al canale luma, senza alcuna perdita significativa di qualità percettiva. Una notazione detta notazione "A:B: C" viene usata per descrivere la frequenza con cui si campionano i e V rispetto a Y:

-   4:4:4 indica nessun sottocampionando dei canali Chroma.
-   4:2:2 indica 2:1 sottocampionando orizzontali, senza sottocampionando verticali. Ogni riga di analisi contiene quattro campioni Y per ogni due campioni U o V.
-   4:2:0 indica 2:1 sottocampionando orizzontali, con 2:1 sottocampionando verticali.
-   4:1:1 indica 4:1 sottocampionando orizzontali, senza sottocampionando verticali. Ogni riga di analisi contiene quattro esempi Y per ogni esempio di utente e V. 4:1:1 il campionamento è meno comune di altri formati e non viene descritto in dettaglio in questo articolo.

I diagrammi seguenti illustrano come viene campionato Chroma per ogni frequenza sottocampionando. Gli esempi di Luma sono rappresentati da una croce e gli esempi di Chroma sono rappresentati da un cerchio.

![Figura 1. campionamento Chroma](images/yuv-sampling-grids.png)

Il formato dominante del campionamento 4:2:2 è definito nella raccomandazione ITU-R BT. 601. Esistono due varianti comuni del campionamento 4:2:0. Uno di questi viene usato nel video MPEG-2 e l'altro viene usato in MPEG-1 e nelle raccomandazioni ITU-T H. 261 e H. 263.

Rispetto allo schema MPEG-1, è più semplice eseguire la conversione tra lo schema MPEG-2 e le griglie di campionamento definite per i formati 4:2:2 e 4:4:4. Per questo motivo, lo schema MPEG-2 è preferibile in Windows e deve essere considerato l'interpretazione predefinita dei formati 4:2:0.

## <a name="surface-definitions"></a>Definizioni di superficie

Questa sezione descrive i formati YUV a 8 bit consigliati per il rendering video. Questi rientrano in diverse categorie:

-   [4:4:4 formati, 32 bit per pixel](#444-formats-32-bits-per-pixel)
-   [4:2:2 formati, 16 bit per pixel](#422-formats-16-bits-per-pixel)
-   [4:2:0 formati, 16 bit per pixel](#420-formats-16-bits-per-pixel)
-   [4:2:0 formati, 12 bit per pixel](#420-formats-12-bits-per-pixel)

Prima di tutto, è necessario tenere presenti i concetti seguenti per comprendere quanto segue:

-   *Origine della superficie*. Per i formati YUV descritti in questo articolo, l'origine (0, 0) è sempre l'angolo superiore sinistro della superficie.
-   *Stride*. Lo stride di una superficie, talvolta denominato pitch, è la larghezza in byte della superficie. Data un'origine della superficie nell'angolo superiore sinistro, lo stride è sempre positivo.
-   *Allineamento*. L'allineamento di una superficie è a discrezione del driver di visualizzazione grafica. La superficie deve essere sempre allineata DWORD; ovvero le singole righe all'interno della superficie hanno come origine un limite di 32 bit (DWORD). Tuttavia, l'allineamento può essere maggiore di 32 bit, a seconda delle esigenze dell'hardware.
-   Formato compresso rispetto al formato Planar. I formati YUV sono divisi in formati *compressi* e *planari* . In un formato compresso, i componenti Y, U e V vengono archiviati in una sola matrice. I pixel sono organizzati in gruppi di macropixels, il cui layout dipende dal formato. In un formato planare, i componenti Y, U e V vengono archiviati come tre piani distinti.

Per ognuno dei formati YUV descritti in questo articolo è stato assegnato un codice FOURCC. Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.

-   4:4:4 (32 BPP)
    -   [AYUV](#ayuv)
-   4:2:2 (16 BPP)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 BPP)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 BPP)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>4:4:4 formati, 32 bit per pixel

### <a name="ayuv"></a>AYUV

È consigliabile usare un unico formato 4:4:4, con il codice FOURCC AYUV. Si tratta di un formato compresso, in cui ogni pixel è codificato come quattro byte consecutivi, disposti nella sequenza illustrata nella figura seguente.

![Figura 2. layout della memoria ayuv](images/yuvformats01.gif)

I byte contrassegnati come contengono valori per Alpha.

## <a name="422-formats-16-bits-per-pixel"></a>4:2:2 formati, 16 bit per pixel

Sono consigliati due formati 4:2:2, con i codici FOURCC seguenti:

-   YUY2
-   UYVY

Entrambi sono formati compressi, in cui ogni macropixel è codificato in due pixel come quattro byte consecutivi. In questo modo si ottiene un sottocampionando orizzontale del Chroma per un fattore di due.

### <a name="yuy2"></a>YUY2

Nel formato YUY2, i dati possono essere considerati come una matrice di valori **char** senza segno, dove il primo byte contiene il primo campione y, il secondo byte contiene il primo campione U (CB), il terzo byte contiene il secondo campione Y e il quarto byte contiene il primo esempio V (CR), come illustrato nel diagramma seguente.

![Figura 3. layout della memoria YUY2](images/yuvformats02.gif)

Se l'immagine viene trattata come una matrice di valori di **parola** little-endian, la prima **parola** contiene il primo campione Y nei bit meno significativi (LSB) e il primo campione U (CB) nei bit più significativi (MSBs). La seconda **parola** contiene il secondo campione Y in LSB e il primo esempio V (CR) in MSBs.

YUY2 è il formato di 4:2:2 pixel preferito per l'accelerazione video Microsoft DirectX (DirectX VA). Si prevede che sia un requisito a breve termine per gli acceleratori DirectX VA che supportano 4:2:2 video.

### <a name="uyvy"></a>UYVY

Questo formato è identico a quello del formato YUY2, ad eccezione del fatto che l'ordine dei byte è invertito, ovvero i byte Chroma e Luma sono capovolti (Figura 4). Se l'immagine viene trattata come una matrice di due valori di **parola** little-endian, la prima **parola** contiene U in LSB e Y0 in MSBs e la seconda **parola** contiene V in LSB e Y1 in MSBs.

![Figura 4. layout della memoria UYVY](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>4:2:0 formati, 16 bit per pixel

Sono consigliati due formati di 4:2:0 16 bit per pixel (BPP), con i codici FOURCC seguenti:

-   IMC1
-   IMC3

Entrambi i formati YUV sono formati planari. I canali Chroma sono sottocampionati da un fattore di due nelle dimensioni orizzontale e verticale.

### <a name="imc1"></a>IMC1

Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno. Questa operazione è seguita da tutti gli esempi V (CR), quindi da tutti gli esempi U (CB). I piani V e U hanno lo stesso stride del piano Y, con la conseguente presenza di aree di memoria inutilizzate, come illustrato nella figura 5. I piani utente e V devono iniziare sui limiti di memoria che sono un multiplo di 16 righe. Nella figura 5 viene illustrata l'origine di u e V per un fotogramma video 352 x 240. L'indirizzo iniziale dei piani utente e V viene calcolato come segue:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

dove *py* è un puntatore di byte all'inizio della matrice di memoria, come illustrato nella figura seguente.

![Figura 5. layout di memoria IMC1 (esempio)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Questo formato è identico a IMC1, ad eccezione del fatto che i piani utente e V vengono scambiati, come illustrato nel diagramma seguente.

![Figura 6. layout della memoria imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 formati, 12 bit per pixel

Sono consigliati quattro formati a 4:2:0 12 BPP, con i codici FOURCC seguenti:

-   IMC2
-   IMC4
-   YV12
-   NV12

In tutti questi formati, i canali Chroma vengono sottocampionati in base a un fattore di due nelle dimensioni orizzontale e verticale.

### <a name="imc2"></a>IMC2

Questo formato è identico a quello di IMC1, ad eccezione della differenza seguente: le linee V (CR) e U (CB) sono Interleaved con limiti a metà stride. In altre parole, ogni riga a stride totale nell'area Chroma inizia con una riga di campioni V, seguita da una riga di campioni U che inizia al limite di metà stride successivo (Figura 7). Questo layout rende più efficiente l'uso dello spazio degli indirizzi rispetto a IMC1. Taglia lo spazio degli indirizzi Chroma a metà e quindi lo spazio degli indirizzi totale del 25%. Tra i formati 4:2:0, IMC2 è il secondo formato preferito, dopo NV12. Questo processo è illustrato nella figura seguente.

![Figura 7. layout della memoria IMC2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Questo formato è identico a IMC2, ad eccezione delle righe U (CB) e V (CR), come illustrato nella figura seguente.

![Figura 8. layout della memoria IMC4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno. Questa matrice è seguita immediatamente da tutti gli esempi V (CR). Lo stride del piano V è metà dello stride del piano Y; e il piano V contiene metà del numero di righe del piano Y. Il piano V è immediatamente seguito da tutti gli esempi U (CB), con lo stesso stride e il numero di righe del piano V, come illustrato nella figura seguente.

![Figura 9. layout della memoria YV12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno con un numero pari di righe. Il piano Y è immediatamente seguito da una matrice di valori **char** senza segno che contiene campioni U (CB) e V (CR) compressi. Quando l'array U-V combinato viene considerato come una matrice di valori di **parola** little-endian, LSB contiene i valori U e MSBs contiene i valori V. NV12 è il formato preferito di 4:2:0 pixel per DirectX VA. Si prevede che sia un requisito a breve termine per gli acceleratori DirectX VA che supportano 4:2:0 video. Nella figura seguente vengono illustrati il piano Y e la matrice contenente gli esempi compressi e V.

![Figura 10. layout della memoria NV12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversioni dello spazio colore e della frequenza di campionamento Chroma

Questa sezione fornisce le linee guida per la conversione tra YUV e RGB e per la conversione tra diversi formati YUV. In questa sezione sono considerati due schemi di codifica RGB: *computer a 8 bit RGB*, noti anche come sRGB o "full-scale" RGB e *studio video RGB*, oppure "RGB con Head-Room e toe-room". Questi vengono definiti come segue:

-   Il computer RGB utilizza 8 bit per ogni campione di rosso, verde e blu. Il nero è rappresentato da R = G = B = 0 e il bianco è rappresentato da R = G = B = 255.
-   Studio video RGB usa un numero di bit N per ogni campione di rosso, verde e blu, dove N è 8 o più. Il video RGB di studio usa un fattore di scala diverso rispetto al computer RGB e presenta un offset. Il nero è rappresentato da R = G = B = 16 \* 2 ^ (n-8) e il bianco è rappresentato da r = g = b = 235 \* 2 ^ (n-8). Tuttavia, i valori effettivi possono non essere compresi in questo intervallo.

Studio video RGB è la definizione RGB preferita per i video in Windows, mentre il computer RGB è la definizione RGB preferita per le applicazioni non video. In entrambe le forme di RGB, le coordinate di cromaticità sono specificate in ITU-R BT. 709 per la definizione delle primarie di colore RGB. Le coordinate (x, y) di R, G e B sono (0,64, 0,33), (0,30, 0,60) e (0,15, 0,06), rispettivamente. Il riferimento bianco è D65 con coordinate (0,3127, 0,3290). La gamma nominale è 1/0.45 (approssimativamente 2,2), con una gamma precisa definita dettagliatamente in ITU-R BT. 709.

**Conversione tra RGB e 4:4:4 YUV**

Viene innanzitutto descritta la conversione tra RGB e 4:4:4 YUV. Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4 YUV a RGB. Il formato AYUV, che è un formato 4:4:4, USA 8 bit ciascuno per gli esempi Y, U e V. YUV può anche essere definito usando più di 8 bit per esempio per alcune applicazioni.

Per i video digitali sono state definite due conversioni YUV dominanti da RGB. Entrambi sono basati sulla specifica nota come ITU-R Recommendation BT. 709. La prima conversione è il modulo YUV precedente definito per l'uso di 50 Hz in BT. 709. Corrisponde alla relazione specificata nella raccomandazione ITU-R BT. 601, nota anche con il nome precedente, CCIR 601. Deve essere considerato il formato YUV preferito per la risoluzione TV Standard-Definition (720 x 576) e il video di risoluzione inferiore. È caratterizzato dai valori di due costanti *KR* e *KB*:

``` syntax
Kr = 0.299
Kb = 0.114
```

La seconda conversione è il form YUV più recente definito per l'uso 60-Hz in BT. 709 e deve essere considerato il formato preferito per le risoluzioni video precedenti a SDTV. È caratterizzato da valori diversi per queste due costanti:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

La conversione da RGB a YUV viene definita iniziando con quanto segue:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

I valori YUV vengono quindi ottenuti come segue:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

dove

-   M è il numero di bit per campione YUV (M >= 8).
-   Z è la variabile di livello nero. Per il computer RGB, Z è uguale a 0. Per il video RGB di studio, Z equivale a 16 \* 2 ^ (n-8), dove N è il numero di bit per esempio RGB (N >= 8).
-   S è la variabile di ridimensionamento. Per il computer RGB, S è uguale a 255. Per il video RGB di studio, S è uguale a 219 \* 2 ^ (N-8).

La funzione floor (x) restituisce l'intero più grande minore o uguale a x. La funzione clip3 (x, y, z) viene definita nel modo seguente:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> clip3 deve essere implementato come funzione anziché come macro del preprocessore; in caso contrario, si verificheranno più valutazioni degli argomenti.

 

L'esempio Y rappresenta la luminosità e gli esempi di i e V rappresentano rispettivamente le deviazioni dei colori verso il blu e il rosso. L'intervallo nominale per Y è 16 \* 2 ^ (m-8) a 235 \* 2 ^ (m-8). Il nero è rappresentato da 16 \* 2 ^ (m-8) e il bianco viene rappresentato come 235 \* 2 ^ (m-8). L'intervallo nominale per l'utente e V è 16 \* 2 ^ (m-8) a 240 \* 2 ^ (m-8), con il valore 128 \* 2 ^ (m-8) che rappresenta la Croma neutra. Tuttavia, i valori effettivi possono non essere compresi in questi intervalli.

Per i dati di input sotto forma di video RGB di studio, l'operazione di ritaglio è necessaria per memorizzare i valori dell'utente e della V compresi nell'intervallo compreso tra 0 e (2 ^ M)-1. Se l'input è RGB del computer, l'operazione di ritaglio non è obbligatoria, perché la formula di conversione non può produrre valori al di fuori di questo intervallo.

Si tratta delle formule esatte senza approssimazione. Tutte le operazioni seguenti in questo documento sono derivate da queste formule. In questa sezione vengono descritte le conversioni seguenti:

-   [Conversione di RGB888 in YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Conversione da YUV a 8 bit a RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Conversione da 4:2:0 YUV a 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Conversione da 4:2:2 YUV a 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Conversione da 4:2:0 YUV a 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Conversione di RGB888 in YUV 4:4:4

Nel caso di input RGB del computer e output YUV BT. 601 a 8 bit, si ritiene che le formule fornite nella sezione precedente possano essere ragionevolmente approssimate in base a quanto segue:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Queste formule producono risultati a 8 bit usando coefficienti che non richiedono più di 8 bit di precisione (senza segno). I risultati intermedi richiederanno fino a 16 bit di precisione.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Conversione da YUV a 8 bit a RGB888

Dalle formule originali da RGB a YUV, è possibile derivare le relazioni seguenti per BT. 601.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Pertanto, Data:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

le formule per convertire YUV in RGB possono essere derivate come indicato di seguito:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

dove `clip()` indica il ritaglio a un intervallo compreso tra \[ 0 e 255 \] . Si ritiene che queste formule possano essere ragionevolmente approssimate in base a quanto segue:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Queste formule usano alcuni coefficienti che richiedono più di 8 bit di precisione per produrre ogni risultato a 8 bit e i risultati intermedi richiedono più di 16 bit di precisione.

Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4 YUV a RGB. Le sezioni seguenti illustrano alcuni metodi per la conversione di formati 4:2:0 e 4:2:2 in 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Conversione da 4:2:0 YUV a 4:2:2 YUV

Per la conversione da YUV a 4:2:0 YUV a 4:2:2 YUV è richiesta la conversione verticale per due fattori. In questa sezione viene descritto un metodo di esempio per eseguire la conversione. Il metodo presuppone che le immagini video siano Progressive Scan.

> [!Note]  
> Il processo di conversione dell'analisi interlacciata da 4:2:0 a 4:2:2 presenta problemi atipici ed è difficile da implementare. Questo articolo non risolve il problema di conversione dell'analisi interlacciata da 4:2:0 a 4:2:2.

 

Consentire a ogni riga verticale di input Chroma samples di essere una matrice `Cin[]` compresa tra 0 e N-1. La linea verticale corrispondente nell'immagine di output sarà una matrice `Cout[]` che varia da 0 a 2n-1. Per convertire ogni linea verticale, eseguire il processo seguente:

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

dove clip () indica il ritaglio a un intervallo compreso tra \[ 0 e 255 \] .

> [!Note]  
> Le equazioni per la gestione dei bordi possono essere matematicamente semplificate. Vengono mostrati in questo modulo per illustrare l'effetto di bloccaggio ai bordi dell'immagine.

 

In effetti, questo metodo calcola ogni valore mancante interpolando la curva sui quattro pixel adiacenti, ponderata in base ai valori dei due pixel più vicini (Figura 11). Il metodo di interpolazione specifico usato in questo esempio genera esempi mancanti in posizioni a metà Integer usando un metodo noto denominato interpolazione Catmull-Rom, nota anche come interpolazione della convoluzione cubica.

![Figura 11. diagramma che mostra il campionamento da 4:2:0 a 4:2:2](images/yuvformats14.gif)

Nei termini di elaborazione dei segnali, la conversione verticale dovrebbe includere idealmente una compensazione dello spostamento della fase per tenere conto dell'offset verticale di metà pixel (rispetto alla griglia di campionamento 4:2:2 di output) tra i percorsi delle righe di esempio 4:2:0 e la posizione di ogni altra riga di esempio 4:2:2. Tuttavia, l'introduzione di questo offset aumenterebbe la quantità di elaborazione necessaria per generare gli esempi e renderà impossibile ricostruire gli esempi originali 4:2:0 dall'immagine 4:2:2 sottocampionata. Potrebbe anche non essere possibile decodificare il video direttamente in superfici di 4:2:2 e quindi usare tali superfici come immagini di riferimento per la decodifica delle immagini successive nel flusso. Pertanto, il metodo fornito qui non prende in considerazione l'allineamento verticale preciso degli esempi. Questa operazione non è probabilmente visivamente dannosa per risoluzioni di immagini ragionevolmente elevate.

Se si inizia con 4:2:0 video che usa la griglia di campionamento definita nel video H. 261, H. 263 o MPEG-1, la fase degli esempi di Chroma di output 4:2:2 verrà spostata anche da un offset orizzontale a metà pixel rispetto alla spaziatura nella griglia di campionamento luma (un offset di quarto pixel rispetto alla spaziatura della griglia di campionamento Chroma 4:2:2). Tuttavia, il formato MPEG-2 di 4:2:0 video è probabilmente usato più di frequente nei PC e non subisce questo problema. Inoltre, la distinzione non è probabilmente visivamente dannosa per risoluzioni di immagini ragionevolmente elevate. Il tentativo di correggere questo problema creerebbe lo stesso tipo di problemi trattati per l'offset della fase verticale.

## <a name="converting-422-yuv-to-444-yuv"></a>Conversione da 4:2:2 YUV a 4:4:4 YUV

Per la conversione da YUV a 4:2:2 YUV a 4:4:4 YUV è necessaria una conversione orizzontale per due fattori. Il metodo descritto in precedenza per la conversione verticale può essere applicato anche alla conversione orizzontale. Per il video MPEG-2 e ITU-R BT. 601, questo metodo produrrà esempi con l'allineamento della fase corretto.

## <a name="converting-420-yuv-to-444-yuv"></a>Conversione da 4:2:0 YUV a 4:4:4 YUV

Per convertire 4:2:0 YUV a 4:4:4 YUV, è possibile seguire semplicemente i due metodi descritti in precedenza. Convertire l'immagine 4:2:0 in 4:2:2 e quindi convertire l'immagine 4:2:2 in 4:4:4. È anche possibile cambiare l'ordine dei due processi di conversione, perché l'ordine di operazione non è rilevante per la qualità visiva del risultato.

## <a name="other-yuv-formats"></a>Altri formati YUV

Altri formati YUV meno comuni includono i seguenti:

-   AI44 è un formato YUV pallettizzati con 8 bit per campione. Ogni esempio contiene un indice nei 4 bit più significativi (MSBs) e un valore alfa nei 4 bit meno significativi (LSB). L'indice fa riferimento a una matrice di voci della tavolozza YUV, che devono essere definite nel tipo di supporto per il formato. Questo formato viene utilizzato principalmente per le immagini di sottoimmagine.
-   NV11 è un formato Planar 4:1:1 con 12 bit per pixel. Gli esempi Y vengono visualizzati per primi in memoria. Il piano Y è seguito da una matrice di campioni U (CB) e V (CR) compressi. Quando l'array U-V combinato viene considerato come una matrice di valori di **parola** little-endian, gli esempi u sono contenuti nel LSB di ogni **parola** e gli esempi V sono contenuti in MSBs. Questo layout di memoria è simile a NV12, anche se il campionamento Chroma è diverso.
-   Y41P è un formato compresso 4:1:1, con l'utente e la V campionati ogni quarto pixel orizzontalmente. Ogni macropixel contiene 8 pixel in tre byte, con il seguente layout di byte: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T è identico a Y41P, ad eccezione del bit meno significativo di ogni esempio Y che specifica il tasto Chroma (0 = transparent, 1 = opaque).
-   Y42T è identico a UYVY, ad eccezione del bit meno significativo di ogni esempio Y che specifica il tasto Chroma (0 = transparent, 1 = opaque).
-   YVYU è equivalente a YUYV, ad eccezione del fatto che gli esempi di i e V sono stati scambiati.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identificazione dei formati YUV in Media Foundation

Per ognuno dei formati YUV descritti in questo articolo è stato assegnato un codice FOURCC. Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.

Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente. La macro **MAKEFOURCC** , ad esempio, è dichiarata in mmsystem. h e la macro **FCC** è dichiarata in Aviriff. h. Utilizzarli come indicato di seguito:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri. Ad esempio:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

Invertire l'ordine è necessario perché il sistema operativo Windows usa un'architettura little-endian. ' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.

In Media Foundation i formati sono identificati da un GUID di tipo principale e da un GUID del sottotipo. Il tipo principale per i formati video del computer è sempre \_ video MFMediaType. Il sottotipo può essere costruito eseguendo il mapping del codice FOURCC a un GUID, come indicato di seguito:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

dove `XXXXXXXX` è il codice FourCC. Pertanto, il GUID del sottotipo per YUY2 è:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Le costanti per i GUID di formato YUV più comuni sono definite nel file di intestazione mfapi. h. Per un elenco di queste costanti, vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video su YUV](about-yuv-video.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 



