---
title: MCI_SET comando (Mmsystem.h)
description: Il comando MCI \_ SET imposta le informazioni sul dispositivo. Questo comando viene riconosciuto da dispositivi CD audio, digital-video, MIDI Sequencer, VCR, videodisc, overlay video e audio waveform.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f5affb6ce41c5c321b24353ece8f0946dc668194ac59cee95e579178a8b03df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803387"
---
# <a name="mci_set-command"></a>Comando MCI \_ SET

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [per Bias-Free comunicazioni](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo riconosce come parola di esclusione.  Questa formulazione viene usata perché è attualmente la formulazione usata all'interno dei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo che sia allineato.

Il comando MCI \_ SET imposta le informazioni sul dispositivo. Questo comando viene riconosciuto da dispositivi CD audio, digital-video, MIDI Sequencer, VCR, videodisc, overlay video e audio waveform.

Per inviare questo comando, chiamare [**la funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT o, per i dispositivi video digitale e \_ VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Puntatore a [**una struttura MCI \_ SET \_ PARMS.**](mci-set-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ SET:

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ SET \_ AUDIO
</dt> <dd>

Un numero di canale audio è incluso nel membro dwAudio della struttura identificata da *lpSet*. Questo flag deve essere usato con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. Usare una delle costanti seguenti per indicare il numero di canale:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ SET \_ AUDIO \_ ALL
</dt> <dd>

Tutti i canali audio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ SET \_ AUDIO \_ LEFT
</dt> <dd>

Canale sinistro.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ SET \_ AUDIO \_ RIGHT
</dt> <dd>

Canale destro.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI \_ SET \_ DOOR \_ CLOSED
</dt> <dd>

Chiude la copertura multimediale (se presente).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI \_ SET \_ DOOR \_ OPEN
</dt> <dd>

Apre la copertura multimediale (se presente).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Disabilita il canale audio o video specificato.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Abilita il canale audio o video specificato.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI \_ SET \_ TIME \_ FORMAT
</dt> <dd>

Un parametro di formato dell'ora è incluso nel **membro dwTimeFormat** della struttura identificata da *lpSet*. Con questo flag vengono usati i flag seguenti:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>BYTE IN FORMATO MCI \_ \_
</dt> <dd>

All'interno di un formato di dati PCM (Pulse Code Modulation), modifica la descrizione del membro temporale in byte per l'input o l'output. Riconosciuto dal **tipo di dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>FRAME IN \_ FORMATO \_ MCI
</dt> <dd>

I comandi successivi useranno i frame. Riconosciuto dai **tipi di dispositivo digitalvideo**, **vcr** e **videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>HMS \_ IN \_ FORMATO MCI
</dt> <dd>

Modifica il formato dell'ora in ore, minuti e secondi. Riconosciuto dai tipi **di dispositivo vcr** e **videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MILLISECONDI \_ DI \_ FORMATO MCI
</dt> <dd>

Modifica il formato dell'ora in millisecondi. Riconosciuto da tutti i tipi di dispositivo.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>FORMATO MCI \_ \_ MSF
</dt> <dd>

Modifica il formato dell'ora in minuti, secondi e fotogrammi. Riconosciuto dai tipi **di dispositivo cdaudio** e **vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>ESEMPI DI FORMATO MCI \_ \_
</dt> <dd>

Modifica il formato dell'ora in esempi per l'input o l'output. Riconosciuto dal **tipo di dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ FORMAT \_ SMPTE \_ 24, MCI \_ FORMAT \_ SMPTE \_ 25 e MCI \_ FORMAT \_ SMPTE \_ 30
</dt> <dd>

Imposta il formato dell'ora rispettivamente su 24, 25 e 30 fotogrammi SMPTE (Society of Motion Picture and Engineers). Riconosciuto dai tipi **di dispositivo sequencer** **e vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI \_ FORMAT \_ SMPTE \_ 30DROP
</dt> <dd>

Imposta il formato dell'ora su 30 SMPTE con drop-frame. Riconosciuto dai tipi **di dispositivo sequencer** **e vcr.**

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>FORMATO MCI \_ \_ TMSF
</dt> <dd>

Modifica il formato dell'ora in tracce, minuti, secondi e fotogrammi. (MCI usa numeri di traccia continui).) Riconosciuto dai tipi **di dispositivo cdaudio** e **vcr.**

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI \_ SET \_ VIDEO
</dt> <dd>

Imposta o disattiva il segnale video. Questo flag deve essere usato con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. I dispositivi che non hanno video restituiscono MCIERR \_ UNSUPPORTED \_ FUNCTION.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ SET \_ FILEFORMAT
</dt> <dd>

Un parametro di formato di file è incluso nel **membro dwFileFormat** della struttura identificata da *lpSet*. Per i dispositivi video digitali, il formato di file viene usato per i comandi di salvataggio o acquisizione. Se omesso, il valore predefinito potrebbe essere un formato definito dal driver di dispositivo. Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, vengono modificati i valori predefiniti per il formato di file. Vengono definite le costanti di formato di file seguenti:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

Formato AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

Formato DIB.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

Formato JFIF.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

Formato JPEG.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

Formato MPEG.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

Formato RLE DIB.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

Formato RJPEG.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ SET \_ SEEK \_ EXACTLY
</dt> <dd>

Imposta il formato utilizzato per il posizionamento. Questo flag deve essere usato con MCI \_ SET \_ ON o MCI SET \_ \_ OFF. Se si specificato MCI SET ON, la riproduzione o la registrazione accede con precisione \_ al frame specificato con il flag \_ MCI \_ FROM. Questo potrebbe aggiungere un ritardo aggiuntivo se il fotogramma richiesto non è un fotogramma chiave. Se si specifica MCI SET OFF, il dispositivo cercherà un'immagine con fotogramma chiave \_ \_ che precede il fotogramma richiesto. Per alcuni file e dispositivi, questo potrebbe essere il primo frame del file. Il valore predefinito per questo flag è dipendente dal dispositivo.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI \_ DGV \_ SET \_ SPEED
</dt> <dd>

Un parametro speed è incluso nel **membro dwSpeed** della struttura identificata da *lpSet*. La velocità viene specificata come rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata in cui la frequenza dei fotogrammi nominali è designata come 1000. La velocità media è 500 e la velocità doppia è 2000. L'intervallo di velocità consentito dipende dal dispositivo e probabilmente anche dal file.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI \_ DGV \_ SET \_ STILL
</dt> <dd>

Se usato con MCI \_ DGV \_ SET \_ FILEFORMAT, MCI \_ SET imposta il formato di file usato per i comandi di acquisizione.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Per i dispositivi video digitali, il *parametro lpSet* punta a una [**struttura MCI \_ DGV \_ SET \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo sequencer:**

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ SEQ \_ FORMAT \_ SONGPTR
</dt> <dd>

Imposta il formato dell'ora su unità puntatore del brano.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ SEQ \_ SET \_ MASTER
</dt> <dd>

Imposta il sequencer come origine dei dati di sincronizzazione e indica che il tipo di sincronizzazione è specificato nel **membro dwMaster** della struttura identificata da *lpSet*. MCISEQ restituisce MCIERR \_ UNSUPPORTED \_ FUNCTION. Per il tipo di sincronizzazione vengono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

Sequencer invierà i dati di sincronizzazione in formato MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

Sequencer invierà i dati di sincronizzazione in formato SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

Sequencer non invierà dati di sincronizzazione.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI \_ SEQ \_ SET \_ OFFSET
</dt> <dd>

Modifica l'offset SMPTE di una sequenza in quello specificato dal **membro dwOffset** della struttura identificata da *lpSet*. Questo influisce solo sulle sequenze con un tipo di divisione SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ SEQ \_ SET \_ PORT
</dt> <dd>

Imposta la porta MIDI di output di una sequenza su quella specificata dall'identificatore di dispositivo MIDI nel membro **dwPort** della struttura identificata da *lpSet*. Il dispositivo chiude la porta precedente (se presente) e tenta di aprire e usare la nuova porta. Se ha esito negativo, restituisce un errore e riapre la porta usata in precedenza (se presente). Per le porte vengono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

Chiude la porta usata in precedenza (se presente). Il sequencer si comporta esattamente come se una porta fosse aperta, ad eccezione del fatto che non viene inviato alcun messaggio MIDI.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI \_ MAPPER
</dt> <dd>

Imposta la porta aperta per il mapper MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ SEQ \_ SET \_ SLAVE
</dt> <dd>

Imposta il sequencer per ricevere i dati di sincronizzazione e indica che il tipo di sincronizzazione è specificato nel **membro dwSync della** struttura identificata da *lpSet*. MCISEQ restituisce MCIERR \_ UNSUPPORTED \_ FUNCTION. Per il tipo di sincronizzazione vengono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI \_ SEQ \_ FILE
</dt> <dd>

Imposta il sequencer per ricevere i dati di sincronizzazione contenuti nel file MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ SEQ \_ MIDI
</dt> <dd>

Imposta il sequencer per ricevere i dati di sincronizzazione MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ SEQ \_ NONE
</dt> <dd>

Imposta il sequencer per ignorare i dati di sincronizzazione in un flusso MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ SEQ \_ SMPTE
</dt> <dd>

Imposta il sequencer per ricevere i dati di sincronizzazione SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ SEQ \_ SET \_ TEMPO
</dt> <dd>

Imposta il tempo della sequenza MIDI su quello specificato dal **membro dwTempo** della struttura a cui punta *lpSet*. Per le sequenze con tipo di divisione PPQN, il tempo viene specificato in picchi al minuto; per le sequenze con tipo di divisione SMPTE, il tempo viene specificato in fotogrammi al secondo.

</dd> </dl>

Per i dispositivi Sequencer, il *parametro lpSet* punta a una [**struttura MCI \_ SEQ SET \_ \_ PARMS.**](mci-seq-set-parms.md)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI \_ VCR \_ SET \_ ASSEMBLE \_ RECORD
</dt> <dd>

Imposta il dispositivo da registrare in modalità di assemblaggio o inserimento (quando l'assemblaggio è disattivato, l'inserimento è on e viceversa). Usare con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Imposta assemble record on e disattiva l'inserimento di record. Registra tutte le tracce video, audio e timecode.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Imposta assemble record off e attiva l'inserimento di record. Quando assemble record è disattivato, è possibile selezionare singole tracce di video, audio e timecode per la registrazione.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR \_ SET \_ CLOCK
</dt> <dd>

Il **membro dwClock** della struttura identificata da *lpSet* contiene la nuova ora del clock.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR \_ SET \_ COUNTER \_ FORMA
</dt> <dd>

Il **membro dwCounterFormat** della struttura identificata da *lpSet* contiene una costante che specifica il nuovo formato dell'ora del contatore da usare per il contatore dello stato. Per un elenco di costanti valide, vedere MCI \_ SET \_ TIME FORMAT \_ nell'elenco di flag aggiuntivi per questo comando.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI \_ VCR \_ SET \_ COUNTER \_ VALUE
</dt> <dd>

Il **membro dwCounterValue** della struttura identificata da *lpSet* contiene il nuovo valore del contatore.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI \_ VCR \_ SET \_ INDEX
</dt> <dd>

Il **membro dwIndex** della struttura identificata da *lpSet* contiene una costante che indica il contenuto dello schermo e deve essere uno dei seguenti:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>CONTATORE \_ DELL'INDICE DEL VCR MCI \_ \_
</dt> <dd>

Visualizza il contatore.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI \_ VCR \_ INDEX \_ DATE
</dt> <dd>

Visualizza la data.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI \_ VCR \_ INDEX \_ TIME
</dt> <dd>

Visualizza l'ora.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>CODICE TEMPORALE \_ \_ DELL'INDICE DEL \_ VCR MCI
</dt> <dd>

Visualizza il timecode.

Per altre informazioni, vedere il [comando MCI \_ INDEX.](mci-index.md)

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI \_ VCR \_ SET \_ PAUSE \_ TIMEOUT
</dt> <dd>

Il **membro dwPauseTimeout** della struttura identificata da *lpSet* contiene la durata massima, in millisecondi, di un comando di sospensione.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI \_ VCR \_ SET \_ POSTROLL \_ DURATION
</dt> <dd>

Il membro **dwPostrollDuration** della struttura identificata da *lpSet* contiene la lunghezza della videotape, nel formato di ora corrente, necessaria per bloccare il trasporto vcr quando viene eseguito un comando stop o pause.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ SET \_ POWER
</dt> <dd>

Consente di spegnere o spegnere l'alimentazione. Deve essere usato con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Disattiva l'alimentazione.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Attiva l'accensione.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI \_ VCR \_ SET \_ PREROLL \_ DURATION
</dt> <dd>

Il **membro dwPrerollDuration** della struttura identificata da *lpSet* contiene la lunghezza della videotape, nel formato di ora corrente, necessaria per stabilizzare l'output del videoregistratore.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>FORMATO DI RECORD \_ DEL \_ SET DI VCR \_ MCI \_
</dt> <dd>

Il **membro dwRecordFormat** della struttura identificata da *lpSet* contiene una costante che descrive la velocità del record, che deve essere una delle seguenti:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR \_ FORMAT \_ EP
</dt> <dd>

Registra a velocità ridotta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>LP \_ FORMATO VCR MCI \_ \_
</dt> <dd>

Registra a velocità medio-lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR \_ FORMAT \_ SP
</dt> <dd>

Registra alla velocità standard.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>IMPOSTARE LA VELOCITÀ \_ DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwSpeed** della struttura identificata da *lpSet* contiene la nuova impostazione di velocità, dove 1000 è la velocità normale, 2000 è a doppia velocità, 500 è a metà velocità e così via.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ SET \_ TAPE \_ LENGTH
</dt> <dd>

Il **membro dwTapeLength** della struttura identificata da *lpSet* contiene la nuova lunghezza del nastro, a condizione che la lunghezza del nastro non sia rilevabile.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR \_ SET \_ TIME \_ MODE
</dt> <dd>

Il **membro dwTimeMode** della struttura identificata da *lpSet* contiene una costante che indica la nuova modalità temporale posizionale. Sono valide le costanti seguenti:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>CONTATORE DEL \_ TEMPO DEL VCR MCI \_ \_
</dt> <dd>

Forza l'uso esclusivo del contatore da parte del dispositivo.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>RILEVAMENTO ORA DEL VCR MCI \_ \_ \_
</dt> <dd>

Ogni volta che viene inserita una nuova videotape nel dispositivo o la modalità cambia da non pronta a pronta, il dispositivo deve tentare di determinare se nella videotape è disponibile un timecode. Se il timecode è disponibile, usare il timecode in tutti i comandi successivi che specificano le posizioni. In caso contrario, usare il contatore .

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>TIMECODE \_ DEL VCR MCI \_ \_
</dt> <dd>

Forza il dispositivo a usare esclusivamente il timecode.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>RILEVAMENTO DEI \_ SET DI \_ VCR MCI \_
</dt> <dd>

Regola la velocità del trasporto del nastro vcr con una regolazione fine e deve essere usato con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ PLUS
</dt> <dd>

Aumenta la velocità di trasporto del nastro.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ MINUS
</dt> <dd>

Riduce la velocità di trasporto del nastro.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI \_ VCR \_ RESET
</dt> <dd>

Restituisce la regolazione del rilevamento su zero.

</dd> </dl>

Per i dispositivi VCR, il *parametro lpSet* punta a una [**struttura MCI \_ VCR SET \_ \_ PARMS.**](mci-vcr-set-parms.md)

Il flag aggiuntivo seguente viene usato con il tipo **di dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>TRACCIA DEL \_ FORMATO MCI VD \_ \_
</dt> <dd>

Modifica il formato dell'ora in tracce. McI usa numeri di traccia continui.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Imposta l'input usato per la registrazione sul **membro wInput** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>OUTPUT DELLE ONDE MCI \_ \_
</dt> <dd>

Imposta l'output usato per la riproduzione sul **membro wOutput** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI \_ WAVE \_ SET \_ ANYINPUT
</dt> <dd>

Per la registrazione è possibile usare qualsiasi input wave compatibile con il formato corrente.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI \_ WAVE \_ SET \_ ANYOUTPUT
</dt> <dd>

Per la riproduzione è possibile usare qualsiasi output audio compatibile con il formato corrente.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
</dt> <dd>

Imposta i byte al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nAvgBytesPerSec** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI \_ WAVE \_ SET \_ BITSPERSAMPLE
</dt> <dd>

Imposta i bit per campione usati per la riproduzione, la registrazione e il salvataggio nel membro **nBitsPerSample** del formato dati PCM identificato da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI \_ WAVE \_ SET \_ BLOCKALIGN
</dt> <dd>

Imposta l'allineamento del blocco usato per la riproduzione, la registrazione e il salvataggio nel membro **nBlockAlign** della struttura identificata da *lpSet.*

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>CANALI DEL SET DI ONDE MCI \_ \_ \_
</dt> <dd>

Il numero di canali è indicato nel **membro nChannels** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI \_ WAVE \_ SET \_ FORMATTAG
</dt> <dd>

Imposta il tipo di formato usato per la riproduzione, la registrazione e il salvataggio nel membro **wFormatTag** della struttura identificata da *lpSet*. Se si specifica WAVE \_ FORMAT \_ PCM, il formato viene modificato in PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI \_ WAVE \_ SET \_ SAMPLESPERSEC
</dt> <dd>

Imposta gli esempi al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nSamplesPerSec** della struttura identificata da *lpSet*.

</dd> </dl>

Per i dispositivi audio waveform, il *parametro lpSet* punta a una [**struttura MCI WAVE SET \_ \_ \_ PARMS.**](mci-wave-set-parms.md)

Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio waveform. Queste proprietà descrivono il modo in cui i dati sono strutturati all'interno del file e non possono essere modificati una volta avviata la registrazione. L'elenco seguente di flag identifica queste proprietà:

-   MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
-   MCI \_ WAVE \_ SET \_ BITSPERSAMPLE
-   MCI \_ WAVE \_ SET \_ BLOCKALIGN
-   CANALI DEL SET DI ONDE MCI \_ \_ \_
-   MCI \_ WAVE \_ SET \_ FORMATTAG
-   MCI \_ WAVE \_ SET \_ SAMPLESPERSEC

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

