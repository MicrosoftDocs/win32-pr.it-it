---
description: Costanti XAudio2 che specificano i parametri predefiniti, i valori massimi e i flag.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Flag e valori limite XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332104"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Flag e valori limite XAudio2

Costanti XAudio2 che specificano i parametri predefiniti, i valori massimi e i flag.

**Valori limite XAudio2**



| Costante                                                                                                                                                                                                     | Descrizione                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**\_ \_ Byte buffer massimo \_ XAUDIO2**</dt> </dl>             | Valore massimo consentito per [**il \_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**XAUDIO2 \_ \_ buffer in coda \_ Max**</dt> </dl>       | Numero massimo di buffer consentiti in una coda voce.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**\_ \_ Sistema buffer XAUDIO2 Max \_**</dt> </dl>       | Numero massimo di buffer consentiti per i thread di sistema (solo Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ Max \_ \_ canali audio**</dt> </dl>       | Valore massimo consentito per **WAVEFORMATEX. nChannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**\_Frequenza di \_ campionamento minima XAUDIO2 \_**</dt> </dl>                | Frequenza di campionamento audio minima supportata.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**\_Frequenza di \_ campionamento max XAUDIO2 \_**</dt> </dl>                | Frequenza di campionamento audio massima supportata.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**\_Livello massimo di \_ volume \_ XAUDIO2**</dt> </dl>             | Livello massimo consentito per il volume.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**\_ \_ Rapporto frequenza minima \_ XAUDIO2**</dt> </dl>                   | Rapporto frequenza minima consentito in una voce di origine.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**\_ \_ Rapporto frequenza massima \_ XAUDIO2**</dt> </dl>                   | Rapporto di frequenza massima consentito in una voce di origine.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**\_Percentuale di \_ frequenza XAUDIO2 predefinita \_**</dt> </dl>       | Valore predefinito per l'argomento **MaxFrequencyRatio** di [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**\_ \_ ONEOVERQ filtro XAUDIO2 \_ Max**</dt> </dl>    | Valore massimo per [**i \_ \_ parametri del filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**\_Frequenza di \_ filtro \_ massima XAUDIO2**</dt> </dl> | Valore massimo per [**i \_ \_ parametri del filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frequenza**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**\_Numero massimo di \_ cicli \_ XAUDIO2**</dt> </dl>                   | Valore massimo che non verrà considerato come ciclo infinito per il [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**XAUDIO2 \_ numero massimo di \_ istanze**</dt> </dl>                       | Numero massimo di istanze simultanee di XAudio2 consentite in Xbox 360.<br/>                                                                       |



**XAudio2 valori con un significato speciale**



| Costante                                                                                                                                                                                              | Descrizione                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ commit \_ ora**</dt> </dl>                         | Usato come parametro per i metodi con un argomento di Operational. Per ulteriori informazioni, vedere [set di operazioni XAudio2](xaudio2-operation-sets.md) .<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ commit \_ tutto**</dt> </dl>                         | Usato come parametro in [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**\_OPSET XAUDIO2 non valido \_**</dt> </dl>                | Specifica un valore non valido per gli argomenti del funzionamento. Per ulteriori informazioni, vedere [set di operazioni XAudio2](xaudio2-operation-sets.md) .<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ Nessuna \_ area del ciclo \_**</dt> </dl>            | Specifica nessuna area del ciclo, utilizzata [**nel \_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**\_Ciclo XAUDIO2 \_ infinito**</dt> </dl>                | Specifica un ciclo infinito, usato nel [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**XAUDIO2 \_ i \_ canali predefiniti**</dt> </dl>       | Specifica il numero predefinito di canali per la piattaforma corrente, usati in [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**\_ \_ Campionamento predefinito XAUDIO2**</dt> </dl> | Specifica la frequenza di campionamento predefinita per la piattaforma corrente, usata in [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Flag XAudio2**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che deve essere utilizzata la versione di debug/controllata del motore audio al posto della versione di rilascio. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Questo flag non è supportato in Windows 8 o Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che una voce di origine non userà il cambio di passo, vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che in una voce di origine non è disponibile alcuna conversione della frequenza di campionamento. gli output della voce devono avere la stessa frequenza di campionamento. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che l'effetto del filtro deve essere disponibile in una voce. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a> e <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2:: CreateSubmixVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che una voce deve continuare a emettere l'output dell'effetto dopo che è stata arrestata. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice:: Stop</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Indica l'ultimo buffer in un flusso. Vedere <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Flag</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che il motore audio deve essere interrotto quando nessuna voce di origine viene avviata e avviata quando viene avviata una voce. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Indica che è necessario utilizzare un filtro su un'invio vocale. Vedere <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Flag</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Specifica un quantum di elaborazione non predefinito di 21,33 ms (1024 campioni a 48 kHz). Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Specifica che un client audio virtuale non deve essere utilizzato. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2:: CreateMasteringVoice</strong></a>.<br/>
<blockquote>
[!Note]<br />
Nei dispositivi della famiglia di dispositivi mobili, viene sempre usato un client audio virtuale, indipendentemente dal fatto che questo flag venga usato.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**XAudio2 parametri predefiniti per il filtro vocale incorporato**



| Costante                                                                                                                                                                                                                 | Descrizione                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_Tipo di \_ filtro \_ predefinito XAUDIO2**</dt> </dl>                | Specifica il tipo di filtro predefinito da usare con voci e invii vocali.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**\_Frequenza di \_ filtro \_ predefinita XAUDIO2**</dt> </dl> | Specifica la frequenza di filtro predefinita da usare con voci e invii vocali.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**\_ \_ ONEOVERQ filtro predefinito \_ XAUDIO2**</dt> </dl>    | Specifica la frequenza di filtro predefinita del decadimento da utilizzare con le voci e le invii vocali.<br/> |



## <a name="remarks"></a>Commenti

### <a name="platform-requirements"></a>Requisiti della piattaforma

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); DirectX SDK (XAudio 2,7)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XAudio2:: Constants](constants.md)
</dt> </dl>

 

 
