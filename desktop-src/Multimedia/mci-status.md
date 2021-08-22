---
title: MCI_STATUS comando (Mmsystem.h)
description: Il comando MCI \_ STATUS recupera informazioni su un dispositivo MCI. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro dwReturn della struttura identificata dal parametro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9905000c718ff70435ec91bf86bf7a77d14379ed7ca557eaa85fb0df594196c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784281"
---
# <a name="mci_status-command"></a>Comando MCI \_ STATUS

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo riconosce come parola di esclusione.  Questa formulazione viene usata perché è attualmente la formulazione usata all'interno dei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo che sia allineato.

Il comando MCI \_ STATUS recupera informazioni su un dispositivo MCI. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro **dwReturn** della struttura identificata dal *parametro lpStatus.*

Per inviare questo comando, chiamare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificatore di dispositivo del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o, per i dispositivi digital-video e VCR, MCI \_ TEST. Per informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Puntatore a [**una struttura MCI \_ STATUS \_ PARMS.**](mci-status-parms.md) I dispositivi con set di comandi estesi potrebbero sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I flag standard e specifici dei comandi seguenti si applicano a tutti i dispositivi che supportano LO STATO \_ MCI:

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>ELEMENTO DI STATO MCI \_ \_
</dt> <dd>

Specifica che il **membro dwItem** della struttura identificata da *lpStatus* contiene una costante che specifica quale elemento di stato ottenere. Le costanti seguenti definiscono l'elemento di stato da restituire nel membro **dwReturn** della struttura :

STATO MCI \_ \_ TRACCIA \_ CORRENTE

Il **membro dwReturn** è impostato sul numero di traccia corrente. MCI usa numeri di traccia continui.

LUNGHEZZA \_ DELLO STATO MCI \_

Il **membro dwReturn** è impostato sulla lunghezza totale del supporto.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MODALITÀ DI \_ STATO MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla modalità corrente del dispositivo. Le modalità includono quanto segue:

-   MODALITÀ MCI \_ \_ NON \_ PRONTA
-   SOSPENSIONE DELLA MODALITÀ MCI \_ \_
-   MODALITÀ MCI \_ \_ PLAY
-   ARRESTO DELLA MODALITÀ MCI \_ \_
-   MODALITÀ MCI \_ \_ APERTA
-   RECORD IN MODALITÀ MCI \_ \_
-   MODALITÀ MCI \_ \_ SEEK

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>NUMERO DI \_ TRACCE \_ DELLO STATO MCI \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sul numero totale di tracce riproducibili.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>POSIZIONE \_ DELLO STATO MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla posizione corrente.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>STATO MCI \_ \_ PRONTO
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il dispositivo è pronto. è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>FORMATO ORA STATO MCI \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sul formato di ora corrente del dispositivo. I formati di ora includono:

-   BYTE IN FORMATO MCI \_ \_
-   FRAME IN FORMATO MCI \_ \_
-   FORMATO MCI \_ \_ HMS
-   MILLISECONDI \_ DI FORMATO \_ MCI
-   FORMATO MCI \_ \_ MSF
-   ESEMPI DI FORMATO MCI \_ \_
-   FORMATO MCI \_ \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>AVVIO DELLO \_ STATO MCI \_
</dt> <dd>

Ottiene la posizione iniziale del supporto. Per ottenere la posizione iniziale, combinare questo flag con MCI STATUS ITEM e impostare il membro dwItem della struttura identificata da \_ \_ *lpStatus* su MCI STATUS  \_ \_ POSITION.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>TRACCIA \_ MCI
</dt> <dd>

Indica che un parametro della traccia di stato è incluso nel **membro dwTrack** della struttura identificata da *lpStatus*. È necessario usare questo flag con le costanti MCI STATUS POSITION o \_ \_ MCI \_ STATUS \_ LENGTH. Se usato con MCI \_ STATUS \_ POSITION, MCI \_ TRACK ottiene la posizione iniziale della traccia specificata. Se usato con MCI \_ STATUS \_ LENGTH, MCI \_ TRACK ottiene la lunghezza della traccia specificata. MCI usa numeri di traccia continui.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo cdaudio.** Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>TRACCIA DEL TIPO \_ DI STATO CDA \_ \_ \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato su uno dei valori seguenti:

-   MCI \_ CDA \_ TRACK \_ AUDIO
-   MCI \_ CDA \_ TRACK \_ OTHER

Per usare questo flag, è necessario impostare il flag MCI TRACK e il membro dwTrack della struttura identificata da \_ *lpStatus* deve contenere un numero di  traccia valido.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto viene inserito nel dispositivo; è impostato su **FALSE in caso contrario.**

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>STATO \_ MCI DGV \_ \_ DISKSPACE
</dt> <dd>

Il **membro lpstrDrive** della struttura identificata da *lpStatus* specifica un'unità disco o, in alcune implementazioni, un percorso. Il comando MCI STATUS restituisce la quantità approssimativa di spazio su disco che può essere ottenuta dal \_ [comando MCI \_ RESERVE](mci-reserve.md) nel membro **dwReturn** della struttura identificata da *lpStatus*. Lo spazio su disco viene misurato in unità del formato di ora corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>INPUT STATO \_ MCI DGV \_ \_
</dt> <dd>

La costante specificata dal **membro dwItem** della struttura identificata da *lpStatus* si applica all'input.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>STATO \_ MCI DGV \_ \_ A SINISTRA
</dt> <dd>

La costante specificata dal **membro dwItem** della struttura identificata da *lpStatus* si applica al canale audio sinistro.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>STATO \_ MCI DGV \_ \_ NOMINALE
</dt> <dd>

La costante specificata dal **membro dwItem** della struttura identificata da *lpStatus* richiede il valore nominale anziché il valore corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>OUTPUT DELLO \_ STATO MCI DGV \_ \_
</dt> <dd>

La costante specificata dal **membro dwItem** della struttura identificata da *lpStatus* si applica all'output.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>RECORD DI \_ STATO MCI DGV \_ \_
</dt> <dd>

La frequenza dei fotogrammi restituita per il flag MCI \_ DGV \_ STATUS FRAME RATE è la \_ \_ frequenza usata per la compressione.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>INFORMAZIONI DI RIFERIMENTO SULLO STATO DI MCI \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** della struttura identificata da *lpStatus* restituisce l'immagine del fotogramma chiave più vicina che precede il frame specificato nel **membro dwReference.**

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI \_ DGV \_ STATUS \_ RIGHT
</dt> <dd>

La costante specificata dal **membro dwItem** della struttura identificata da *lpStatus* si applica al canale audio destro.

</dd> </dl>

Le costanti seguenti vengono usate con il tipo di dispositivo **digitalvideo** nel membro **dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI STATUS ITEM per \_ il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>INTERRUZIONI AUDIO DI STATO DI MCI \_ AVI \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI si è disaffezionata. Il sistema conta un'interruzione audio ogni volta che tenta di scrivere dati audio nel driver di dispositivo e rileva che il driver ha già riprodotto tutti i dati disponibili. Questo flag viene riconosciuto solo dal driver video digitale MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>FRAME DI \_ STATO DI MCI AVI \_ \_ \_ IGNORATI
</dt> <dd>

Il **membro dwReturn** restituisce il numero di fotogrammi che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI. Questo flag viene riconosciuto solo dal driver video digitale MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>STATO \_ AVI MCI \_ \_ ULTIMA VELOCITÀ DI \_ \_ RIPRODUZIONE
</dt> <dd>

Il **membro dwReturn** restituisce un valore che rappresenta il tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione. Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali. Il valore 2000, ad esempio, indica che la riproduzione della sequenza AVI ha richiesto il doppio del tempo necessario per la riproduzione. Questo flag viene riconosciuto solo dal driver video digitale MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>AUDIO DI \_ STATO MCI DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce MCI ON o MCI OFF a seconda dell'opzione MCI SET AUDIO più recente \_ per il comando \_ \_ \_ [MCI \_ SET.](mci-set.md) Restituisce MCI ON se uno o entrambi gli altoparlanti \_ sono abilitati e MCI \_ OFF in caso contrario.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>INPUT AUDIO DI STATO \_ MCI DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il livello audio istantaneo approssimativo del segnale audio analogico. Un valore maggiore di 1000 implica la distorsione del ritaglio. Alcuni dispositivi possono determinare questo valore solo durante la registrazione dell'audio. A questo valore di stato non è associato alcun comando **MCI \_ SET** o [MCI \_ SETAUDIO.](mci-setaudio.md) Questo valore è correlato, ma normalizzato in modo diverso, al comando waveform-audio MCI \_ WAVE \_ STATUS \_ LEVEL.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>RECORD AUDIO DI STATO MCI \_ DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce MCI ON o MCI OFF che riflette lo stato impostato dal \_ flag \_ MCI \_ DGV \_ SETAUDIO RECORD del comando \_ **MCI \_ SETAUDIO.**

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>ORIGINE AUDIO DI STATO MCI \_ \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** restituisce l'origine del digitalizzatore audio corrente:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI \_ DGV \_ SETAUDIO \_ AVERAGE
</dt> <dd>

Specifica la media dei canali audio sinistro e destro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ A SINISTRA
</dt> <dd>

Specifica il canale audio sinistro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT
</dt> <dd>

Specifica il canale audio destro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ STEREO
</dt> <dd>

Specifica stereo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>FLUSSO AUDIO DI STATO MCI \_ \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** restituisce il numero del flusso audio corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>STATO \_ DI MCI DGV \_ \_ AVGBYTESPERSEC
</dt> <dd>

Il **membro dwReturn** restituisce il numero medio di byte al secondo usati per la registrazione.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>STATO MCI \_ DGV \_ \_ BASS
</dt> <dd>

Il **membro dwReturn** restituisce il livello basso audio corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>BITSPERPEL DI STATO MCI \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** restituisce il numero di bit per pixel usati per salvare i dati acquisiti o registrati.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>BITSPERSAMPLE DI STATO MCI \_ DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il numero di bit per campione che il dispositivo usa per la registrazione. Questo vale solo per i dispositivi che supportano il formato PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>BLOCCO DI \_ STATO DGV \_ \_ MCI
</dt> <dd>

Il **membro dwReturn** restituisce l'allineamento dei blocchi di dati rispetto all'inizio della forma d'onda di input.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>LUMINOSITÀ STATO \_ MCI DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il livello di luminosità video corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>COLORE STATO \_ MCI \_ DGV \_
</dt> <dd>

Il **membro dwReturn** restituisce il livello di colore corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>CONTRASTO STATO MCI \_ DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il livello di contrasto corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>FILE DI \_ STATO MCI DGVFORMAT \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce il formato di file corrente per la registrazione o il salvataggio.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MODALITÀ FILE DI \_ STATO MCI DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce lo stato dell'operazione file:

MODIFICA DELLA \_ MODALITÀ FILE MCI DGV \_ \_ \_

Restituito durante le operazioni di taglia, copia, eliminazione, incolla e annullamento.

MODALITÀ FILE \_ MCI DGV \_ \_ \_ INATTIVA

Restituito quando il file è pronto per l'operazione successiva.

CARICAMENTO IN \_ MODALITÀ FILE MCI DGV \_ \_ \_

Restituito durante il caricamento del file.

SALVATAGGIO \_ IN MODALITÀ FILE MCI DGV \_ \_ \_

Restituito durante il salvataggio del file.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>COMPLETAMENTO FILE DI STATO MCI \_ DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce la percentuale stimata dell'avanzamento di un'operazione di caricamento, salvataggio, acquisizione, taglia, copia, eliminazione, incolla o annullamento. Le applicazioni possono usarlo per fornire un indicatore visivo dello stato di avanzamento. Questo flag non è supportato da tutti i dispositivi video digitali.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>INOLTRO DELLO \_ STATO MCI DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE se** la direzione del dispositivo è in avanti o il dispositivo non è in riproduzione.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>FREQUENZA FOTOGRAMMI STATO MCI \_ \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** deve essere usato con MCI \_ DGV \_ STATUS \_ NOMINAL, MCI \_ DGV \_ STATUS RECORD o \_ entrambi. Se usato con MCI \_ DGV \_ STATUS \_ RECORD, viene restituita la frequenza fotogrammi corrente usata per la registrazione. Se usato con MCI \_ DGV STATUS RECORD e \_ \_ MCI \_ DGV \_ STATUS NOMINAL, viene restituita la \_ frequenza fotogrammi nominale associata al segnale video di input. Se usato con MCI DGV STATUS NOMINAL, viene restituita la \_ \_ \_ frequenza fotogrammi nominale associata al file. In tutti i casi le unità sono in fotogrammi al secondo moltiplicate per 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>STATO \_ MCI DGV \_ \_ GAMMA
</dt> <dd>

Il **membro dwReturn** restituisce il valore gamma corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>STATO \_ MCI DGV \_ \_ HPAL
</dt> <dd>

Il **membro dwReturn** restituisce il valore decimale ASCII per l'handle del riquadro corrente. L'handle è contenuto nella parola di ordine basso del valore restituito.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>STATO \_ DGV \_ \_ MCI HWND
</dt> <dd>

Il **membro dwReturn** restituisce il valore decimale ASCII per l'handle di finestra esplicito o predefinito corrente associato a questa istanza del driver di dispositivo. L'handle è contenuto nella parola di ordine basso del valore restituito.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>COLORE DELLA CHIAVE DI STATO MCI \_ \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** restituisce il valore key-color corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI \_ DGV \_ STATUS \_ KEY \_ INDEX
</dt> <dd>

Il **membro dwReturn** restituisce il valore key-index corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MONITORAGGIO DELLO STATO DI MCI \_ DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce una costante che indica l'origine della presentazione corrente. Sono definite le costanti seguenti:

FILE DI \_ MONITORAGGIO MCI DGV \_ \_

Un file è l'origine.

INPUT DI MONITORAGGIO \_ DGV MCI \_ \_

L'input è l'origine.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>METODO DI \_ MONITORAGGIO DELLO STATO MCI DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce una costante che indica il metodo usato per il monitoraggio dell'input. Vengono definite le costanti seguenti:

MCI \_ DGV \_ METHOD \_ DIRECT

Monitoraggio diretto dell'input.

MCI \_ DGV \_ METHOD \_ POST

Monitoraggio post-input.

MCI \_ DGV \_ METHOD \_ PRE

Monitoraggio pre-input.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MODALITÀ SOSPENSIONE \_ STATO MCI DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce MCI MODE PLAY se il dispositivo è stato sospeso durante la riproduzione e restituisce MCI MODE RECORD se il dispositivo è stato sospeso durante \_ la \_ \_ \_ registrazione. Il comando restituisce MCIERR NONAPPLICABLE FUNCTION come errore \_ se il dispositivo non è in \_ pausa.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ STATUS \_ SAMPLESPERSECOND
</dt> <dd>

Il **membro dwReturn** restituisce il numero di campioni registrati al secondo.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV \_ STATUS \_ SEEK \_ EXACTLY
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE** o **FALSE** che indica se il formato di ricerca è impostato o meno esattamente. Le applicazioni possono impostare questo formato usando il [comando MCI \_ SET](mci-set.md) con il flag MCI \_ DGV \_ SET SEEK \_ \_ EXACTLY.

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>STATO \_ MCI DGV \_ \_ SHARPNESS
</dt> <dd>

Il **membro dwReturn** restituisce il livello di nitidezza corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI \_ DGV \_ STATUS \_ SIZE
</dt> <dd>

Il **membro dwReturn** restituisce la durata approssimativa di riproduzione dei dati compressi che verranno contenuti nell'area di lavoro riservata. Le unità di durata sono nel formato di ora corrente. Restituisce zero se non è disponibile spazio su disco riservato. Le dimensioni restituite sono approssimative perché lo spazio su disco preciso per i dati compressi non può essere in genere previsto fino a dopo la compressione dei dati.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI \_ DGV \_ STATUS \_ SMPTE
</dt> <dd>

Il **membro dwReturn** restituisce il time code SMPTE associato alla posizione corrente nell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV \_ STATUS \_ SPEED
</dt> <dd>

Il **membro dwReturn** restituisce la velocità di riproduzione corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>STATO \_ MCI DGV \_ \_ ANCORA \_ FILEFORMAT
</dt> <dd>

Il **membro dwReturn** restituisce il formato di file corrente per il [comando MCI \_ CAPTURE.](mci-capture.md)

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV \_ STATUS \_ TINT
</dt> <dd>

Il **membro dwReturn** restituisce il livello di tinta video corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI \_ DGV \_ STATUS \_ TREBLE
</dt> <dd>

Il **membro dwReturn** restituisce il livello audio acuto corrente. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>STATO \_ MCI DGV \_ \_ NON SALVATO
</dt> <dd>

Il membro **dwReturn** restituisce **TRUE** se nell'area di lavoro sono presenti dati registrati che potrebbero essere persi in seguito a un comando [MCI \_ CLOSE,](mci-close.md) [MCI \_ LOAD,](mci-load.md) [MCI \_ RECORD,](mci-record.md) [MCI \_ RESERVE,](mci-reserve.md) [MCI \_ CUT,](mci-cut.md) [MCI \_ DELETE](mci-delete.md)o [MCI \_ PASTE.](mci-paste.md) In caso contrario, **il membro restituisce FALSE.**

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>VIDEO SULLO \_ STATO DI MCI DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce MCI ON se il video è abilitato \_ o MCI OFF se è \_ disabilitato.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>RECORD VIDEO \_ STATO MCI DGV \_ \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce MCI ON o MCI OFF, che riflette lo stato impostato dal \_ flag \_ \_ MCI DGV SETVIDEO RECORD del comando \_ \_ [MCI \_ SETVIDEO.](mci-setvideo.md)

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>ORIGINE \_ VIDEO DI STATO MCI \_ \_ \_ DGV
</dt> <dd>

Il **membro dwReturn** restituisce una costante che indica il tipo di origine video impostato dal flag MCI \_ DGV \_ SETVIDEO \_ SOURCE del comando **MCI \_ SETVIDEO.**

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV \_ STATUS \_ VIDEO \_ SRC \_ NUM
</dt> <dd>

Il **membro dwReturn** restituisce il numero all'interno del tipo dell'origine di input video attualmente attiva.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI \_ DGV \_ STATUS \_ VIDEO \_ STREAM
</dt> <dd>

Il **membro dwReturn** restituisce il numero del flusso video corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>VOLUME DI \_ STATO MCI DGV \_ \_
</dt> <dd>

Il **membro dwReturn** restituisce la media del volume agli altoparlanti sinistro e destro. Usare MCI \_ DGV \_ STATUS NOMINAL con questo flag per ottenere il livello \_ nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>FINESTRA DI STATO DGV MCI \_ \_ \_ \_ VISIBILE
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE** se la finestra non è nascosta.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>FINESTRA DI STATO DGV MCI \_ RIDOTTA A \_ \_ \_ ICONA
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE se** la finestra è ridotta a icona.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>FINESTRA DI STATO DGV MCI \_ \_ \_ \_ INGRANDITA
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE se** la finestra è ingrandita.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** restituisce **TRUE.**

</dd> </dl>

Per i dispositivi video digitali, il *parametro lpStatus* punta a una struttura [**\_ \_ \_ PARMS DI STATO DGV MCI.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo sequencer.** Queste costanti vengono usate nel **membro dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ SEQ \_ STATUS \_ DIVTYPE
</dt> <dd>

Il **membro dwReturn** viene impostato su uno dei valori seguenti che indica il tipo di divisione corrente di una sequenza:

-   MCI \_ SEQ \_ DIV \_ PPQN
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 24
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 25
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30
-   MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI \_ SEQ \_ STATUS \_ MASTER
</dt> <dd>

Il **membro dwReturn** è impostato sul tipo di sincronizzazione usato per l'operazione master.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>OFFSET DELLO STATO DI MCI \_ SEQ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sull'offset SMPTE corrente di una sequenza.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>PORTA DI STATO DI MCI \_ \_ \_ SEQ
</dt> <dd>

Il **membro dwReturn** viene impostato sull'identificatore di dispositivo MIDI per la porta corrente usata dalla sequenza.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ SEQ \_ STATUS \_ SLAVE
</dt> <dd>

Il **membro dwReturn** è impostato sul tipo di sincronizzazione usato per l'operazione subordinata.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI \_ SEQ \_ STATUS \_ TEMPO
</dt> <dd>

Il **membro dwReturn** viene impostato sul tempo corrente di una sequenza MIDI in picchi al minuto per i file PPQN o fotogrammi al secondo per i file SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto viene inserito nel dispositivo; In caso contrario, è **impostato su FALSE.**

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo vcr.** Queste costanti vengono usate nel **membro dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto viene inserito nel dispositivo; In caso contrario, è **impostato su FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>RECORD ASSEMBLE \_ DELLO STATO DEL \_ VCR \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE se** la modalità assemble è attiva; In caso contrario, è **impostato su FALSE.**

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MONITOR AUDIO \_ DELLO STATO \_ DEL VCR \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante, che indica il tipo di monitor audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>NUMERO DI MONITOR \_ AUDIO DELLO STATO DEL \_ \_ VIDEOREGISTRATORE \_ \_ MCI
</dt> <dd>

Il **membro dwReturn** viene impostato sul numero del tipo di monitor audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>REGISTRAZIONE AUDIO DELLO \_ STATO DEL VCR MCI \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se l'audio verrà registrato quando viene fornito il comando di registrazione successivo. In caso contrario, è **impostato su FALSE.** Se si specifica MCI \_ TRACK nel *parametro dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica la richiesta.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>ORIGINE AUDIO DELLO STATO \_ DEL VCR MCI \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante, che indica il tipo di origine audio corrente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ VCR \_ STATUS \_ AUDIO \_ SOURCE \_ NUMBER
</dt> <dd>

Il **membro dwReturn** viene impostato sul numero del tipo di origine audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>OROLOGIO DI STATO \_ DEL VCR MCI \_ \_
</dt> <dd>

Il **membro dwReturn** viene impostato sul valore di clock corrente, in incrementi di clock totali.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>ID OROLOGIO \_ DELLO STATO \_ DEL VIDEOREGISTRATORE \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su un numero che descrive in modo univoco l'orologio in uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>FORMATO DEL \_ CONTATORE \_ DELLO STATO DEL \_ VIDEOREGISTRATORE \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che descrive il formato del contatore corrente. Per altre informazioni, vedere il flag MCI \_ SET TIME FORMAT del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>RISOLUZIONE DEL \_ CONTATORE \_ DELLO STATO DEL VCR \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che descrive la risoluzione del contatore ed è uno dei valori seguenti:

-   FRAME \_ MCI VCR \_ COUNTER \_ \_ RES: il contatore ha la risoluzione dei fotogrammi.
-   MCI \_ VCR \_ COUNTER \_ RES \_ SECONDS: il contatore ha una risoluzione di secondi.
-   VALORE CONTATORE STATO DEL VCR MCI: il membro \_ \_ \_ \_ **dwReturn** è impostato sulla lettura corrente del contatore, nel formato contatore corrente.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>FREQUENZA \_ FOTOGRAMMI \_ DI STATO DEL \_ VCR \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato sulla frequenza fotogrammi nativa corrente del dispositivo.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>INDICE DI STATO \_ DEL VCR \_ \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che descrive il contenuto corrente dello schermo ed è uno dei seguenti:

-   CONTATORE \_ DELL'INDICE DEL VCR \_ MCI \_
-   MCI \_ VCR \_ INDEX \_ DATE
-   TEMPO DI INDICIZZAZIONE \_ DEL VCR MCI \_ \_
-   CODICE TEMPORALE \_ \_ DELL'INDICE MCI \_ VCR

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI \_ VCR \_ STATUS \_ INDEX \_ ON
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se lo schermo è on; è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>TIPO DI SUPPORTO \_ DI \_ STATO DEL VCR \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su uno degli elementi seguenti:

-   MCI \_ VCR \_ MEDIA \_ 8MM
-   MCI \_ VCR \_ MEDIA \_ HI8
-   \_VHS MULTIMEDIALI MCI VCR \_ \_
-   MCI \_ VCR \_ MEDIA \_ SVHS
-   MCI \_ VCR \_ MEDIA \_ BETA
-   MCI \_ VCR \_ MEDIA \_ EDBETA
-   MCI \_ VCR \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>NUMERO DI STATO \_ DEL VCR \_ \_ MCI
</dt> <dd>

Il **membro dwNumber** viene impostato sul numero del siner logico quando si usa questo flag con il flag MCI \_ VCR STATUS \_ \_ TUNER \_ CHANNEL.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>NUMERO DI \_ STATO \_ DEL VIDEOREGISTRATORE MCI \_ DI TRACCE \_ \_ \_ AUDIO
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di tracce audio selezionabili in modo indipendente.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>NUMERO DI \_ STATO \_ DEL \_ VIDEOREGISTRATORE \_ \_ \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di tracce video selezionabili in modo indipendente.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>TIMEOUT DI SOSPENSIONE \_ \_ DELLO STATO DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla durata massima, in millisecondi, di un comando pause. Il valore restituito pari a zero indica che non si verificherà alcun timeout.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>FORMATO DI RIPRODUZIONE \_ DELLO \_ STATO DEL \_ VIDEOREGISTRATORE \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato su uno degli elementi seguenti:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>DURATA \_ POSTROLL DELLO \_ STATO DEL \_ VCR \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato sulla lunghezza del videotape che verrà riprodotto dopo il punto in cui è stato arrestato, nel formato ora corrente. Questa operazione è necessaria per bloccare il trasporto del nastro del videoregistratore da un comando di arresto o sospensione.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>STATO \_ DEL VIDEOREGISTRATORE MCI \_ \_ \_ ACCENSIONE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se l'alimentazione è in funzione. è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>DURATA \_ PREROLL DELLO \_ STATO DEL \_ VCR \_ MCI
</dt> <dd>

Il **membro dwReturn** è impostato sulla lunghezza del videotape che verrà riprodotto prima del punto in cui è stato avviato, nel formato ora corrente. Questa operazione è necessaria per stabilizzare l'output del videoregistratore.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>FORMATO DEL \_ RECORD DI STATO DEL \_ \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su uno degli elementi seguenti:

-   MCI \_ VCR \_ FORMAT \_ EP
-   MCI \_ VCR \_ FORMAT \_ LP
-   MCI \_ VCR \_ FORMAT \_ OTHER
-   MCI \_ VCR \_ FORMAT \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>VELOCITÀ DELLO STATO \_ DEL VCR MCI \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità corrente. Per altre informazioni, vedere il flag MCI \_ VCR \_ SET SPEED del \_ comando [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MODALITÀ TEMPO \_ DI \_ STATO DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su uno degli elementi seguenti:

-   CONTATORE DI \_ TEMPO DEL VCR MCI \_ \_
-   RILEVAMENTO \_ TEMPOR MCI VCR \_ \_
-   CODICE TEMPORALE DEL VCR MCI \_ \_ \_

Per altre informazioni, vedere il flag MCI \_ VCR \_ SET TIME MODE del comando \_ \_ [MCI \_ SET.](mci-set.md)

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>TIPO DI TEMPO \_ DI \_ STATO DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che descrive il tipo di ora corrente in uso (usato da [play](play.md), [record](record.md), [seek](seek.md)e così via) ed è uno dei seguenti:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>CONTATORE DI \_ TEMPO DEL VCR MCI \_ \_
</dt> <dd>

Il contatore è in uso.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>CODICE TEMPORALE DEL VCR MCI \_ \_ \_
</dt> <dd>

Il codice temporale è in uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>CODICE TEMPORALE \_ DELLO \_ STATO DEL \_ VCR MCI \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il codice temporale è presente nella posizione corrente nel contenuto; è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>RECORD \_ TIMECODE DI STATO \_ DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il codice temporale verrà registrato quando viene fornito il comando di record successivo. è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>TIPO DI CODICE TEMPORALE \_ \_ DELLO STATO DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che descrive il tipo di codice temporale supportato direttamente dal dispositivo ed è uno dei seguenti:

-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ NONE: questo dispositivo non usa un codice temporale.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ OTHER: questo dispositivo usa un codice temporale non specificato.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ SMPTE: questo dispositivo usa il codice temporale SMPTE.
-   MCI \_ VCR \_ TIMECODE \_ TYPE \_ SMPTE DROP: questo dispositivo usa il codice temporale \_ di rilascio SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>CANALE \_ SINER DI \_ STATO DEL VIDEOREGISTRATORE \_ MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di canale corrente. Se si specifica MCI VCR STATUS NUMBER nel \_ \_ parametro \_ *dwFlags* di questo comando, **dwNumber** contiene il numero del sintassi logica a cui si applica questo comando.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MONITORAGGIO VIDEO DELLO STATO DEL VIDEO DI MCI \_ VCR \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che indica il tipo di monitoraggio video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>NUMERO DI MONITORAGGIO \_ VIDEO DELLO STATO DEL \_ \_ VIDEO \_ \_ DI MCI VCR
</dt> <dd>

Il **membro dwReturn** è impostato sul numero del tipo di monitoraggio video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>REGISTRAZIONE VIDEO DELLO STATO DEL VIDEO DI MCI \_ VCR \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il video verrà registrato quando viene fornito il comando di record successivo. è impostato su **FALSE in caso contrario.** Se si specifica MCI \_ TRACK nel *parametro dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica questa richiesta.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>ORIGINE VIDEO DI STATO \_ \_ DEL \_ VCR MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato su una costante che indica il tipo di origine video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI VCR STATUS VIDEO SOURCE NUMBER (CODICE SORGENTE VIDEO STATO MCI \_ \_ \_ \_ \_ VCR)
</dt> <dd>

Il **membro dwReturn** è impostato sul numero del tipo di origine video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ STATUS \_ WRITE \_ PROTECTED
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto è protetto da scrittura; è impostato su **FALSE in caso contrario.**

</dd> </dl>

Per i dispositivi VCR, il *parametro lpStatus* punta a una [**struttura MCI \_ VCR STATUS \_ \_ PARMS.**](mci-vcr-status-parms.md)

L'uso del flag MCI STATUS LENGTH per determinare la lunghezza del supporto restituisce sempre 2 ore per i dispositivi vcr, a meno che la lunghezza non sia stata modificata in modo esplicito usando \_ \_ il comando [MCI \_ SET.](mci-set.md)

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo di** sovrimpressione. Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>STATO DI MCI \_ OVLY \_ \_ HWND
</dt> <dd>

Il **membro dwReturn** è impostato sull'handle della finestra associata al dispositivo di sovrapposizione video.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>ESTENSIONE DELLO STATO DI MCI \_ OVLY \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se l'estensione è abilitata. è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto viene inserito nel dispositivo; è impostato su **FALSE in caso contrario.**

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo videodisc.** Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>SUPPORTO DI STATO MCI \_ \_ \_ PRESENTE
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se il supporto viene inserito nel dispositivo; è impostato su **FALSE in caso contrario.**

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MODALITÀ DI \_ STATO MCI \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla modalità corrente del dispositivo. I dispositivi videodisc possono restituire la costante MCI VD MODE PARK, oltre alle costanti che qualsiasi dispositivo può restituire, come documentato con il \_ \_ parametro \_ *dwFlags.*

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>DIMENSIONI DISCO DI STATO DI MCI \_ VD \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla dimensione del disco caricato in pollici (8 o 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>INOLTRO DELLO STATO DI MCI \_ VD \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su **TRUE** se viene riprodotto; è impostato su **FALSE in caso contrario.**

Il dispositivo videodisc MCI non supporta questo flag.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>TIPO DI SUPPORTO DI STATO DI MCI \_ VD \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sul tipo di supporto del supporto inserito. È possibile restituire i tipi di supporti seguenti:

CAV MULTIMEDIALE MCI \_ VD \_ \_

MCI \_ VD \_ MEDIA \_ CLV

MCI \_ VD \_ MEDIA \_ OTHER

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>LATO STATO \_ VD MCI \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato su 1 o 2 per indicare il lato del disco caricato. Non tutti i dispositivi videodisc supportano questo flag.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>VELOCITÀ DELLO STATO DI MCI \_ VD \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sulla velocità di riproduzione in fotogrammi al secondo. Oggetto MCIPIONR. Il driver di dispositivo DRV restituisce MCIERR \_ UNSUPPORTED \_ FUNCTION.

</dd> </dl>

I flag aggiuntivi seguenti vengono usati con il **tipo di dispositivo waveaudio.** Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il *parametro lpStatus* quando si specifica MCI \_ STATUS ITEM per il parametro \_ *dwFlags.*

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ WAVE \_ FORMATTAG
</dt> <dd>

Il **membro dwReturn** è impostato sul tag di formato corrente usato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Il **membro dwReturn** è impostato sul dispositivo di input wave usato per la registrazione. Se nessun dispositivo è in uso e nessun dispositivo è stato impostato in modo esplicito, il valore restituito dall'errore è MCIERR \_ WAVE \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ OUTPUT
</dt> <dd>

Il **membro dwReturn** è impostato sul dispositivo di output wave usato per la riproduzione. Se nessun dispositivo è in uso e nessun dispositivo è stato impostato in modo esplicito, il risultato dell'errore è MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>STATO DI MCI \_ WAVE \_ \_ AVGBYTESPERSEC
</dt> <dd>

Il **membro dwReturn** è impostato sui byte correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>BITSPERSAMPLE DELLO STATO DI MCI \_ WAVE \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sui bit correnti per ogni campione usato per la riproduzione, la registrazione e il salvataggio di dati formattati PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>STATO DI MCI \_ WAVE \_ \_ BLOCKALIGN
</dt> <dd>

Il **membro dwReturn** è impostato sull'allineamento del blocco corrente usato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>CANALI DI STATO DELLE ONDE MCI \_ \_ \_
</dt> <dd>

Il **membro dwReturn** è impostato sul numero di canali corrente usato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>LIVELLO DI STATO DI MCI \_ \_ \_ WAVE
</dt> <dd>

Il **membro dwReturn** è impostato sul record corrente o sul livello di riproduzione dei dati formattati PCM. Il valore viene restituito come valore a 8 o 16 bit, a seconda delle dimensioni del campione usate. Il livello di canale destro o mono viene restituito nella parola meno importante. Il livello del canale sinistro viene restituito nella parola di ordine superiore.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>ESEMPI DI STATO DI MCI \_ \_ \_ WAVEPERSEC
</dt> <dd>

Il **membro dwReturn** è impostato sui campioni correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.

</dd> </dl>

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
</dt> <dt>

[MCI \_ CUT](mci-cut.md)
</dt> <dt>

[MCI \_ DELETE](mci-delete.md)
</dt> <dt>

[MCI \_ PASTE](mci-paste.md)
</dt> <dt>

[RISERVA \_ MCI](mci-reserve.md)
</dt> <dt>

[MCI \_ SET](mci-set.md)
</dt> <dt>

[Giocare](play.md)
</dt> <dt>

[Registrazione](record.md)
</dt> <dt>

[Cercare](seek.md)
</dt> </dl>

 

