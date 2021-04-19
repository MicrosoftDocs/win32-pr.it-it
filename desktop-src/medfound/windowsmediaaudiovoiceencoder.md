---
description: Il codificatore Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Si tratta del codificatore preferito per i flussi costituiti principalmente da parole vocali.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificatore Voice Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332241"
---
# <a name="windows-media-audio-voice-encoder"></a>Codificatore Voice Windows Media Audio

Il codificatore Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Si tratta del codificatore preferito per i flussi costituiti principalmente da parole vocali.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il codificatore Voice Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMSPEncMediaObject2**. È possibile creare un'istanza del codificatore vocale chiamando **CoCreateInstance**.

## <a name="output-formats"></a>Formati di output

Windows Media Audio contenuto con codifica Voice viene identificato dal tag di formato 0x00A.

## <a name="encoder-properties"></a>Proprietà del codificatore

Il codificatore Windows Media Audio Voice supporta le seguenti proprietà.



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
<td>Specifica la finestra del buffer, in millisecondi, utilizzata per il codec voce.<br/> <dl> Windows XP e versioni successive.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Specifica la latenza del codificatore in unità di pacchetti.<br/> <dl> Windows XP e versioni successive.<br />
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
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Uso del codec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




