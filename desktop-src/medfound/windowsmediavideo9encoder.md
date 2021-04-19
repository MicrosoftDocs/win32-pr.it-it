---
description: Il codificatore Windows Media Video 9 codifica i flussi video.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Codificatore Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331569"
---
# <a name="windows-media-video-9-encoder"></a>Codificatore Windows Media Video 9

Il codificatore Windows Media Video 9 codifica i flussi video. Il codificatore supporta le quattro categorie di output codificate seguenti.

-   Profilo semplice Windows Media Video 9
-   Profilo principale Windows Media Video 9
-   Profilo avanzato Windows Media Video 9
-   Immagine di Windows Media Video 9,1

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMV9EncMediaObject**. È possibile creare un'istanza del codificatore video chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto del codificatore video espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un codificatore video si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore video si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del codificatore                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un codificatore Windows Media video si comporta sempre come DMO.                                                                                                                |
| Windows Vista e Windows 7 | Per impostazione predefinita, un codificatore video Windows Media si comporta come DMO. Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un codificatore video, si comporta come un MFT. |



 

## <a name="input-formats"></a>Formati di input

Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da DMO.

-   \_IYUV MEDIASUBTYPE
-   \_I420 MEDIASUBTYPE
-   \_YV12 MEDIASUBTYPE
-   \_NV11 MEDIASUBTYPE
-   \_NV12 MEDIASUBTYPE
-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_YVYU MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE
-   MEDIASUBTYPE \_ FOTOmotion

Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da MFT.

-   \_IYUV MFVideoFormat
-   \_I420 MFVideoFormat
-   \_YV12 MFVideoFormat
-   \_NV11 MFVideoFormat
-   \_NV12 MFVideoFormat
-   \_YUY2 MFVideoFormat
-   \_UYVY MFVideoFormat
-   \_YVYU MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_RGB24 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB555 MFVideoFormat
-   \_RGB8 MFVideoFormat
-   MEDIASUBTYPE \_ FOTOmotion

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i codici a quattro caratteri (fourcc) che corrispondono alle categorie di output codificato.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Profilo semplice Windows Media Video 9   | WMV3                                   |
| Profilo principale Windows Media Video 9     | WMV3                                   |
| Profilo avanzato Windows Media Video 9 | WVC1                                   |
| Immagine di Windows Media Video 9,1          | "WMVP" per 9,1, "WVP2" per 9,1 versione 2 |



 

Per distinguere tra profilo semplice e profilo principale, impostare la proprietà [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .

## <a name="properties"></a>Proprietà

Il codificatore Windows Media Video 9 supporta le seguenti proprietà.



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
<td>Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Specifica la frequenza media dei fotogrammi del contenuto video, in frame al secondo.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>Specifica il modello di codifica da usare all'inizio di un Group of Pictures.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
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
Profilo semplice, profilo principale. Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>Specifica il tipo di ottimizzazione da utilizzare per il codec del profilo avanzato Windows Media Video 9.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>Non usato.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Specifica il modello di conformità del dispositivo in cui è conforme il contenuto codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>Specifica il metodo usato per codificare le informazioni sul vettore di movimento.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>Specifica se il codec utilizzerà il filtro rumore durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video eliminati durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Specifica la fine di un passaggio di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>Specifica un'altezza del frame intermedia per il video codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>Specifica una larghezza del frame intermedia per il video codificato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>Specifica se il codec deve usare il filtro mediano durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>Obsoleta.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>Specifica se il codificatore può rilasciare frame.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Specifica se l'output del codec sarà interlacciato.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
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
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>Specifica il metodo da usare per la corrispondenza di movimento.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>Specifica i tipi di informazioni video utilizzate nelle operazioni di ricerca di movimento.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>Specifica l'intervallo usato nelle ricerche di movimento.<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>Specifica il numero di frame predittivi bidirezionali (fotogrammi B).<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>Specifica il numero di thread che il codec utilizzerà per la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Specifica il numero massimo di passaggi supportati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Specifica QP.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>Specifica se il codificatore usa la ricerca MV dei sottopixel basata su desktop remoto. <br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>Per la ricodifica del segmento, specifica le dimensioni del buffer.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>Per la ricodifica del segmento, specifica la durata del segmento da codificare di nuovo.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>Per la ricodifica del segmento, specifica il quantizzatore del frame prima del segmento iniziale.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>Per la ricodifica del segmento, specifica la completezza del buffer iniziale.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Specifica la velocità in bit del picco, in bit al secondo, usata per la velocità in bit (VBR) a due passaggi vincolati.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.<br/> <dl> Windows XP e versioni successive.<br />
Profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>Per la ricodifica del segmento, specifica i dati privati dei codec del file da codificare di nuovo.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
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
<td>Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola lettura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> </dl>

 

 
