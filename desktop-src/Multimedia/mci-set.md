---
title: Comando MCI_SET (mmsystem. h)
description: Il \_ set di comandi MCI set imposta le informazioni sul dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Comando MCI_SET Windows Multimedia
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
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320057"
---
# <a name="mci_set-command"></a>\_Comando set MCI

> [!NOTE]
> Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.  Questo testo viene usato in quanto è attualmente il testo usato nei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.

Il \_ set di comandi MCI set imposta le informazioni sul dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri set di MCI**](mci-set-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano \_ set MCI:

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>\_audio set \_ MCI
</dt> <dd>

Un numero di canale audio è incluso nel membro dwAudio della struttura identificata da *lpSet*. Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off. Per indicare il numero di canale, utilizzare una delle costanti seguenti:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>\_ \_ tutti i set audio MCI \_
</dt> <dd>

Tutti i canali audio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>\_audio set \_ MCI \_ lasciato
</dt> <dd>

Canale sinistro.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>\_set di \_ audio a \_ destra di MCI
</dt> <dd>

Canale destro.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>\_sportello set \_ MCI \_ chiuso
</dt> <dd>

Chiude il coperchio del supporto (se presente).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>\_ \_ Apri sportello set \_ MCI
</dt> <dd>

Apre il coperchio del supporto (se presente).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Disabilita il video o il canale audio specificato.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Abilita il canale audio o video specificato.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_ \_ formato ora set \_ MCI
</dt> <dd>

Un parametro di formato dell'ora è incluso nel membro **dwTimeFormat** della struttura identificata da *lpSet*. Con questo flag vengono usati i flag seguenti:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_byte in formato MCI \_
</dt> <dd>

All'interno di un formato dati PCM (Pulse Code Modulation), modifica la descrizione del membro dell'ora in byte per l'input o l'output. Riconosciuta dal tipo di dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_frame di formato MCI \_
</dt> <dd>

I comandi successivi utilizzeranno i frame. Riconosciuta dai tipi di dispositivi **digitalvideo**, **VCR** e **videodisco** .

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS
</dt> <dd>

Modifica il formato dell'ora in ore, minuti e secondi. Riconosciuta dai tipi di dispositivo **VCR** e **videodisco** .

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>\_ \_ millisecondi formato MCI
</dt> <dd>

Modifica il formato dell'ora in millisecondi. Riconosciuta da tutti i tipi di dispositivo.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_MSF formato \_ MCI
</dt> <dd>

Modifica il formato dell'ora in minuti, secondi e frame. Riconosciuta dai tipi di dispositivo **CDAudio** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_esempi di formato MCI \_
</dt> <dd>

Modifica il formato dell'ora in esempi per l'input o l'output. Riconosciuta dal tipo di dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ Format \_ SMPTE \_ 24, MCI \_ Format \_ SMPTE \_ 25 e MCI \_ Format \_ SMPTE \_ 30
</dt> <dd>

Imposta il formato dell'ora su 24, 25 e 30 frame SMPTE (Society of Motion Picture and Television Engineers), rispettivamente. Riconosciuta dai tipi di dispositivo **sequencer** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ \_ 30DROP
</dt> <dd>

Imposta il formato dell'ora su 30 SMPTE del frame di rilascio. Riconosciuta dai tipi di dispositivo **sequencer** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF
</dt> <dd>

Modifica il formato dell'ora in tracce, minuti, secondi e frame. (MCI usa i numeri di traccia continui). Riconosciuta dai tipi di dispositivo **CDAudio** e **VCR** .

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_video su set MCI \_
</dt> <dd>

Imposta il segnale video su on o off. Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off. I dispositivi che non hanno il video restituiscono MCIERR \_ funzione non supportata \_ .

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>\_ \_ set \_ FileFormat DGV di MCI
</dt> <dd>

Un parametro del formato di file è incluso nel membro **dwFileFormat** della struttura identificata da *lpSet*. Per i dispositivi digitali video, il formato di file viene usato per i comandi di salvataggio o acquisizione. Se omesso, per impostazione predefinita è possibile che sia un formato definito dal driver di dispositivo. Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, verranno modificati nei valori predefiniti per il formato di file. Sono definite le costanti di formato di file seguenti:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>DGV di MCI \_ \_ FF \_ AVI
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss
</dt> <dd>

Formato AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>\_DIB DGV MCI \_ FF \_
</dt> <dd>

Formato DIB.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

Formato JFIF.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>DGV di MCI \_ \_ FF \_ JPEG
</dt> <dd>

Formato JPEG.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>DGV di MCI \_ \_ FF \_ MPEG
</dt> <dd>

Formato MPEG.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

Formato DIB RLE.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

Formato RJPEG.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>la \_ ricerca del set di DGV MCI è \_ \_ \_ esatta
</dt> <dd>

Imposta il formato utilizzato per il posizionamento. Questo flag deve essere utilizzato con MCI \_ impostato \_ su o MCI \_ impostato su \_ off. Se \_ \_ è specificato MCI impostato su, la riproduzione o la registrazione di accede con precisione al frame specificato con il \_ flag MCI from. Questo potrebbe aggiungere un ritardo aggiuntivo se il frame richiesto non è un fotogramma chiave. Se \_ si specifica MCI impostato su \_ off, il dispositivo cercherà un'immagine con fotogrammi chiave che precede il frame richiesto. Per alcuni file e dispositivi, potrebbe trattarsi del primo frame del file. Il valore predefinito per questo flag è dipendente dal dispositivo.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocità di \_ impostazione \_ DGV MCI
</dt> <dd>

Un parametro della velocità è incluso nel membro **dwSpeed** della struttura identificata da *lpSet*. La velocità viene specificata come rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata, in cui la frequenza dei fotogrammi nominale viene designata come 1000. La metà della velocità è 500 e la velocità doppia è 2000. L'intervallo di velocità consentito dipende anche dal dispositivo e possibilmente dal file.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_set di DGV MCI \_ \_ ancora
</dt> <dd>

Se usato con MCI \_ DGV \_ set \_ FileFormat, MCI \_ set imposta il formato di file usato per i comandi di acquisizione.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Per i dispositivi digitali video, il parametro *lpSet* punta a una struttura [**MCI \_ DGV \_ set \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .

Con il tipo di dispositivo **sequencer** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_ \_ formato SONGPTR MCI \_ Seq
</dt> <dd>

Imposta il formato dell'ora sulle unità del puntatore del brano.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_ \_ Master set Seq di MCI \_
</dt> <dd>

Imposta sequencer come origine dei dati di sincronizzazione e indica che il tipo di sincronizzazione viene specificato nel membro **dwMaster** della struttura identificata da *lpSet*. MCISEQ restituisce la \_ funzione MCIERR non supportata \_ . Per il tipo di sincronizzazione sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>\_MIDI seq \_ MIDI
</dt> <dd>

Sequencer invierà i dati di sincronizzazione del formato MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>sequenza di MCI \_ seq \_
</dt> <dd>

Sequencer invierà i dati di sincronizzazione del formato SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_
</dt> <dd>

Sequencer non invierà i dati di sincronizzazione.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>\_ \_ offset set seq \_
</dt> <dd>

Modifica l'offset SMPTE di una sequenza in quella specificata dal membro **dwOffset** della struttura identificata da *lpSet*. Questa operazione ha effetto solo sulle sequenze con un tipo di divisione SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_ \_ porta set SEQ per MCI \_
</dt> <dd>

Imposta la porta MIDI di output di una sequenza su quella specificata dall'identificatore del dispositivo MIDI nel membro **dwPort** della struttura identificata da *lpSet*. Il dispositivo chiude la porta precedente (se presente) e tenta di aprire e usare la nuova porta. Se ha esito negativo, restituisce un errore e riapre la porta usata in precedenza (se presente). Per le porte sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_
</dt> <dd>

Chiude la porta utilizzata in precedenza (se presente). Sequencer si comporta esattamente come se fosse aperta una porta, ad eccezione del fatto che non viene inviato alcun messaggio MIDI.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_Mapper MIDI
</dt> <dd>

Imposta la porta aperta per il mapper MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>\_ \_ set \_ slave per MCI Seq
</dt> <dd>

Imposta sequencer per la ricezione dei dati di sincronizzazione e indica che il tipo di sincronizzazione viene specificato nel membro **dwSlave** della struttura identificata da *lpSet*. MCISEQ restituisce la \_ funzione MCIERR non supportata \_ . Per il tipo di sincronizzazione sono definite le costanti seguenti:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_file SEQ di MCI \_
</dt> <dd>

Imposta sequencer per la ricezione dei dati di sincronizzazione contenuti nel file MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>\_MIDI seq \_ MIDI
</dt> <dd>

Imposta sequencer per la ricezione dei dati di sincronizzazione MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_nessuno Seq seq \_
</dt> <dd>

Imposta sequencer per ignorare i dati di sincronizzazione in un flusso MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>sequenza di MCI \_ seq \_
</dt> <dd>

Imposta sequencer per la ricezione dei dati di sincronizzazione SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_ \_ set \_ tempo per MCI Seq
</dt> <dd>

Imposta il tempo della sequenza MIDI su quello specificato dal membro **dwTempo** della struttura a cui punta *lpSet*. Per le sequenze con tipo di divisione PPQN, il tempo viene specificato in battute al minuto; per le sequenze con tipo di divisione SMPTE, il tempo viene specificato in frame al secondo.

</dd> </dl>

Per i dispositivi sequencer, il parametro *lpSet* punta a una struttura [**parametri di MCI \_ seq \_ set \_**](mci-seq-set-parms.md) .

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_record di \_ \_ assemblaggio set VCR MCI \_
</dt> <dd>

Imposta la registrazione del dispositivo in modalità assembla o Inserisci (quando il montaggio è disattivato, INSERT è on e viceversa). Usare con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Imposta assembla record su e disattiva il record di inserimento. Registra tutte le tracce video, audio e timecode.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Imposta assembla record off e attiva il record di inserimento. Quando il record di assemblaggio è disattivato, è possibile selezionare singole tracce di video, audio e timecode per la registrazione.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_ \_ clock set VCR \_ MCI
</dt> <dd>

Il membro **dwClock** della struttura identificata da *lpSet* contiene la nuova ora di clock.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>forma \_ \_ contatore set \_ VCR \_ MCI
</dt> <dd>

Il membro **dwCounterFormat** della struttura identificata da *lpSet* contiene una costante che specifica il nuovo formato del contatore di tempo che deve essere utilizzato dal contatore di stato. Per un elenco di costanti valide, vedere MCI \_ set \_ time \_ format nell'elenco di flag aggiuntivi per questo comando.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_ \_ \_ valore contatore set VCR \_ MCI
</dt> <dd>

Il membro **dwCounterValue** della struttura identificata da *lpSet* contiene il nuovo valore del contatore.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_ \_ indice set VCR \_ MCI
</dt> <dd>

Il membro **dwIndex** della struttura identificata da *lpSet* contiene una costante che indica il contenuto della visualizzazione sullo schermo e deve essere uno dei seguenti:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_ \_ contatore indice VCR \_ MCI
</dt> <dd>

Visualizza il contatore.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_Data di \_ Indice MCI VCR \_
</dt> <dd>

Visualizza la data.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_ora di \_ indicizzazione VCR MCI \_
</dt> <dd>

Visualizza l'ora.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_ \_ codice temporale dell'indice MCI VCR \_
</dt> <dd>

Visualizza il timecode.

Per ulteriori informazioni, vedere il comando [MCI \_ index](mci-index.md) .

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_timeout della \_ \_ pausa set del VCR \_ MCI
</dt> <dd>

Il membro **dwPauseTimeout** della struttura identificata da *lpSet* contiene la durata massima, in millisecondi, di un comando di sospensione.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>\_ \_ \_ durata postroll del set di VCR MCI \_
</dt> <dd>

Il membro **dwPostrollDuration** della struttura identificata da *lpSet* contiene la lunghezza del nastro, nel formato dell'ora corrente, necessaria per bloccare il trasporto del videoregistratore quando viene emesso un comando di arresto o sospensione.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_ \_ Power set VCR \_ MCI
</dt> <dd>

Consente di attivare o disattivare l'accensione. Deve essere usato con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato
</dt> <dd>

Disattiva lo spegnimento.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su
</dt> <dd>

Attiva l'accensione.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_ \_ \_ durata preregistrazione set VCR \_ MCI
</dt> <dd>

Il membro **dwPrerollDuration** della struttura identificata da *lpSet* contiene la lunghezza del nastro, nel formato dell'ora corrente, necessaria per stabilizzare l'output del VCR.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_ \_ \_ formato record set VCR \_ MCI
</dt> <dd>

Il membro **dwRecordFormat** della struttura identificata da *lpSet* contiene una costante che descrive la velocità del record, che deve essere uno dei seguenti:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_EP del \_ formato \_ VCR MCI
</dt> <dd>

Record a velocità ridotta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_ \_ LP formato VCR \_ MCI
</dt> <dd>

Registra la velocità media rallentata.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_ \_ SP formato VCR \_ MCI
</dt> <dd>

Registra la velocità standard.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocità di \_ set \_ VCR MCI
</dt> <dd>

Il membro **dwSpeed** della struttura identificata da *lpSet* contiene la nuova impostazione della velocità, dove 1000 è la velocità normale, 2000 è la doppia velocità e 500 è la metà della velocità e così via.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_ \_ \_ Lunghezza nastri set VCR \_ MCI
</dt> <dd>

Il membro **dwTapeLength** della struttura identificata da *lpSet* contiene la nuova lunghezza del nastro, purché la lunghezza del nastro non sia rilevabile.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_ \_ modalità ora di impostazione del VCR MCI \_ \_
</dt> <dd>

Il membro **dwTimeMode** della struttura identificata da *lpSet* contiene una costante che indica la nuova modalità di tempo posizionale. Sono valide le costanti seguenti:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ contatore tempo VCR \_ MCI
</dt> <dd>

Impone al dispositivo di usare esclusivamente il contatore.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_ \_ rilevamento ora VCR \_ MCI
</dt> <dd>

Ogni volta che un nuovo nastro viene inserito nel dispositivo o la modalità passa da non pronto a pronto, il dispositivo deve tentare di determinare se è disponibile un timecode sul nastro. Se il codice timecode è disponibile, usare il codice temporale in tutti i comandi successivi che specificano le posizioni. In caso contrario, utilizzare il contatore.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_ \_ timecode ora VCR \_ MCI
</dt> <dd>

Impone al dispositivo di usare esclusivamente il timecode.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_ \_ Rilevamento set VCR \_ MCI
</dt> <dd>

Ottimizza la velocità del trasporto del nastro VCR con una rettifica corretta e deve essere utilizzata con uno dei flag seguenti:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_VCR MCI \_ Plus
</dt> <dd>

Aumenta la velocità di trasporto del nastro.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>\_VCR MCI \_ meno
</dt> <dd>

Diminuisce la velocità del trasporto del nastro.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_reimpostazione VCR MCI \_
</dt> <dd>

Restituisce zero per la regolazione del rilevamento.

</dd> </dl>

Per i dispositivi VCR, il parametro *lpSet* punta a una struttura [**\_ \_ \_ parametri del VCR MCI**](mci-vcr-set-parms.md) .

Il flag aggiuntivo seguente viene usato con il tipo di dispositivo **videodisco** :

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_traccia del \_ formato MCI VD \_
</dt> <dd>

Modifica il formato dell'ora in tracce. MCI usa i numeri di traccia continui.

</dd> </dl>

Con il tipo di dispositivo **WaveAudio** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI
</dt> <dd>

Imposta l'input utilizzato per la registrazione nel membro **wInput** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI
</dt> <dd>

Imposta l'output utilizzato per la riproduzione nel membro **wOutput** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>\_set di Wave MCI \_ \_ ANYINPUT
</dt> <dd>

Qualsiasi input wave compatibile con il formato corrente può essere usato per la registrazione.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>\_set di Wave MCI \_ \_ ANYOUTPUT
</dt> <dd>

Qualsiasi output wave compatibile con il formato corrente può essere usato per la riproduzione.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>\_set di Wave MCI \_ \_ AVGBYTESPERSEC
</dt> <dd>

Imposta i byte al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nAvgBytesPerSec** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_set di Wave MCI \_ \_ BitsPerSample
</dt> <dd>

Imposta i bit per esempio usati per la riproduzione, la registrazione e il salvataggio nel membro **nBitsPerSample** del formato di dati PCM identificato da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>\_set di Wave MCI \_ \_ BLOCKALIGN
</dt> <dd>

Imposta l'allineamento del blocco utilizzato per la riproduzione, la registrazione e il salvataggio nel membro **nBlockAlign** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_ \_ canali set Wave \_ MCI
</dt> <dd>

Il numero di canali è indicato nel membro **nChannels** della struttura identificata da *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>\_set di Wave MCI \_ \_ FORMATTAG
</dt> <dd>

Imposta il tipo di formato utilizzato per la riproduzione, la registrazione e il salvataggio nel membro **wFormatTag** della struttura identificata da *lpSet*. Specificando \_ \_ il PCM in formato Wave, il formato viene modificato in PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>\_set di Wave MCI \_ \_ SAMPLESPERSEC
</dt> <dd>

Imposta gli esempi al secondo usati per la riproduzione, la registrazione e il salvataggio nel membro **nSamplesPerSec** della struttura identificata da *lpSet*.

</dd> </dl>

Per i dispositivi Waveform-Audio, il parametro *lpSet* punta a una struttura [**parametri del \_ \_ set \_ di Wave MCI**](mci-wave-set-parms.md) .

Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio della forma d'onda. Queste proprietà descrivono la struttura dei dati all'interno del file e non possono essere modificate una volta avviata la registrazione. Il seguente elenco di flag identifica queste proprietà:

-   \_set di Wave MCI \_ \_ AVGBYTESPERSEC
-   \_set di Wave MCI \_ \_ BitsPerSample
-   \_set di Wave MCI \_ \_ BLOCKALIGN
-   \_ \_ canali set Wave \_ MCI
-   \_set di Wave MCI \_ \_ FORMATTAG
-   \_set di Wave MCI \_ \_ SAMPLESPERSEC

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandi MCI](mci-commands.md)
</dt> </dl>

 

