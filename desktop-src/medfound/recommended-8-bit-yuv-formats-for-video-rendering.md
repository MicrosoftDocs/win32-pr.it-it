---
description: Formati YUV a 8 bit consigliati per il rendering video
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formati YUV a 8 bit consigliati per il rendering video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6e30f33c59bedf9a2e842d2d33328bd97d8078d21bda90ae84af9af00ec113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722135"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formati YUV a 8 bit consigliati per il rendering video

Gary e Stephen Estrop

Microsoft Corporation

Aprile 2002, aggiornato a novembre 2008

Questo argomento descrive i formati di colore YUV a 8 bit consigliati per il rendering video nel Windows operativo. Questo articolo presenta le tecniche per la conversione tra formati YUV e RGB e fornisce anche tecniche per l'upsampling dei formati YUV. Questo articolo è destinato a chiunque lavori con la decodifica video YUV o il rendering in Windows.

## <a name="introduction"></a>Introduzione

In tutto il settore video sono definiti numerosi formati YUV. Questo articolo identifica i formati YUV a 8 bit consigliati per il rendering video in Windows. I fornitori di decodificatori e i fornitori di display sono invitati a supportare i formati descritti in questo articolo. Questo articolo non tratta altri usi del colore YUV, ad esempio la fotografia.

I formati descritti in questo articolo usano tutti 8 bit per posizione pixel per codificare il canale Y (chiamato anche canale luma) e usano 8 bit per campione per codificare ogni campione di chroma U o V. Tuttavia, la maggior parte dei formati YUV usa in media meno di 24 bit per pixel, perché contengono meno campioni dell'utente e della V rispetto a Y. Questo articolo non illustra i formati YUV con canali Y a 10 bit o superiori.

> [!Note]  
> Ai fini di questo articolo, il termine U equivale a Cb e il termine V è equivalente a Cr.

 

Questo articolo include gli argomenti seguenti:

-   [Campionamento YUV](#yuv-sampling). Descrive le tecniche di campionamento YUV più comuni.
-   [Definizioni di superficie](#surface-definitions). Descrive i formati YUV consigliati.
-   [Conversioni dello spazio colore e della frequenza di campionamento di Chroma](#color-space-and-chroma-sampling-rate-conversions). Fornisce alcune linee guida per la conversione tra formati YUV e RGB e per la conversione tra formati YUV diversi.
-   [Identificazione dei formati YUV in Media Foundation](#identifying-yuv-formats-in-media-foundation). Viene illustrato come descrivere i tipi di formato YUV in Media Foundation.

## <a name="yuv-sampling"></a>Campionamento YUV

I canali chroma possono avere una frequenza di campionamento inferiore rispetto al canale luma, senza una perdita notevole di qualità percettiva. Una notazione denominata "A:B:C" viene usata per descrivere la frequenza con cui si e V vengono campionati rispetto a Y:

-   4:4:4 indica nessun downsampling dei canali chroma.
-   4:2:2 indica il downsampling orizzontale 2:1, senza downsampling verticale. Ogni riga di analisi contiene quattro campioni Y per ogni due campioni U o V.
-   4:2:0 indica il downsampling orizzontale 2:1, con downsampling verticale 2:1.
-   4:1:1 indica il downsampling orizzontale 4:1, senza downsampling verticale. Ogni riga di analisi contiene quattro esempi Y per ogni campione di tipo you e V. Il campionamento 4:1:1 è meno comune rispetto ad altri formati e non viene descritto in dettaglio in questo articolo.

I diagrammi seguenti illustrano come viene campionata la croma per ognuna delle percentuali di downsampling. I campioni di Luma sono rappresentati da una croce e i campioni di chroma sono rappresentati da un cerchio.

![figura 1. campionamento di chroma](images/yuv-sampling-grids.png)

La forma dominante del campionamento 4:2:2 è definita nella raccomandazione ITU-R BT.601. Esistono due varianti comuni del campionamento 4:2:0. Uno di questi viene usato nel video MPEG-2 e l'altro in MPEG-1 e in ITU-T Consigli H.261 e H.263.

Rispetto allo schema MPEG-1, è più semplice eseguire la conversione tra lo schema MPEG-2 e le griglie di campionamento definite per i formati 4:2:2 e 4:4:4. Per questo motivo, lo schema MPEG-2 è preferibile in Windows e deve essere considerato l'interpretazione predefinita dei formati 4:2:0.

## <a name="surface-definitions"></a>Definizioni di superficie

Questa sezione descrive i formati YUV a 8 bit consigliati per il rendering video. Questi rientrano in diverse categorie:

-   [Formati 4:4:4, 32 bit per pixel](#444-formats-32-bits-per-pixel)
-   [Formati 4:2:2, 16 bit per pixel](#422-formats-16-bits-per-pixel)
-   [Formati 4:2:0, 16 bit per pixel](#420-formats-16-bits-per-pixel)
-   [Formati 4:2:0, 12 bit per pixel](#420-formats-12-bits-per-pixel)

Prima di tutto, è necessario tenere presenti i concetti seguenti per comprendere quanto segue:

-   *Origine della superficie*. Per i formati YUV descritti in questo articolo, l'origine (0,0) è sempre l'angolo superiore sinistro della superficie.
-   *Stride*. Lo stride di una superficie, talvolta chiamato passo, è la larghezza della superficie in byte. Data l'origine della superficie nell'angolo superiore sinistro, lo stride è sempre positivo.
-   *Allineamento*. L'allineamento di una superficie è a discrezione del driver di visualizzazione grafica. La superficie deve essere sempre allineata con DWORD. ovvero è garantito che le singole righe all'interno della superficie hanno origine su un limite DWORD (32 bit). L'allineamento può tuttavia essere maggiore di 32 bit, a seconda delle esigenze dell'hardware.
-   Formato pacchetto rispetto al formato planare. I formati YUV sono suddivisi *in formati pack e* *planari.* In formato pack, i componenti Y, U e V vengono archiviati in un'unica matrice. I pixel sono organizzati in gruppi di macropixel, il cui layout dipende dal formato. In formato planare, i componenti Y, U e V vengono archiviati come tre piani separati.

A ognuno dei formati YUV descritti in questo articolo è assegnato un codice FOURCC. Un codice FOURCC è un intero senza segno a 32 bit creato concatenando quattro caratteri ASCII.

-   4:4:4 (32 bpp)
    -   [AYUV](#ayuv)
-   4:2:2 (16 bpp)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 bpp)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 bpp)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>Formati 4:4:4, 32 bit per pixel

### <a name="ayuv"></a>AYUV

È consigliabile un singolo formato 4:4:4, con il codice FOURCC AYUV. Si tratta di un formato compresso, in cui ogni pixel viene codificato come quattro byte consecutivi, disposti nella sequenza illustrata nella figura seguente.

![figura 2. layout della memoria ayuv](images/yuvformats01.gif)

I byte contrassegnati con A contengono valori per alpha.

## <a name="422-formats-16-bits-per-pixel"></a>Formati 4:2:2, 16 bit per pixel

Sono consigliati due formati 4:2:2, con i codici FOURCC seguenti:

-   YUY2
-   UYVY

Entrambi sono formati compressi, in cui ogni macropixel è di due pixel codificati come quattro byte consecutivi. Ciò comporta un downsampling orizzontale della chroma di un fattore di due.

### <a name="yuy2"></a>YUY2

Nel formato YUY2, i dati possono essere  considerati come una matrice di valori char senza segno, in cui il primo byte contiene il primo esempio Y, il secondo byte contiene il primo esempio U (Cb), il terzo byte contiene il secondo campione Y e il quarto byte contiene il primo campione V (Cr), come illustrato nel diagramma seguente.

![figura 3. Layout di memoria yuy2](images/yuvformats02.gif)

Se l'immagine viene indirizzata come matrice  di valori **WORD** little-endian, la prima parola contiene il primo campione Y nei bit meno significativi (LSB) e il primo campione U (Cb) nei bit più significativi (MSB). La seconda **parola** contiene il secondo esempio Y nelle LSB e il primo esempio V (Cr) nei database MSB.

YUY2 è il formato 4:2:2 pixel preferito per l'accelerazione video Microsoft DirectX (DirectX VA). Si prevede che sia un requisito a termine intermedio per gli acceleratori DirectX VA che supportano video 4:2:2.

### <a name="uyvy"></a>UYVY

Questo formato è lo stesso del formato YUY2, ad eccezione del fatto che l'ordine dei byte viene invertito, ovvero i byte chroma e luma vengono capovolti (Figura 4). Se l'immagine viene indirizzata come matrice di due valori **WORD** little-endian, la prima **parola** contiene U nei LSB e Y0 nei MSB e la seconda **PAROLA** contiene V nei LSB e Y1 nei BLOB.

![figura 4. Layout della memoria uyvy](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>Formati 4:2:0, 16 bit per pixel

Sono consigliati due formati 4:2:0 a 16 bit per pixel (bpp), con i codici FOURCC seguenti:

-   IMC1
-   IMC3

Entrambi questi formati YUV sono formati planari. I canali chroma vengono sottocampionati in base a un fattore di due nelle dimensioni orizzontale e verticale.

### <a name="imc1"></a>IMC1

Tutti gli esempi Y vengono visualizzati per primi in memoria come matrice di valori **char senza** segno. Questo è seguito da tutti gli esempi V (Cr) e quindi da tutti gli esempi U (Cb). I piani V e U hanno lo stesso passo del piano Y, determinando aree di memoria inutilizzate, come illustrato nella figura 5. I piani you e V devono iniziare sui limiti di memoria che sono un multiplo di 16 righe. La figura 5 mostra l'origine dell'utente e di V per un fotogramma video 352 x 240. L'indirizzo iniziale dei piani you e V viene calcolato come segue:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

dove *pY* è un puntatore di byte all'inizio della matrice di memoria, come illustrato nel diagramma seguente.

![figura 5. Layout di memoria imc1 (esempio)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Questo formato è identico a IMC1, ad eccezione del fatto che i piani you e V vengono scambiati, come illustrato nel diagramma seguente.

![figura 6. Layout di memoria imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>Formati 4:2:0, 12 bit per pixel

Sono consigliati quattro formati 4:2:0 da 12 bpp, con i codici FOURCC seguenti:

-   IMC2
-   IMC4
-   YV12
-   NV12

In tutti questi formati, i canali chroma vengono sottocampionati in base a un fattore di due nelle dimensioni orizzontale e verticale.

### <a name="imc2"></a>IMC2

Questo formato è lo stesso di IMC1 ad eccezione della differenza seguente: le linee V (Cr) e U (Cb) vengono interfoliate ai limiti a metà passo. In altre parole, ogni riga a passo intero nell'area chroma inizia con una riga di esempi V, seguita da una riga di esempi U che inizia in corrispondenza del limite a metà passo successivo (Figura 7). Questo layout rende più efficiente l'uso dello spazio degli indirizzi rispetto a IMC1. Riduce a metà lo spazio degli indirizzi chroma e quindi lo spazio indirizzi totale del 25%. Tra i formati 4:2:0, IMC2 è il secondo formato preferito, dopo NV12. L'immagine seguente illustra questo processo.

![figura 7. Layout di memoria imc2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Questo formato è identico a IMC2, ad eccezione delle righe U (Cb) e V (Cr), come illustrato nella figura seguente.

![figura 8. Layout di memoria imc4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Tutti gli esempi Y vengono visualizzati per primi in memoria come matrice di valori **char senza** segno. Questa matrice è seguita immediatamente da tutti gli esempi V (Cr). Lo stride del piano V è metà del passo del piano Y; e il piano V contiene metà delle linee del piano Y. Il piano V è seguito immediatamente da tutti gli esempi U (Cb), con lo stesso passo e lo stesso numero di linee del piano V, come illustrato nella figura seguente.

![figura 9. Layout della memoria yv12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Tutti gli esempi Y vengono visualizzati per primi in memoria come matrice di valori **char** senza segno con un numero pari di righe. Il piano Y è seguito immediatamente da una matrice di valori **char** senza segno che contiene esempi di U (Cb) e V (Cr) imballati. Quando la matrice U-V combinata viene indirizzata come matrice di valori **WORD** little-endian, i LSB contengono i valori U e i valori V. NV12 è il formato 4:2:0 pixel preferito per DirectX VA. Si prevede che sia un requisito a termine intermedio per gli acceleratori DirectX VA che supportano il video 4:2:0. La figura seguente mostra il piano Y e la matrice che contiene gli esempi packed you e V.

![figura 10. Layout di memoria nv12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversioni dello spazio colore e della frequenza di campionamento di Chroma

Questa sezione fornisce linee guida per la conversione tra YUV e RGB e per la conversione tra alcuni formati YUV diversi. In questa sezione vengono valutati due schemi di codifica RGB: RGB del computer a *8 bit,* noto anche come RGB sRGB o RGB "full-scale" e RGB video di *studio,* o "RGB con head-room e toe-room". Questi sono definiti come segue:

-   RGB del computer usa 8 bit per ogni campione di rosso, verde e blu. Il nero è rappresentato da R = G = B = 0 e il bianco è rappresentato da R = G = B = 255.
-   RGB video di Studio usa un certo numero di bit N per ogni campione di rosso, verde e blu, dove N è 8 o più. RGB video di Studio usa un fattore di scala diverso rispetto a RGB del computer e ha un offset. Il nero è rappresentato da R = G = B = 16 2^(N-8) e il bianco è rappresentato da \* R = G = B = 235 \* 2^(N-8). Tuttavia, i valori effettivi possono non rientrare in questo intervallo.

RGB video di Studio è la definizione RGB preferita per il video in Windows, mentre RGB del computer è la definizione RGB preferita per le applicazioni non video. In entrambi i tipi di RGB, le coordinate di cromaticità sono specificate in ITU-R BT.709 per la definizione dei colori primari RGB. Le coordinate (x,y) di R, G e B sono rispettivamente (0,64, 0,33), (0,30, 0,60) e (0,15, 0,06). Il bianco di riferimento è D65 con coordinate (0,3127, 0,3290). La gamma nominale è 1/0,45 (circa 2,2), con gamma precisa definita in dettaglio in ITU-R BT.709.

**Conversione tra RGB e 4:4:4 YUV**

Prima di tutto viene descritta la conversione tra RGB e 4:4:4 YUV. Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4:4 YUV a RGB. Il formato AYUV, che è un formato 4:4:4, usa 8 bit ciascuno per gli esempi Y, U e V. È anche possibile definire YUV usando più di 8 bit per campione per alcune applicazioni.

Per il video digitale sono state definite due conversioni YUV dominanti da RGB. Entrambi si basano sulla specifica nota come ITU-R Recommendation BT.709. La prima conversione è il modulo YUV precedente definito per l'uso a 50 Hz in BT.709. Corrisponde alla relazione specificata nella raccomandazione ITU-R BT.601, nota anche con il nome precedente, CCIR 601. Deve essere considerato il formato YUV preferito per la risoluzione TV a definizione standard (720 x 576) e il video a risoluzione inferiore. È caratterizzato dai valori di due costanti *Kr* e *Kb*:

``` syntax
Kr = 0.299
Kb = 0.114
```

La seconda conversione è il modulo YUV più recente definito per l'uso a 60 Hz in BT.709 e deve essere considerato il formato preferito per le risoluzioni video sopra SDTV. È caratterizzato da valori diversi per queste due costanti:

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
-   Z è la variabile di livello nero. Per il computer RGB, Z è uguale a 0. Per RGB video di studio, Z equivale a 16 2^(N-8), dove N è il numero di bit per campione \* RGB (N >= 8).
-   S è la variabile di ridimensionamento. Per il computer RGB, S è uguale a 255. Per RGB video studio, S è uguale a 219 \* 2^(N-8).

La funzione floor(x) restituisce l'intero più grande minore o uguale a x. La funzione clip3(x, y, z) è definita come segue:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> Clip3 deve essere implementato come funzione anziché come macro del preprocessore. In caso contrario, verranno eseguite più valutazioni degli argomenti.

 

Il campione Y rappresenta la luminosità e i campioni you e V rappresentano rispettivamente le deviazioni di colore verso il blu e il rosso. L'intervallo nominale per Y è compreso tra \* 16 2^(M-8) e 235 \* 2^(M-8). Il nero è rappresentato come 16 2^(M-8) e il bianco è rappresentato come \* 235 \* 2^(M-8). L'intervallo nominale per l'utente e V è compreso tra 16 \* 2^(M-8) e 240 \* 2^(M-8), con il valore 128 \* 2^(M-8) che rappresenta la chroma neutra. Tuttavia, i valori effettivi possono non rientrare in questi intervalli.

Per i dati di input sotto forma di RGB video di Studio, l'operazione di ritaglio è necessaria per mantenere i valori you e V nell'intervallo da 0 a (2^M)-1. Se l'input è RGB del computer, l'operazione di ritaglio non è necessaria, perché la formula di conversione non può produrre valori al di fuori di questo intervallo.

Queste sono le formule esatte senza approssimazione. Tutto ciò che segue in questo documento deriva da queste formule. In questa sezione vengono descritte le conversioni seguenti:

-   [Conversione di RGB888 in YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Conversione di YUV a 8 bit in RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Conversione da 4:2:0 YUV a 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Conversione da 4:2:2 YUV a 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Conversione da 4:2:0 YUV a 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Conversione di RGB888 in YUV 4:4:4

Nel caso dell'input RGB del computer e dell'output YUV BT.601 a 8 bit, si ritiene che le formule fornite nella sezione precedente possano essere ragionevolmente approssimate nel modo seguente:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Queste formule producono risultati a 8 bit usando coefficienti che non richiedono più di 8 bit di precisione (senza segno). I risultati intermedi richiederanno fino a 16 bit di precisione.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Conversione di YUV a 8 bit in RGB888

Dalle formule RGB-YUV originali, è possibile derivare le relazioni seguenti per BT.601.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Di conseguenza, dato:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

Le formule per convertire YUV in RGB possono essere derivate come segue:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

dove `clip()` indica il ritaglio in un intervallo di \[ 0,.255 \] . Si ritiene che queste formule possano essere ragionevolmente approssimate nel modo seguente:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Queste formule usano alcuni coefficienti che richiedono più di 8 bit di precisione per produrre ogni risultato a 8 bit e i risultati intermedi richiedono più di 16 bit di precisione.

Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4 YUV a RGB. Le sezioni seguenti illustrano alcuni metodi per la conversione dei formati 4:2:0 e 4:2:2 in 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Conversione da 4:2:0 YUV a 4:2:2 YUV

La conversione da 4:2:0 YUV a 4:2:2 YUV richiede l'upconversione verticale di un fattore di due. In questa sezione viene descritto un metodo di esempio per l'esecuzione dell'upconversion. Il metodo presuppone che le immagini video siano digitalizzare progressivamente.

> [!Note]  
> Il processo di conversione dell'analisi interlacciata da 4:2:0 a 4:2:2 presenta problemi atipici ed è difficile da implementare. Questo articolo non tratta il problema della conversione dell'analisi interlacciata da 4:2:0 a 4:2:2.

 

Lasciare che ogni riga verticale dei campioni di chroma di input sia una matrice che va `Cin[]` da 0 a N - 1. La linea verticale corrispondente nell'immagine di output sarà una matrice che va da 0 a `Cout[]` 2N - 1. Per convertire ogni linea verticale, seguire questa procedura:

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

dove clip() indica il ritaglio in un intervallo di \[ 0,.255 \] .

> [!Note]  
> Le equazioni per la gestione degli bordi possono essere matematicamente semplificate. Vengono visualizzati in questo modulo per illustrare l'effetto di chiusura ai bordi dell'immagine.

 

In effetti, questo metodo calcola ogni valore mancante interpolando la curva sui quattro pixel adiacenti, ponderati verso i valori dei due pixel più vicini (Figura 11). Il metodo di interpolazione specifico usato in questo esempio genera campioni mancanti in posizioni di mezzo integer usando un metodo noto denominato interpolazione Catmull-Rom, noto anche come interpolazione convoluzione cubica.

![Figura 11. Diagramma che mostra l'upsampling da 4:2:0 a 4:2:2](images/yuvformats14.gif)

In termini di elaborazione dei segnali, l'upconversione verticale deve idealmente includere una compensazione dello spostamento di fase per prendere in considerazione l'offset verticale di mezzo pixel (rispetto alla griglia di campionamento 4:2:2 di output) tra le posizioni delle linee di campionamento 4:2:0 e la posizione di ogni altra linea di campionamento 4:2:2. Tuttavia, l'introduzione di questo offset aumenterà la quantità di elaborazione necessaria per generare i campioni e renderebbe impossibile ricostruire i campioni 4:2:0 originali dall'immagine 4:2:2 ricampionata. Renderebbe anche impossibile decodificare i video direttamente in superfici 4:2:2 e quindi usarle come immagini di riferimento per decodificare le immagini successive nel flusso. Pertanto, il metodo qui fornito non prende in considerazione l'allineamento verticale preciso degli esempi. Questa operazione probabilmente non è visivamente dannosa a risoluzioni dell'immagine ragionevolmente elevate.

Se si inizia con un video 4:2:0 che usa la griglia di campionamento definita nel video H.261, H.263 o MPEG-1, anche la fase dei campioni di chroma di output 4:2:2 verrà spostata di un offset orizzontale di mezzo pixel rispetto alla spaziatura nella griglia di campionamento luma (offset di quattro pixel rispetto alla spaziatura della griglia di campionamento di 4:2:2 chroma). Tuttavia, il formato MPEG-2 del video 4:2:0 è probabilmente più comunemente usato nei PC e non subisce questo problema. Inoltre, la distinzione probabilmente non è visivamente dannosa a risoluzioni dell'immagine ragionevolmente elevate. Il tentativo di risolvere questo problema creerebbe lo stesso tipo di problemi illustrati per l'offset della fase verticale.

## <a name="converting-422-yuv-to-444-yuv"></a>Conversione da 4:2:2 YUV a 4:4:4 YUV

La conversione da 4:2:2 YUV a 4:4:4 YUV richiede l'upconversione orizzontale di un fattore di due. Il metodo descritto in precedenza per l'upconversion verticale può essere applicato anche all'upconversion orizzontale. Per il video MPEG-2 e ITU-R BT.601, questo metodo produrrà campioni con l'allineamento di fase corretto.

## <a name="converting-420-yuv-to-444-yuv"></a>Conversione da 4:2:0 YUV a 4:4:4 YUV

Per convertire 4:2:0 YUV in 4:4:4 YUV, è sufficiente seguire i due metodi descritti in precedenza. Convertire l'immagine 4:2:0 in 4:2:2 e quindi convertire l'immagine 4:2:2 in 4:4:4. È anche possibile cambiare l'ordine dei due processi di conversione, perché l'ordine delle operazioni non è realmente importante per la qualità visiva del risultato.

## <a name="other-yuv-formats"></a>Altri formati YUV

Di seguito sono riportati alcuni altri formati YUV meno comuni:

-   AI44 è un formato YUV con 8 bit per campione. Ogni esempio contiene un indice nei 4 bit più significativi (MSB) e un valore alfa nei 4 bit meno significativi (LSB). L'indice fa riferimento a una matrice di voci della tavolozza YUV, che devono essere definite nel tipo di supporto per il formato. Questo formato viene usato principalmente per le immagini di sotto-immagine.
-   NV11 è un formato planare 4:1:1 con 12 bit per pixel. Gli esempi Y vengono visualizzati per primi in memoria. Il piano Y è seguito da una matrice di esempi di U (Cb) e V (Cr) imballati. Quando la matrice U-V combinata viene indirizzata come matrice di valori **WORD** little-endian, gli esempi U sono contenuti nei LSB di ogni **PAROLA** e gli esempi V sono contenuti nei file MSB. Questo layout di memoria è simile a NV12 anche se il campionamento della chroma è diverso.
-   Y41P è un formato packed 4:1:1, con l'utente e V campionati orizzontalmente ogni quarto pixel. Ogni macropixel contiene 8 pixel in tre byte, con il layout di byte seguente: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T è identico a Y41P, ad eccezione del bit meno significativo di ogni campione Y che specifica la chiave chroma (0 = trasparente, 1 = opaco).
-   Y42T è identico a UYVY, ad eccezione del bit meno significativo di ogni campione Y che specifica la chiave chroma (0 = trasparente, 1 = opaco).
-   YVYU equivale a YUYV, ad eccezione del fatto che gli esempi you e V vengono scambiati.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identificazione dei formati YUV in Media Foundation

A ognuno dei formati YUV descritti in questo articolo è assegnato un codice FOURCC. Un codice FOURCC è un intero senza segno a 32 bit creato concatenando quattro caratteri ASCII.

Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente. Ad esempio, la macro **MAKEFOURCC** viene dichiarata in Mmsystem.h e la macro **FCC** viene dichiarata in Aviriff.h. Usarli come indicato di seguito:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

È anche possibile dichiarare un codice FOURCC direttamente come valore letterale stringa semplicemente invertindo l'ordine dei caratteri. Esempio:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

L'invertimento dell'ordine è necessario perché Windows sistema operativo usa un'architettura little-endian. 'Y' = 0x59, 'U' = 0x55 e '2' = 0x32, quindi '2YUY' è 0x32595559.

In Media Foundation i formati sono identificati da un GUID di tipo principale e da un GUID di sottotipo. Il tipo principale per i formati video dei computer è sempre MFMediaType \_ Video. Il sottotipo può essere costruito tramite il mapping del codice FOURCC a un GUID, come indicato di seguito:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

dove `XXXXXXXX` è il codice FOURCC. Di conseguenza, il GUID del sottotipo per YUY2 è:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Le costanti per i GUID di formato YUV più comuni sono definite nel file di intestazione mfapi.h. Per un elenco di queste costanti, vedere [GUID del sottotipo video.](video-subtype-guids.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su YUV Video](about-yuv-video.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 



