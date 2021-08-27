---
description: Costanti XAudio2 che specificano parametri predefiniti, valori massimi e flag.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Valori limite e flag XAudio2 (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11293b55a44b0aefdeacf95b9e36e90a626de2c1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470707"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Valori limite e flag XAudio2

Costanti XAudio2 che specificano parametri predefiniti, valori massimi e flag.

**Valori limite XAudio2**



| Costante                                                                                                                                                                                                     | Descrizione                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ MAX \_ BUFFER \_ BYTES**</dt> </dl>             | Valore massimo consentito per [**XAUDIO2 \_ BUFFER.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**NUMERO MASSIMO BUFFER IN CODA XAUDIO2 \_ \_ \_**</dt> </dl>       | Numero massimo di buffer consentiti in una coda vocale.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**SISTEMA BUFFER MAX XAUDIO2 \_ \_ \_**</dt> </dl>       | Numero massimo di buffer consentiti per i thread di sistema (Xbox 360 consentiti).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ MAX \_ AUDIO \_ CHANNELS**</dt> </dl>       | Valore massimo consentito per **WAVEFORMATEX.nChannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**FREQUENZA DI \_ CAMPIONAMENTO MINIMA XAUDIO2 \_ \_**</dt> </dl>                | Frequenza di campionamento audio minima supportata.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**FREQUENZA DI \_ CAMPIONAMENTO MASSIMA XAUDIO2 \_ \_**</dt> </dl>                | Frequenza di campionamento audio massima supportata.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**XAUDIO2 \_ MAX \_ VOLUME \_ LEVEL**</dt> </dl>             | Livello massimo di volume consentito.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ MIN \_ FREQ \_ RATIO**</dt> </dl>                   | Rapporto di frequenza minimo consentito in una voce di origine.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FREQ \_ RATIO**</dt> </dl>                   | Rapporto di frequenza massimo consentito in una voce di origine.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ DEFAULT \_ FREQ \_ RATIO**</dt> </dl>       | Valore predefinito per **l'argomento MaxFrequencyRatio** di [**IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FILTER \_ ONEOVERQ**</dt> </dl>    | Valore massimo per [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**FREQUENZA FILTRO MAX XAUDIO2 \_ \_ \_**</dt> </dl> | Valore massimo per [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frequenza**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**XAUDIO2 \_ MAX \_ LOOP \_ COUNT**</dt> </dl>                   | Valore massimo che non verrà considerato come ciclo infinito per [**BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**ISTANZE MAX \_ XAUDIO2 \_**</dt> </dl>                       | Numero massimo di istanze simultanee di XAudio2 consentite Xbox 360.<br/>                                                                       |



**Valori XAudio2 con significato speciale**



| Costante                                                                                                                                                                                              | Descrizione                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ NOW**</dt> </dl>                         | Usato come parametro per i metodi con un argomento OperationSet. Per altre informazioni, vedere Set di [operazioni XAudio2.](xaudio2-operation-sets.md)<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ ALL**</dt> </dl>                         | Usato come parametro in [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**OPSET XAUDIO2 \_ \_ NON VALIDO**</dt> </dl>                | Specifica un valore non valido per gli argomenti operationSet. Per altre informazioni, vedere Set di [operazioni XAudio2.](xaudio2-operation-sets.md)<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ NO \_ LOOP \_ REGION**</dt> </dl>            | Non specifica alcuna area del ciclo, usata in [**XAUDIO2 \_ BUFFER.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**CICLO INFINITO \_ XAUDIO2 \_**</dt> </dl>                | Specifica il ciclo infinito, usato in [**BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**CANALI PREDEFINITI \_ XAUDIO2 \_**</dt> </dl>       | Specifica il numero predefinito di canali per la piattaforma corrente, usato in [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**CAMPIONAMENTO PREDEFINITO XAUDIO2 \_ \_**</dt> </dl> | Specifica la frequenza di campionamento predefinita per la piattaforma corrente, usata in [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/>        |



**Flag XAudio2**




| Costante | Descrizione | 
|----------|-------------|
| <span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt></dl> | Specifica che deve essere usata la versione di debug/verifica del motore audio anziché la versione di rilascio. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create.</strong></a><br /><blockquote>[!Note]<br />Questo flag non è supportato in Windows 8 o Windows 10.</blockquote><br /> | 
| <span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt></dl> | Specifica che una voce di origine non userà lo spostamento del passo. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice.</strong></a><br /> | 
| <span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt></dl> | Specifica che non è disponibile alcuna conversione della frequenza di campionamento in una voce di origine. Gli output della voce devono avere la stessa frequenza di campionamento. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice.</strong></a><br /> | 
| <span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt></dl> | Specifica che l'effetto filtro deve essere disponibile in una voce. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a> e <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2::CreateSubmixVoice.</strong></a><br /> | 
| <span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt></dl> | Specifica che una voce deve continuare a emettere l'output dell'effetto dopo l'arresto. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice::Stop.</strong></a><br /> | 
| <span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt></dl> | Indica l'ultimo buffer in un flusso. Vedere <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Flag</strong>.<br /> | 
| <span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt></dl> | Specifica che il motore audio deve arrestarsi quando non vengono avviate voci di origine e avviarsi all'avvio di una voce. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create.</strong></a><br /> | 
| <span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt></dl> | Indica che è necessario usare un filtro in un invio vocale. Vedere <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Flag</strong>.<br /> | 
| <span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt></dl> | Specifica un quantum di elaborazione non predefinito di 21,33 ms (1024 campioni a 48 KHz). Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create.</strong></a><br /> | 
| <span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt></dl> | Specifica che un client audio virtuale non deve essere utilizzato. Vedere <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2::CreateMasteringVoice.</strong></a><br /><blockquote>[!Note]<br />Nei dispositivi della famiglia di dispositivi mobili viene sempre usato un client audio virtuale, indipendentemente dall'uso di questo flag.</blockquote><br /> | 




**Parametri predefiniti XAudio2 per il filtro vocale predefinito**



| Costante                                                                                                                                                                                                                 | Descrizione                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**TIPO DI FILTRO PREDEFINITO XAUDIO2 \_ \_ \_**</dt> </dl>                | Specifica il tipo di filtro predefinito da usare con voci e invii vocali.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**FREQUENZA FILTRO PREDEFINITA XAUDIO2 \_ \_ \_**</dt> </dl> | Specifica la frequenza di filtro predefinita da usare con voci e invii vocali.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ DEFAULT \_ FILTER \_ ONEOVERQ**</dt> </dl>    | Specifica la frequenza di decadimento del filtro predefinita da usare con voci e invii vocali.<br/> |



## <a name="remarks"></a>Commenti

### <a name="platform-requirements"></a>Requisiti della piattaforma

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 
