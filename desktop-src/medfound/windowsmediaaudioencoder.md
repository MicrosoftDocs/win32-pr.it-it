---
description: 'Il codificatore Windows Media Audio codifica i flussi audio. Il codificatore supporta tre categorie di output codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificatore Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331689"
---
# <a name="windows-media-audio-encoder"></a>Codificatore Windows Media Audio

Il codificatore Windows Media Audio codifica i flussi audio. Il codificatore supporta tre categorie di output codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMAEncMediaObject**. È possibile creare un'istanza del codificatore audio chiamando **CoCreateInstance**.

## <a name="input-formats"></a>Formati di input

La tabella seguente illustra i tag di formato audio che rappresentano le categorie di input supportate dal codificatore Windows Media Audio. Per informazioni su come impostare i tipi di input e output per il codificatore, vedere [Configuring audio encoding](configuringaudioencoding.md).



| Costante tag di formato       | Valore del tag di formato | Formato audio                                          |
|---------------------------|------------------|-------------------------------------------------------|
| \_PCM in formato Wave \_         | 0x0001           | Formato PCM                                            |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Virgola mobile IEEE                                   |
| \_formato Wave \_ estendibile  | 0xFFFE           | Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE** |



 

## <a name="output-formats"></a>Formati di output

La tabella seguente illustra i tag di formato audio che rappresentano le categorie di output supportate dal codificatore Windows Media Audio.



| Costante tag di formato             | Valore del tag di formato | Formato audio                     |
|---------------------------------|------------------|----------------------------------|
| \_Formato Wave \_ WMAUDIO2          | 0x0161           | Windows Media Audio standard     |
| \_Formato Wave \_ WMAUDIO3          | 0x0162           | Windows Media Audio Professional |
| \_formato Wave \_ WMAUDIO \_ Lossless | 0x0163           | Windows Media Audio senza perdita di perdite     |



 

## <a name="interfaces"></a>Interfacce

Un oggetto di utilizzo del contenuto audio espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un codificatore Windows Media Audio si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore audio si comporta come DMO o MFT.



| Sistema operativo | Comportamento del codificatore                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un codificatore Windows Media Audio si comporta sempre come DMO.                                                                                                                                |
| Windows Vista    | Per impostazione predefinita, un codificatore Windows Media Audio si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un codificatore audio, si comporta come un MFT. |
| Windows 7        | Per impostazione predefinita, un codificatore Windows Media Audio si comporta come DMO. Se si ottiene un'interfaccia **IMFTransform** su un codificatore audio, si comporta come un MFT.                                    |



 

## <a name="encoder-properties"></a>Proprietà del codificatore

Il codificatore Windows Media Audio supporta le seguenti proprietà.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></td>
<td>Specifica se il codificatore usa la codifica VBR media controllabile.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit limitata (VBR) a livello di picco.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></td>
<td>Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi. <br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></td>
<td>Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></td>
<td>Specifica se la complessità dell'algoritmo di codifica è vincolata.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></td>
<td>Specifica se il codificatore è vincolato da un requisito di latenza massima.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Specifica se le modalità enumerate dal codificatore sono limitate a quelle che soddisfano un requisito di qualità.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>Specifica il profilo di complessità del contenuto codificato.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità desiderato per la codifica VBR.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></td>
<td>Specifica se il codificatore utilizza la sostituzione del rumore.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></td>
<td>Specifica se il codificatore usa la limitazione dell'intervallo PCM.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></td>
<td>Specifica la larghezza di banda massima codificata consentita dal troncamento della banda nel codificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></td>
<td>Specifica la larghezza di banda minima codificata consentita dal troncamento della banda nel codificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></td>
<td>Specifica la qualità a cui è consentita una larghezza di banda minima codificata. <br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></td>
<td>Specifica la qualità di massima consentita per la larghezza di banda codificata.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></td>
<td>Specifica se il codificatore esegue il troncamento della banda.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></td>
<td>Specifica se il codificatore usa lo stile di calcolo della maschera eseguito dalla versione 7 del codificatore Windows Media Audio.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></td>
<td>Specifica se il codificatore esegue l'elaborazione di immagini stereo. <br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></td>
<td>Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></td>
<td>Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></td>
<td>Specifica la complessità dell'algoritmo di codifica.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>Specifica la fine di un passaggio di codifica.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></td>
<td>Specifica se il codificatore principale utilizza &quot; la &quot; funzionalità più.<br/> <dl> Windows Vista e versioni successive.<br />
Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></td>
<td>Specifica la latenza massima per il decodificatore, in millisecondi.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></td>
<td>Specifica la latenza massima per il codificatore, in millisecondi.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></td>
<td>Specifica il livello di qualità VBR del tipo di output enumerato più di recente.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>Specifica il numero massimo di passaggi supportati dal codificatore.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>Specifica il numero di passaggi che il codificatore utilizzerà per codificare il contenuto.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></td>
<td>Specifica se il codificatore è vincolato da una velocità in bit di picco.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></td>
<td>Specifica il numero preferito di campioni per fotogramma.<br/> <dl> Windows Vista e versioni successive.<br />
Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></td>
<td>Specifica se il codificatore deve utilizzare una dimensione del frame preferita.<br/> <dl> Windows Vista e versioni successive.<br />
Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>Specifica la velocità in bit del picco, in bit al secondo, usata per la codifica con velocità in bit (VBR) a 2 passaggi vincolata. <br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></td>
<td>Specifica la finestra media del buffer, in millisecondi, di un flusso codificato.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></td>
<td>Specifica la finestra massima del buffer, in millisecondi, di un flusso codificato.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></td>
<td>Specifica la velocità in bit media, in bit al secondo, di un flusso codificato.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></td>
<td>Specifica la velocità in bit massima, in bit al secondo, di un flusso codificato.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>Specifica se il codificatore usa la codifica VBR.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></td>
<td>Questa proprietà non è attualmente utilizzata dal codec Windows Media Audio.<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></td>
<td>Specifica il livello di volume medio del contenuto audio.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></td>
<td>Specifica il livello di volume massimo che si verifica nel contenuto audio.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></td>
<td>Specifica il numero medio di byte al secondo per l'audio con codifica VBR.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional, lossless.<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></td>
<td>Specifica se il codificatore deve produrre 1 pacchetto WMA per fotogramma.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></td>
<td>Specifica se il codificatore deve generare parametri dinamici per il controllo degli intervalli.<br/> <dl> Windows Vista e versioni successive.<br />
Standard, Professional, lossless.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></td>
<td>Specifica la struttura <strong>WAVEFORMATEX</strong> che descrive il contenuto audio di input.<br/> <dl> Windows XP e versioni successive.<br />
Standard, Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></td>
<td>Specifica se il codificatore deve abilitare la codifica S/PDIF in tempo reale.<br/> <dl> Windows Vista e versioni successive.<br />
Professional.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmadmoe.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> </dl>

 

 




