---
description: Il codificatore Windows Media Video 7/8 implementa le versioni precedenti del codificatore Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificatore Windows Media Video 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332806"
---
# <a name="windows-media-video-78-encoder"></a>Codificatore Windows Media Video 7/8

Il codificatore Windows Media Video 7/8 implementa le versioni precedenti del codificatore Windows Media Video.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore Windows Media Video 7/8 è **CLSID \_ CWMVXEncMediaObject**. È possibile creare un'istanza del codificatore chiamando **CoCreateInstance**.

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

La tabella seguente illustra i codici a quattro caratteri (fourcc) per i tipi di output supportati dal codificatore Windows Media Video 7/8.



| Category              | FOURCC |
|-----------------------|--------|
| Windows Media Video 7 | WMV1 |
| Windows Media Video 8 | WMV2 |



 

## <a name="properties"></a>Proprietà

Il codificatore Windows Media Video 7/8 supporta le seguenti proprietà.



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
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>Specifica la frequenza media dei fotogrammi del contenuto video, in frame al secondo.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.<br/> <dl> Windows XP e versioni successive.<br />
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
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Specifica il modello di conformità del dispositivo in cui è conforme il contenuto codificato.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video eliminati durante la codifica.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Specifica la fine di un passaggio di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>Specifica se l'output del codec sarà interlacciato.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Specifica il numero massimo di passaggi supportati dal codec.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>Specifica QP.<br/> <dl> Windows Vista e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Specifica la velocità in bit del picco, in bit al secondo, usata per la velocità in bit (VBR) a due passaggi vincolati.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.<br/> <dl> Windows XP e versioni successive.<br />
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
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> <dt>

[GUID del sottotipo video](video-subtype-guids.md)
</dt> </dl>

 

 
