---
description: Il codificatore di schermo Windows Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificatore della schermata Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331568"
---
# <a name="windows-media-video-9-screen-encoder"></a>Codificatore dello schermo Windows Media Video 9

Il codificatore di schermo Windows Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore di schermo Windows Media Video 9 è rappresentato dalla costante **CLSID \_ CMSSCEncMediaObject2**. È possibile creare un'istanza del codificatore chiamando **CoCreateInstance**.

## <a name="input-types"></a>Tipi di input

I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come DMO (DirectX Media Object).

-   \_RGB24 MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_ARGB32 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE

I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come trasformazione Media Foundation (MFT).

-   \_RGB24 MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_ARGB32 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB555 MFVideoFormat
-   \_RGB8 MFVideoFormat

## <a name="output-types"></a>Tipi di output

Il codice di quattro caratteri (FOURCC) per il contenuto codificato Windows Media Video schermata versione 9 è "MSS2".

I tipi di output seguenti sono supportati dal codificatore dello schermo versione 9.

-   \_Mss2 MEDIASUBTYPE

## <a name="encoder-properties"></a>Proprietà del codificatore

Il codificatore Windows Media Video 9 dello schermo supporta le seguenti proprietà.



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
<td>Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Windows XP e versioni successive. Proprietà di lettura/scrittura.<br/> Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>Specifica QP. I valori possibili sono compresi tra 1,0 e 31,0.<br/> <dl> Windows Vista e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>Specifica la velocità in bit del picco, in bit al secondo, usata per la codifica con velocità in bit (VBR) a 2 passaggi vincolata.<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).<br/> <dl> Windows XP e versioni successive.<br />
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
<td>Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Un oggetto del codificatore di schermata espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un codificatore dello schermo si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore dello schermo si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del codificatore                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un codificatore Windows Media Screen si comporta sempre come DMO.                                                                                             |
| Windows Vista e Windows 7 | Per impostazione predefinita, un codificatore Windows Media Screen si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** su un codificatore di schermo, si comporta come un MFT. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> <dt>

[Uso del codec della schermata Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Decodificatore dello schermo Windows Media Video 9](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




