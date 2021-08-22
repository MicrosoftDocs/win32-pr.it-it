---
description: Il Windows dello schermo di Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitor del computer.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Windows Codificatore di schermo Media Video 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6d9fbe59671d978fb7374acbbc8ed1d8e9ea5afded0154242c4d1ccb4df3d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713141"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Codificatore di schermo Media Video 9

Il Windows dello schermo di Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitor del computer.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore di schermo Windows Media Video 9 è rappresentato dalla costante **CLSID \_ CMSSCEncMediaObject2**. È possibile creare un'istanza del codificatore chiamando **CoCreateInstance**.

## <a name="input-types"></a>Tipi di input

I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come oggetto multimediale DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come Media Foundation Transform (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>Tipi di output

Il codice a quattro caratteri (FOURCC) per Windows contenuto codificato di Media Video Screen versione 9 è "MSS2".

I tipi di output seguenti sono supportati dal codificatore dello schermo versione 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>Proprietà del codificatore

Il Windows dello schermo di Media Video 9 supporta le proprietà seguenti.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>Specifica il sovraccarico, in byte per pacchetto, necessario per il contenitore utilizzato per archiviare il contenuto compresso.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso a velocità in bit variabile vincolata (VBR) alla velocità in bit media (specificata <a href="mfpkey-ravgproperty.md">da MFPKEY_RAVG</a>).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso a velocità in bit variabile vincolata (VBR) alla velocità in bit massima (specificata <a href="mfpkey-rmaxproperty.md">da MFPKEY_RMAX</a>).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente dati.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>Questa proprietà viene sostituita da <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>Specifica la complessità dell'algoritmo del codificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>Specifica una rappresentazione numerica del compromesso tra l'uniformità del movimento e la qualità dell'immagine nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>Specifica il numero di fotogrammi video eliminati durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>Specifica la fine di un passaggio di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>Specifica l'elemento FOURCC che identifica il codificatore che si vuole usare.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Specifica il tempo massimo, in millisecondi, tra fotogrammi chiave nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>Obsoleta.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>Specifica il numero massimo di passaggi supportati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP e versioni successive. Proprietà di lettura/scrittura.<br/> Specifica il numero di passaggi che il codec userà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Specifica QP. I valori possibili sono da 1.0 a 31.0.<br/> <dl> Windows Vista e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Specifica la velocità in bit media, in bit al secondo, usata per la codifica VBR (Variable-Bit Rate) a 2 passi.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Specifica la velocità in bit di picco, in bit al secondo, usata per la codifica vbr (Variable-Bit Rate) a 2 passi vincolata.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>Specifica se il codec userà la codifica VBR (Variable-Bit-Rate).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Specifica il livello di qualità effettivo per la codifica a velocità variabile (VBR) basata sulla qualità (1 passaggio).<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>Quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.<br/> <dl> Windows XP e versioni successive,<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>Specifica il numero di fotogrammi video ignorati perché erano duplicati dei fotogrammi precedenti.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Un oggetto codificatore di schermo espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come directx media object (DMO) e espone **l'interfaccia IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un codificatore di schermo si comporta come DMO o MFT a seconda delle interfacce che si ottengono e della versione di Windows in esecuzione. La tabella seguente illustra le condizioni in cui un codificatore di schermo si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del codificatore                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un codificatore dello schermo di Windows Media si comporta sempre come DMO.                                                                                             |
| Windows Vista e Windows 7 | Per impostazione predefinita, un codificatore dello schermo di Windows Media si comporta come DMO. Se si ottiene **un'interfaccia IMFTransform** in un codificatore di schermo, si comporta come un MFT. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione di codec](codecimplementation.md)
</dt> <dt>

[Uso del codec Windows Media Video 9 schermo](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media Video decodificatore schermo 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




