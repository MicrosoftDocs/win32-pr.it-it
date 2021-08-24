---
description: Il Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Si tratta del codificatore preferito per i flussi costituiti principalmente da parole pronunciate.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Media Audio Voice Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c107e4e09309ff0ed56e899d3ec2cd0c9d372261b48231b4530ed3222ee3a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462428"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Media Audio Voice Encoder

Il Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Si tratta del codificatore preferito per i flussi costituiti principalmente da parole pronunciate.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il Windows Media Audio Voice è rappresentato dalla costante **CLSID \_ CWMSPEncMediaObject2.** È possibile creare un'istanza del codificatore vocale chiamando **CoCreateInstance.**

## <a name="output-formats"></a>Formati di output

Windows Il contenuto con codifica Media Audio Voice è identificato dal tag di formato 0x00A.

## <a name="encoder-properties"></a>Proprietà del codificatore

Il Windows Media Audio Voice supporta le proprietà seguenti.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Specifica la finestra del buffer, in millisecondi, usata per il codec vocale.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Specifica la latenza del codificatore in unità di pacchetto.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Specifica le parti di contenuto da codificare come musica dal codec vocale.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Specifica la modalità del codec vocale.<br/> <dl> Windows XP e versioni successive.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Uso del codec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




