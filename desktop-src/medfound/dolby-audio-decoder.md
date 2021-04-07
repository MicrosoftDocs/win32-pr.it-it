---
description: Il decoder audio Dolby è un MFT che decodifica Dolby Digital (AC-3) e Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Decoder audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749263"
---
# <a name="dolby-audio-decoder"></a>Decoder audio Dolby

Il decoder audio Dolby è una [trasformazione Media Foundation](media-foundation-transforms.md) (MFT) che decodifica i tipi di flusso seguenti:

-   Dolby Digital, chiamato anche Dolby AC-3
-   Dolby Digital Plus, detto anche Enhanced AC-3 (E-AC-3)

> [!IMPORTANT]
> Per le versioni di Windows precedenti a Windows 8, l'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.

 

Per ulteriori informazioni su questi formati, vedere la sezione relativa alla revisione B del documento ATSC (Advanced Television Systems Committee) per il documento ATSC ( *Digital Audio Compression standard)*.

Il decodificatore può anche convertire un flusso Dolby Digital Plus in formato Dolby Digital per l'output AC-3 S/PIDF o formattare un flusso Dolby Digital Plus per l'output digitale HDMI.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del decodificatore Dolby audio è **CLSID \_ CMSDDPlusDecMFT**, definito nel file di intestazione wmcodecdsp. h.

## <a name="input-types"></a>Tipi di input

Il decodificatore Dolby audio supporta i sottotipi di input seguenti.



| Subtype                                 | Descrizione                                                                                                                                                 | Intestazione       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ Dolby \_ AC3**            | Audio Dolby Digital.                                                                                                                                        | mfapi. h      |
| **\_DVM MEDIASUBTYPE**                   | Audio Dolby Digital; vedere [**sottotipi audio**](../directshow/audio-subtypes.md). Questo sottotipo può essere usato in modo interscambiabile con **MEDIASUBTYPE \_ Dolby \_ AC3**.<br/> | wmcodecdsp. h |
| **MFAudioFormat \_ Dolby \_ Digital \_ Plus** | Audio Dolby Digital Plus.                                                                                                                                   | mfapi. h      |



 

Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Per informazioni dettagliate, vedere la tabella precedente.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Frequenza di campionamento, in campioni al secondo.</td>
<td>facoltativo. I valori validi sono: 48000, 44100, 32000, 24000, 22050 e 16000. Se questo attributo non è impostato, il valore predefinito è 48000. <br/>
<blockquote>
[!Note]<br />
I flussi Dolby AC-3 sono limitati alle tre tariffe più elevate in questo elenco.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali, incluso il canale LFE (Low Frequency), se presente.</td>
<td>facoltativo. I valori validi sono compresi tra 1 (mono) e 8 (configurazione del canale 7,1). Se questo attributo non è impostato, il valore predefinito è 2 (stereo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se specificato, il valore deve essere coerente con il numero di canali audio. Se l'attributo non è impostato, il decodificatore utilizza una maschera di canale predefinita, in base al numero di canali.</td>
</tr>
</tbody>
</table>



 

La tabella seguente elenca le configurazioni del canale Dolby supportate.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Configurazione del canale</th>
<th>Numero di canali</th>
<th>Maschere del canale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1/0 (mono)</td>
<td>1</td>
<td>0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/0 (stereo) o 1 + 1 (doppio mono)</td>
<td>2</td>
<td>0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</td>
</tr>
<tr class="odd">
<td>3/0</td>
<td>3</td>
<td>0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</td>
</tr>
<tr class="even">
<td>2/1</td>
<td>3</td>
<td>0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="odd">
<td>3/1</td>
<td>4</td>
<td>0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/2</td>
<td>4</td>
<td>0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oppure<br/> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="odd">
<td>3/2</td>
<td>5</td>
<td>0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oppure<br/> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="even">
<td>3/2 + LFE</td>
<td>6</td>
<td>0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> oppure<br/> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)<br/></td>
</tr>
<tr class="odd">
<td>3/2/2 + LFE
<blockquote>
[!Note]<br />
Solo Dolby Digital Plus.
</blockquote>
<br/> <br/></td>
<td>8</td>
<td>0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</td>
</tr>
</tbody>
</table>



 

Inoltre, le configurazioni di canale 1/0, 2/0, 3/0, 2/1, 3/1 e 2/2 possono essere visualizzate anche con un canale LFE.

## <a name="output-types"></a>Tipi di output

Il decodificatore Dolby audio supporta i sottotipi di output seguenti.



| Subtype                                                   | Descrizione                                                                                                                               | Intestazione    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**                      | Audio Dolby AC-3 formattato per l'output digitale S/PDIF.                                                                                     | mfapi. h   |
| **\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus** | Dolby Digital Plus audio formattato per l'output digitale HDMI.                                                                               | ksmedia. h |
| **\_Float MFAudioFormat**                                  | Audio PCM a virgola mobile IEEE a 32 bit<br/> **Windows 10**: stereo, 5,1, 7,1<br/> **Versioni precedenti**: stereo, 5,1<br/> | mfapi. h   |
| **\_PCM MFAudioFormat**                                    | audio PCM a 16 bit<br/> **Windows 10**: stereo, 5,1, 7,1<br/> **Versioni precedenti**: stereo, 5,1<br/>                     | mfapi. h   |



 

Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Per informazioni dettagliate, vedere la tabella precedente.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Frequenza di campionamento, in campioni al secondo.</td>
<td>Obbligatorio. I valori validi sono: 48000, 44100, 32000, 24000, 22050 e 16000. La frequenza di campionamento dell'output deve essere identica alla frequenza di campionamento di input. Il decodificatore non può modificare la frequenza di campionamento del flusso.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali, incluso il canale LFE (Low Frequency), se presente.</td>
<td>Obbligatorio per l'output del PCM. <br/> Non necessario per l'output digitale. <br/> Se il tipo di input è mono, stereo o dual-mono (tutti senza canale LFE), l'unico valore valido è 2, per l'output stereo. In caso contrario, il valore può essere: <br/>
<ul>
<li>2 per downmix stereo</li>
<li>6 per le configurazioni di canale 5,1</li>
<li>8 per le configurazioni di canale 7,1</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>Obbligatorio per l'output PCM se il numero di canali è maggiore di 2. Il valore deve essere:<br/>
<ul>
<li>0x3 per output stereo</li>
<li>0x3F per l'output del canale 5,1</li>
<li>0x63F per l'output del canale 7,1</li>
</ul>
Non necessario per l'output digitale. <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Numero di bit per esempio audio.</td>
<td>Obbligatorio per l'output del PCM. Il valore deve essere 32 per <strong>MFAudioFormat_Float</strong>e 16 per <strong>MFAudioFormat_PCM</strong>.<br/> Non necessario per l'output digitale.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Numero di bit validi di dati audio in ogni esempio audio.</td>
<td>Facoltativo per l'output del PCM. Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.<br/> Non necessario per i sottotipi di output digitali.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Allineamento del blocco in byte.</td>
<td>Facoltativo per l'output del PCM. Non necessario per l'output digitale.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Numero medio di byte al secondo.</td>
<td>Facoltativo per l'output del PCM. Non necessario per l'output digitale.</td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decoder audio Dolby implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . L'applicazione può utilizzare questo metodo per ottenere o impostare gli attributi seguenti.



| Attributo                                                                                | Descrizione                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codecapis \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | Specifica se un flusso audio Dolby a 2 canali è codificato come stereo o dual-mono. Prima che il primo frame Dolby venga decodificato, il valore è **eAVDecAudioDualMono non \_ specificato**. Dopo l'inizio della decodifica, il valore riflette il frame Dolby più recente.<br/> Di sola lettura. <br/> |
| [Codecapis \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | Specifica la modalità di riproduzione audio dual-mono da parte del decodificatore. Il valore predefinito è **eAVDecAudioDualMonoReproMode \_ Left \_ mono**. L'applicazione può impostare questa proprietà in qualsiasi momento.<br/> Proprietà di lettura/scrittura.<br/>                                                                            |
| [Codecapis \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | Per i flussi Dolby Digital (AC-3), specifica la velocità in bit del flusso di input in bit al secondo. Per Dolby Digital Plus (E-AC3), il valore è sempre zero.<br/> Sola lettura.<br/>                                                                                              |
| [Codecapis \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | Il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli.<br/> Proprietà di lettura/scrittura.<br/>                                                                                                                                                                                    |
| [Codecapis \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | Boost di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli.<br/> Proprietà di lettura/scrittura.<br/>                                                                                                                                                                                   |
| [Codecapis \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | Modalità di controllo della compressione.<br/> Proprietà di lettura/scrittura.<br/>                                                                                                                                                                                                                          |
| [Codecapis \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | Tipo di downmix stereo. Questa proprietà si applica quando l'input è un flusso multicanale e l'output è un flusso stereo.<br/> Proprietà di lettura/scrittura.<br/>                                                                                                                           |
| [la \_ \_ modifica del \_ formato \_ dinamico del supporto MFT](mft-support-dynamic-format-change-attribute.md) | Questo attributo restituisce **false**, che indica che il decodificatore deve essere svuotato prima che venga impostato un nuovo tipo di input.<br/> Proprietà di lettura/scrittura.<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il decodificatore accetta solo flussi Dolby RAW, come definito da A/52B. I payload, ad esempio i flussi elementari in pacchetto (PES) non sono supportati. Per Dolby Digital Plus, il decodificatore decodifica fino a 5,1 canali. In Windows 10, i flussi di canale 7,1 vengono decodificati senza downmix. Nelle versioni precedenti del sistema operativo, se il flusso è di 7,1 canali, solo il canale 5,1 downmix verrà decodificato. Se il flusso è Dolby Digital Plus con più di un sottoflusso indipendente, viene decodificato solo il sottoflusso indipendente 0. Il decodificatore ignora gli altri sottoflussi indipendenti. Il decodificatore ignora inoltre tutti i sottoflussi dipendenti. Il decodificatore supporta la decrittografia e la decodifica dei flussi protetti dalla tecnologia di Rights Management digitale (DRM).

Se il tipo di supporto di input ha una configurazione del canale diversa da mono, stereo o dual-mono (tutti senza canale LFE), il decodificatore fornisce due opzioni per le configurazioni del canale di output:

-   output a 8 canali (configurazione del canale 7,1)
-   output a 6 canali (configurazione del canale 5,1)
-   Downmix stereo

Se è selezionata l'opzione downmix stereo, il tipo di downmix può essere impostato su MFT usando la proprietà [CODEcapis \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .

Se il tipo di output è **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, ogni buffer di output contiene 6.144 byte. Il buffer inizia con un'intestazione S/PDIF a 8 byte, seguita da un frame AC-3 compresso, seguito da un riempimento pari a zero a 6.144 byte.

Se il tipo di output è **KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ Dolby \_ Digital \_ Plus**, ogni buffer di output contiene 24.576 byte. Il buffer inizia con un'intestazione S/PDIF a 8 byte, seguita da un frame Dolby Digital Plus compresso da 1 a 6, che corrisponde a campioni PCM 1.536, seguiti da zero padding a 24.576 byte. Per l'output HDMI, viene compresso solo il substream 0 indipendente.

Il decodificatore MFT viene registrato con il flag di **enumerazione MFT flag \_ \_ \_ FIELDOFUSE**, che indica che il MFT deve essere sbloccato dall'applicazione prima dell'uso. Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
