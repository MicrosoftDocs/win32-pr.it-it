---
description: Il codificatore Windows Media Video 9 codifica i flussi video.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Windows Codificatore Media Video 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d3d3e7feb06cfbe9e9149fd9fd55d76ecf5abe2fbe0d6eea6ac961a0561ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398241"
---
# <a name="windows-media-video-9-encoder"></a>Windows Codificatore video multimediale 9

Il codificatore Windows Media Video 9 codifica i flussi video. Il codificatore supporta le quattro categorie seguenti di output codificato.

-   Windows Profilo semplice di Media Video 9
-   Windows Profilo principale di Media Video 9
-   Windows Profilo avanzato di Media Video 9
-   Windows Immagine di Media Video 9.1

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMV9EncMediaObject**. È possibile creare un'istanza del codificatore video chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto codificatore video espone [**l'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come oggetto directx media (DMO) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un codificatore video si comporta come DMO o MFT a seconda delle interfacce che si ottengono e della versione Windows in esecuzione. La tabella seguente illustra le condizioni in cui un codificatore video si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del codificatore                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows video encoder multimediale si comporta sempre come DMO.                                                                                                                |
| Windows Vista e Windows 7 | Per impostazione predefinita, Windows codificatore video multimediale si comporta come DMO. Se si ottiene [**un'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un codificatore video, si comporta come un MFT. |



 

## <a name="input-formats"></a>Formati di input

Il Windows Media Video encoder supporta i sottotipi multimediali di input seguenti quando funge da DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

Il Windows media video supporta i sottotipi multimediali di input seguenti quando funge da MFT.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i codici a quattro caratteri (FOURCC) che corrispondono alle categorie di output codificato.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Profilo semplice di Media Video 9   | "WMV3"                                   |
| Windows Profilo principale di Media Video 9     | "WMV3"                                   |
| Windows Profilo avanzato di Media Video 9 | "WVC1"                                   |
| Windows Immagine di Media Video 9.1          | "WMVP" per la versione 9.1, "WVP2" per la versione 9.1 2 |



 

Per distinguere tra Profilo semplice e Profilo principale, impostare la [**proprietà MFPKEY \_ DECODERCOMPLEXITYREQUESTED.**](mfpkey-decodercomplexityrequestedproperty.md)

## <a name="properties"></a>Proprietà

Il Windows Media Video 9 supporta le proprietà seguenti.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>Specifica il sovraccarico, in byte per pacchetto, necessario per il contenitore utilizzato per archiviare il contenuto compresso.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Specifica la frequenza media dei fotogrammi del contenuto video, in fotogrammi al secondo.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso a velocità in bit variabile vincolata (VBR) alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Specifica l'aumento differenziale tra il quantizer dell'immagine della cornice di ancoraggio e il quantizer dell'immagine del fotogramma B.<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso a velocità in bit variabile vincolata (VBR) alla velocità in bit massima (specificata <a href="mfpkey-rmaxproperty.md"><strong>da MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Specifica il modello di codifica da utilizzare all'inizio di un gruppo di immagini.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente dati.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>Questa proprietà viene sostituita da <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>Specifica la complessità dell'algoritmo del codificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale. Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Specifica il tipo di ottimizzazione da usare per il codec Windows Media Video 9 Advanced Profile.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Specifica una rappresentazione numerica del compromesso tra l'uniformità del movimento e la qualità dell'immagine nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Non usato.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Specifica il modello di conformità del dispositivo a cui è conforme il contenuto codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Specifica il modello di conformità del dispositivo da usare per la codifica video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Specifica il metodo utilizzato per codificare le informazioni sul vettore di movimento.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Specifica se il codec userà il filtro disturbo durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità desiderato per la codifica a velocità variabile (VBR) basata sulla qualità (1 passaggio).<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video eliminati durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Specifica la fine di un passaggio di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Specifica un'altezza intermedia del fotogramma per il video codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Specifica una larghezza intermedia del fotogramma per il video codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Specifica se il codec deve usare il filtro mediano durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Specifica l'elemento FOURCC che identifica il codificatore che si vuole usare.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Obsoleta.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Specifica se al codificatore è consentito rilasciare fotogrammi.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Specifica se l'output del codec verrà interlacciato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Specifica il tempo massimo, in millisecondi, tra fotogrammi chiave nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>Non usato.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Specifica se il codec deve usare il filtro di deblocking nel ciclo durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Specifica il metodo di costo usato dal codec per determinare la modalità macroblock da usare.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Specifica il metodo da utilizzare per la corrispondenza del movimento.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Specifica i tipi di informazioni video usate nelle operazioni di ricerca del movimento.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Specifica l'intervallo usato nelle ricerche in movimento.<br/> <dl> Windows XP e versioni successive.<br />
Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Specifica se il codec deve tentare di rilevare i bordi dei fotogrammi rumorosi e rimuoverli.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi predittivi bidirezionali (fotogrammi B).<br/> <dl> Windows XP e versioni successive.<br />
Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Specifica il numero di thread che il codec userà per la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Specifica il numero massimo di passaggi supportati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Specifica il numero di passaggi che il codec userà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Specifica se il codificatore produce voci di fotogrammi fittizi nel flusso di bit per i fotogrammi duplicati.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Specifica QP.<br/> <dl> Windows Vista e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Specifica il grado in base al quale il codec deve ridurre l'intervallo di colori effettivo del video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Specifica la velocità in bit media, in bit al secondo, usata per la codifica VBR (Variable-Bit Rate) a 2 passi.<br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato).<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Specifica se il codificatore usa la ricerca MV secondaria basata su RD. <br/> <dl> Windows XP e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Per la ri codifiche dei segmenti, specifica le dimensioni del buffer.<br/> <dl> Windows Vista e versioni successive.<br />
Simple Profile (Profilo semplice), Main Profile (Profilo principale), Advanced Profile (Profilo avanzato), Image (Immagine).<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Per la ri-codifica dei segmenti, specifica la durata del segmento da ri-codificare.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Per la ri-codifica dei segmenti, specifica il quantizer del frame prima del segmento iniziale.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Per la ri-codifica dei segmenti, specifica la completezza iniziale del buffer.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Specifica la velocità in bit di picco, in bit al secondo, usata per la velocità in bit variabile a 2 passi vincolata (VBR).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Specifica se il codec userà la codifica VBR (Variable-Bit-Rate).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità effettivo per la codifica a velocità variabile (VBR) basata sulla qualità (1 passaggio).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Specifica se il codec userà l'ottimizzazione del ridimensionamento video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Specifica la quantità di contenuto, in millisecondi, che può essere inserito nel buffer del modello.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Per la ri-codifica dei segmenti, specifica i dati privati del codec del file da ri-codificare.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>Specifica il tipo di logica che il codec userà per rilevare il video di origine interlacciato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video ignorati perché erano duplicati dei fotogrammi precedenti.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, Profilo principale, Profilo avanzato.<br />
Sola lettura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione di codec](codecimplementation.md)
</dt> </dl>

 

 
