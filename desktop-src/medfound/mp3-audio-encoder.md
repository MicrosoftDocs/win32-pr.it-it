---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificatore audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049663"
---
# <a name="mp3-audio-encoder"></a>Codificatore audio MP3

Il codificatore audio Microsoft Media Foundation MP3 è una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT) che codifica audio MPEG-1 Layer 3 (MP3).

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore MP3 è **CLSID \_ MP3ACMCodecWrapper**, definito nel file di intestazione wmcodecdsp. h.

## <a name="media-types"></a>Tipi di supporto

Il codificatore MP3 supporta i tipi di supporto seguenti. Il tipo di output deve essere impostato prima del tipo di input.

### <a name="output-types"></a>Tipi di output

Impostare gli attributi seguenti sul tipo di supporto di output.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
<th>Osservazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principale.</td>
<td>Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Sottotipo audio.</td>
<td>Deve essere <strong>MFAudioFormat_MP3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Velocità in bit del flusso MP3 codificato, in byte al secondo.</td>
<td>Il codificatore supporta tutte le velocità in bit definite dallo standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 o 320 Kbps).<br/> Le velocità in bit predefinite sono di 128 kbps per mono e 320 kbps per lo stereo.<br/> Utilizzare questo attributo per specificare la velocità in bit codificata.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Numero di canali.</td>
<td>Sono supportati i valori seguenti:
<ul>
<li>1 (mono)</li>
<li>2 (stereo)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Campioni al secondo.</td>
<td>Sono supportati i valori seguenti:
<ul>
<li>48000 (48 KHz)</li>
<li>44100 (44,1 KHz)</li>
<li>32000 (32 KHz)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>Dati codec aggiuntivi.</td>
<td>Questo attributo contiene i 12 byte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> che seguono il membro <strong>wfx</strong> di tale struttura.</td>
</tr>
</tbody>
</table>



 

In alternativa, è possibile compilare una struttura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) e chiamare [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) per convertire la struttura in un tipo di supporto Media Foundation.

### <a name="input-types"></a>Tipi di input

Impostare gli attributi seguenti sul tipo di supporto di input.



| Attributo                                                                               | Descrizione         | Osservazioni                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                               | Tipo principale.         | Deve essere **MFMediaType \_ audio**. |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                      | Sottotipo.            | Deve essere **MFAudioFormat \_ PCM**. |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)       | BITS per campione.    | Deve essere 16.                     |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md) | Campioni al secondo. | Deve corrispondere al tipo di output.     |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)              | Numero di canali. | Deve corrispondere al tipo di output.     |



 

Il codificatore supporta solo input PCM a 16 bit di tipo Integer. Non supporta l'input a virgola mobile a 32 bit.

### <a name="media-formats"></a>Formati multimediali

Lo standard MPEG-1 e MPEG-2 definisce i formati audio 252 di livello 3. Il codificatore MP3 supporta lo standard con alcune eccezioni, oltre ad alcuni formati aggiuntivi, come descritto di seguito. Il livello 3 è definito come segue:



| Requisito | Valore |
|----------------------------------|---------------------------------------------------------------|
| Canali                         | mono o stereo                                                |
| Velocità di campionamento MPEG-1 in kHz       | 44,1, 48, 32                                                  |
| Velocità in bit codificate MPEG-1 in kbps | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| Velocità di campionamento MPEG-2 in kHz       | 8, 11,025, 12, 16, 22,05, 24                                  |
| Velocità in bit codificate MPEG-2 in kbps | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

Il codificatore MP3 supporta inoltre i formati seguenti.



| Frequenza di campionamento | Velocità in bit     | Numero canale |
|-------------|--------------|----------------|
| 8000        | 18000, 20000 | 2              |
| 11025       | 18000, 20000 | 1 o 2         |
| 12000       | 18000, 20000 | 1 o 2         |
| 16000       | 18000, 20000 | 1              |
| 32000       | 144000       | 1 o 2         |
| 44100       | 144000       | 1 o 2         |
| 48000       | 144000       | 1 o 2         |



 

Il codificatore MP3 non supporta i formati seguenti definiti dallo standard.



| Frequenza di campionamento | Velocità in bit                                    | Numero canale |
|-------------|----------------------------------------------|----------------|
| 12000       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 11025       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 8000        | 80000, 96000, 112000, 128000, 144000, 160000 | 1 o 2         |
| 8000        | 8000, 11025, 12000, 16000, 22050, 24000      | 2              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
