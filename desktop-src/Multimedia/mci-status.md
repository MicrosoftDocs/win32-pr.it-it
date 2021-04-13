---
title: Comando MCI_STATUS (mmsystem. h)
description: Il \_ comando MCI status recupera le informazioni su un dispositivo MCI. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro dwReturn della struttura identificata dal parametro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Comando MCI_STATUS Windows Multimedia
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
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "104350691"
---
# <a name="mci_status-command"></a>\_Comando stato MCI

> [!NOTE]
> Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.  Questo testo viene usato in quanto è attualmente il testo usato nei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.

Il \_ comando MCI status recupera le informazioni su un dispositivo MCI. Tutti i dispositivi riconoscono questo comando. Le informazioni vengono restituite nel membro **dwReturn** della struttura identificata dal parametro *lpStatus* .

Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.


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

Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ . Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Puntatore a una [**struttura \_ \_ parametri di stato MCI**](mci-status-parms.md) . I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per tutti i dispositivi che supportano lo stato MCI sono validi i flag aggiuntivi e specifici dei comandi seguenti \_ :

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_elemento stato \_ MCI
</dt> <dd>

Specifica che il membro **dwItem** della struttura identificata da *lpStatus* contiene una costante che specifica l'elemento di stato da ottenere. Le costanti seguenti definiscono quale elemento di stato restituire nel membro **dwReturn** della struttura:

\_ \_ traccia corrente stato \_ MCI

Il membro **dwReturn** è impostato sul numero di traccia corrente. MCI usa i numeri di traccia continui.

\_lunghezza stato \_ MCI

Il membro **dwReturn** è impostato sulla lunghezza totale del supporto.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modalità stato \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla modalità corrente del dispositivo. Le modalità includono quanto segue:

-   \_modalità MCI \_ non \_ pronta
-   \_sospensione della modalità MCI \_
-   \_riproduzione in modalità MCI \_
-   \_arresto modalità \_ MCI
-   \_modalità MCI \_ aperta
-   \_record in modalità MCI \_
-   \_ricerca in modalità MCI \_

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ numero \_ di tracce di stato \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero totale di tracce giocabili.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posizione stato \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla posizione corrente.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_stato MCI \_ pronto
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il dispositivo è pronto; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_ \_ formato ora stato \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul formato dell'ora corrente del dispositivo. I formati di ora includono:

-   \_byte in formato MCI \_
-   \_frame di formato MCI \_
-   \_formato MCI \_ HMS
-   \_ \_ millisecondi formato MCI
-   \_MSF formato \_ MCI
-   \_esempi di formato MCI \_
-   \_formato MCI \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_inizio stato \_ MCI
</dt> <dd>

Ottiene la posizione iniziale del supporto. Per ottenere la posizione iniziale, combinare questo flag con l' \_ elemento di stato MCI \_ e impostare il membro **dwItem** della struttura identificata da *LPSTATUS* sulla \_ posizione di stato MCI \_ .

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_traccia MCI
</dt> <dd>

Indica che il parametro Track status è incluso nel membro **dwTrack** della struttura identificata da *lpStatus*. È necessario usare questo flag con la \_ posizione di stato MCI o le costanti di \_ \_ lunghezza dello stato MCI \_ . Se usata con la \_ \_ posizione di stato MCI, MCI \_ Track ottiene la posizione iniziale della traccia specificata. Se utilizzata con la \_ lunghezza dello stato MCI \_ , \_ la traccia MCI ottiene la lunghezza della traccia specificata. MCI usa i numeri di traccia continui.

</dd> </dl>

I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **CDAudio** . Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_ \_ \_ traccia tipo stato CdA \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei valori seguenti:

-   \_ \_ traccia \_ audio di MCI CdA
-   \_ \_ traccia \_ altro per MCI CdA

Per usare questo flag, \_ è necessario impostare il flag di traccia MCI e il membro **dwTrack** della struttura identificata da *lpStatus* deve contenere un numero di traccia valido.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .

</dd> </dl>

Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_ \_ diskspace stato DGV \_ MCI
</dt> <dd>

Il membro **lpstrDrive** della struttura identificata da *lpStatus* specifica un'unità disco o, in alcune implementazioni, un percorso. Il \_ comando MCI Status restituisce la quantità approssimativa di spazio su disco che può essere ottenuta dal comando [MCI \_ Reserve](mci-reserve.md) nel membro **dwReturn** della struttura identificata da *lpStatus*. Lo spazio su disco viene misurato in unità del formato ora corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_ \_ input stato DGV \_ MCI
</dt> <dd>

La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica all'input.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>\_stato DGV MCI a \_ \_ sinistra
</dt> <dd>

La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica al canale audio sinistro.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>\_stato DGV \_ MCI \_ nominale
</dt> <dd>

La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* richiede il valore nominale anziché il valore corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_ \_ output stato DGV \_ MCI
</dt> <dd>

La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica all'output.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_record di \_ stato \_ DGV MCI
</dt> <dd>

La frequenza dei fotogrammi restituiti per il \_ flag di frequenza dei fotogrammi di stato DGV di MCI \_ \_ \_ è la velocità utilizzata per la compressione.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>informazioni \_ di \_ riferimento sullo stato di DGV MCI \_
</dt> <dd>

Il membro **dwReturn** della struttura identificata da *lpStatus* restituisce l'immagine del fotogramma chiave più vicina che precede il frame specificato nel membro **dwReference** .

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_stato DGV MCI- \_ \_ diritto
</dt> <dd>

La costante specificata dal membro **dwItem** della struttura identificata da *lpStatus* si applica al canale audio corretto.

</dd> </dl>

Le costanti seguenti vengono usate con il tipo di dispositivo **digitalvideo** nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ interruzioni audio dello stato di MCI AVI \_
</dt> <dd>

Il membro **dwReturn** restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI è stata interrotta. Il sistema conta un'interruzioni audio ogni volta che tenta di scrivere i dati audio nel driver di dispositivo e rileva che il driver ha già eseguito tutti i dati disponibili. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>frame di stato di MCI \_ AVI \_ \_ \_ ignorati
</dt> <dd>

Il membro **dwReturn** restituisce il numero di frame che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>Data \_ \_ \_ ultima esecuzione stato \_ \_ di MCI AVI
</dt> <dd>

Il membro **dwReturn** restituisce un valore che rappresenta la precisione del tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione. Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali. Il valore 2000, ad esempio, indicherebbe che la sequenza AVI ha richiesto due volte la riproduzione del tempo necessario. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_ \_ audio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce MCI \_ on o MCI \_ disattivato a seconda dell'opzione più recente del \_ set \_ di impostazioni audio MCI per il comando [ \_ set MCI](mci-set.md) . Restituisce MCI \_ in se uno o entrambi gli altoparlanti sono abilitati e MCI è \_ disattivato in caso contrario.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_ \_ \_ input audio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di audio istantaneo approssimativo del segnale audio analogico. Un valore maggiore di 1000 implica la distorsione di ritaglio. Alcuni dispositivi possono determinare questo valore solo durante la registrazione dell'audio. A questo valore di stato non è associato un **\_ set MCI** o un comando [MCI \_ sefonica](mci-setaudio.md) . Questo valore è correlato a, ma normalizzato in modo diverso rispetto a, il livello di stato dell'onda MCI del comando audio Waveform \_ \_ \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_ \_ \_ record audio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce MCI \_ on o MCI \_ off che riflette lo stato impostato dal \_ \_ \_ flag di record DGV di MCI del comando **MCI \_ sefonica** .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_ \_ \_ origine audio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce l'origine del digitalizzatore audio corrente:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_media DGV \_ MCI \_
</dt> <dd>

Specifica la media dei canali audio sinistro e destro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ \_ Left
</dt> <dd>

Specifica il canale audio sinistro.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>DGV MCI a \_ \_ \_ destra
</dt> <dd>

Specifica il canale audio corretto.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ sefonica \_ stereo
</dt> <dd>

Specifica lo stereo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_ \_ \_ flusso audio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero di flusso audio corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>\_ \_ AVGBYTESPERSEC stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero medio di byte al secondo usati per la registrazione.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_ \_ basso stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di basso audio corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_ \_ BITSPERPEL stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero di bit per pixel usato per salvare i dati acquisiti o registrati.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_ \_ BitsPerSample stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero di bit per campione usato dal dispositivo per la registrazione. Questo vale solo per i dispositivi che supportano il formato PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>\_ \_ BLOCKALIGN stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce l'allineamento dei blocchi di dati rispetto all'inizio della forma d'onda di input.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>\_ \_ luminosità stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di luminosità del video corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_ \_ colore stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di colore corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_ \_ contrasto stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di contrasto corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_formato fileDGV di \_ stato MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce il formato di file corrente per la registrazione o il salvataggio.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_ \_ modalità file di stato DGV \_ MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce lo stato dell'operazione file:

\_modifica in \_ \_ modalità file DGV MCI \_

Restituito durante le operazioni Taglia, copia, Elimina, Incolla e Annulla.

\_inattività \_ in \_ modalità file DGV \_ MCI

Restituito quando il file è pronto per l'operazione successiva.

\_caricamento in \_ \_ modalità file DGV MCI \_

Restituito durante il caricamento del file.

\_salvataggio in \_ \_ modalità file DGV MCI \_

Restituito durante il salvataggio del file.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_ \_ completamento file di stato DGV \_ MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce la percentuale stimata. l'operazione di caricamento, salvataggio, acquisizione, taglia, copia, eliminazione, incolla o annullamento è stata progredita. (Le applicazioni possono usare questa operazione per fornire un indicatore visivo dello stato di avanzamento). Questo flag non è supportato da tutti i dispositivi video digitali.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_stato DGV \_ MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce **true** se la direzione del dispositivo è diretta o il dispositivo non viene riprodotto.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_ \_ \_ frequenza fotogrammi di stato DGV MCI \_
</dt> <dd>

Il membro **dwReturn** deve essere usato con il \_ valore \_ nominale dello stato DGV di MCI, il record di \_ \_ stato DGV MCI \_ \_ o entrambi. Quando viene usato con \_ \_ il record di stato DGV MCI \_ , viene restituita la frequenza dei fotogrammi corrente usata per la registrazione. Quando viene usato con \_ il record di stato DGV di MCI \_ \_ e \_ \_ il valore nominale dello stato DGV di MCI \_ , viene restituita la frequenza dei fotogrammi nominale associata al segnale video di input. Se usato con \_ lo stato DGV di MCI \_ \_ , viene restituita la frequenza dei fotogrammi nominale associata al file. In tutti i casi, le unità sono in frame al secondo moltiplicate per 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_gamma di \_ stato \_ DGV MCI
</dt> <dd>

Il membro **dwReturn** restituisce il valore gamma corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>\_ \_ HPAL stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il valore decimale ASCII per l'handle della tavolozza corrente. L'handle è contenuto nella parola di ordine inferiore del valore restituito.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_ \_ HWND stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il valore decimale ASCII per l'handle di finestra esplicito o predefinito corrente associato a questa istanza del driver di dispositivo. L'handle è contenuto nella parola di ordine inferiore del valore restituito.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_ \_ \_ colore chiave stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il valore corrente del colore della chiave.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_ \_ \_ indice chiave stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il valore di indice della chiave corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_ \_ monitoraggio stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce una costante che indica l'origine della presentazione corrente. Sono definite le costanti seguenti:

\_file di \_ monitoraggio \_ DGV MCI

Un file è l'origine.

\_ \_ input monitoraggio DGV \_ MCI

L'input è l'origine.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_metodo di \_ \_ monitoraggio stato DGV MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce una costante che indica il metodo utilizzato per il monitoraggio dell'input. Sono definite le costanti seguenti:

\_Metodo DGV \_ MCI \_ diretto

Monitoraggio diretto degli input.

\_post del \_ metodo \_ DGV di MCI

Monitoraggio post-input.

\_pre- \_ metodo \_ DGV MCI

Monitoraggio pre-input.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modalità di \_ \_ sospensione stato DGV MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce la \_ riproduzione in modalità MCI \_ se il dispositivo è stato sospeso durante la riproduzione e restituisce \_ \_ il record della modalità MCI se il dispositivo è stato sospeso durante la registrazione. Il comando restituisce MCIERR \_ \_ funzione non applicabile come un errore restituito se il dispositivo non è sospeso.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>\_ \_ SAMPLESPERSECOND stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero di campioni al secondo registrati.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>\_ \_ \_ ricerca \_ esatta stato DGV MCI
</dt> <dd>

Il membro **dwReturn** restituisce **true** o **false** che indica se è impostato o meno il formato Seek esatto. (Le applicazioni possono impostare questo formato usando il comando [MCI \_ set](mci-set.md) con il \_ flag DGV \_ set \_ Seek \_ exactly del MCI).

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_ \_ nitidezza stato DGV MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce il livello di nitidezza corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_ \_ dimensioni stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce la durata approssimativa della riproduzione dei dati compressi che l'area di lavoro riservata conterrà. Le unità di durata sono nel formato di ora corrente. Restituisce zero se non è disponibile spazio su disco riservato. Le dimensioni restituite sono approssimative poiché lo spazio su disco preciso per i dati compressi non può essere stimato, in generale, fino a quando i dati non sono stati compressi.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>\_SMPTE DGV \_ stato \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il codice ora SMPTE associato alla posizione corrente nell'area di lavoro.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_ \_ velocità stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce la velocità di riproduzione corrente.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>\_stato DGV di MCI \_ ancora in \_ \_ formato FileFormat
</dt> <dd>

Il membro **dwReturn** restituisce il formato di file corrente per il comando di [ \_ acquisizione MCI](mci-capture.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_ \_ tinta stato DGV MCI \_
</dt> <dd>

Il membro **dwReturn** restituisce il livello di tinta del video corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>\_ \_ Treble stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il livello di acuto audio corrente. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_stato DGV MCI non \_ \_ salvato
</dt> <dd>

Il membro **dwReturn** restituisce **true** se nell'area di lavoro sono presenti dati registrati che potrebbero andare perduti a seguito di un comando [MCI \_ Close](mci-close.md), [MCI \_ Load](mci-load.md), [MCI \_ record](mci-record.md), [MCI \_ Reserve](mci-reserve.md), [MCI \_ Cut](mci-cut.md), [MCI \_ Delete](mci-delete.md)o [MCI \_ paste](mci-paste.md) . Il membro restituisce **false** in caso contrario.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_video di \_ stato \_ DGV MCI
</dt> <dd>

Il membro **dwReturn** restituisce MCI \_ in se il video è abilitato o MCI \_ disattivato se è disabilitato.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_ \_ \_ record video stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce MCI \_ on o MCI \_ off, che riflette lo stato impostato dal \_ \_ flag di record MCI DGV sevideo \_ del comando [MCI \_ sevideo](mci-setvideo.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_ \_ \_ origine video stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce una costante che indica il tipo di origine video impostato dal \_ \_ flag di origine DGV sevideo MCI \_ del comando **MCI \_ sevideo** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_video di stato DGV di MCI-numero \_ \_ \_ src \_
</dt> <dd>

Il membro **dwReturn** restituisce il numero all'interno del tipo di origine di input video attualmente attivo.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_ \_ \_ flusso video stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce il numero corrente del flusso video.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_ \_ volume stato DGV \_ MCI
</dt> <dd>

Il membro **dwReturn** restituisce la media del volume agli altoparlanti sinistro e destro. Utilizzare \_ \_ lo stato DGV MCI \_ nominale con questo flag per ottenere il livello nominale.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>\_finestra di \_ stato DGV MCI \_ \_ visibile
</dt> <dd>

Il membro **dwReturn** restituisce **true** se la finestra non è nascosta.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_finestra di stato DGV di MCI ridotta a \_ \_ \_ icona
</dt> <dd>

Il membro **dwReturn** restituisce **true** se la finestra è ridotta a icona.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_finestra di \_ stato DGV MCI \_ \_ ingrandita
</dt> <dd>

Il membro **dwReturn** restituisce **true** se la finestra è ingrandita.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** restituisce **true**.

</dd> </dl>

Per i dispositivi digitali video, il parametro *lpStatus* punta a una [**struttura \_ DGV \_ stato \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .

I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **sequencer** . Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_ \_ DIVTYPE stato MCI \_ Seq
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei valori seguenti, che indica il tipo di divisione corrente di una sequenza:

-   PPQN per MCI \_ seq \_ div \_
-   MCI \_ seq \_ div \_ SMPTE \_ 24
-   MCI \_ seq \_ div \_ \_ 25
-   MCI \_ seq \_ div \_ \_ 30
-   MCI \_ seq \_ div \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_ \_ Master stato SEQ per MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul tipo di sincronizzazione utilizzato per l'operazione master.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_ \_ offset dello stato Seq di MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sull'offset SMPTE corrente di una sequenza.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_porta di \_ stato Seq seq \_
</dt> <dd>

Il membro **dwReturn** è impostato sull'identificatore del dispositivo MIDI per la porta corrente utilizzata dalla sequenza.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_ \_ stato dello slave Seq stato di MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul tipo di sincronizzazione usato per l'operazione subordinata.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>TEMPO di stato di MCI \_ seq \_ \_
</dt> <dd>

Il membro **dwReturn** è impostato sul tempo corrente di una sequenza MIDI in battute al minuto per i file PPQN o frame al secondo per i file SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .

</dd> </dl>

Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti. Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_record di \_ \_ assemblaggio stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se la modalità di assemblaggio è on; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_ \_ \_ monitoraggio audio stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che indica il tipo di monitoraggio audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_numero di \_ \_ monitor audio \_ stato \_ VCR MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero del tipo di monitoraggio audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_ \_ \_ record audio stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se l'audio viene registrato quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** . Se si specifica la \_ traccia MCI nel parametro *dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica questa richiesta.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_ \_ \_ origine audio stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che indica il tipo di origine audio corrente.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>codice \_ \_ \_ sorgente audio stato \_ VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero del tipo di origine audio attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_ \_ Clock stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul valore clock corrente, in incrementi di clock totali.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_ \_ \_ ID Clock stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su un numero che descrive in modo univoco il clock in uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_ \_ \_ formato contatore stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che descrive il formato del contatore corrente. Per ulteriori informazioni, vedere il \_ flag MCI set \_ time \_ Format del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_risoluzione del \_ contatore di stato VCR \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che descrive la risoluzione del contatore ed è uno dei valori seguenti:

-   \_ \_ \_ Frame di res del contatore VCR MCI \_ : il contatore ha la risoluzione dei frame.
-   \_ \_ Contatori del contatore VCR MCI \_ \_ : contatore con risoluzione dei secondi.
-   \_Valore del \_ contatore di stato VCR MCI \_ \_ : il membro **dwReturn** è impostato sul contatore corrente, nel formato del contatore corrente.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_ \_ \_ frequenza fotogrammi di stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sulla frequenza dei fotogrammi nativa corrente del dispositivo.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_ \_ Indice stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante, che descrive il contenuto corrente dello schermo sullo schermo, ed è uno dei seguenti:

-   \_ \_ contatore indice VCR \_ MCI
-   \_Data di \_ Indice MCI VCR \_
-   \_ora di \_ indicizzazione VCR MCI \_
-   \_ \_ codice temporale dell'indice MCI VCR \_

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ Indice stato VCR \_ MCI \_ in
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se lo schermo sullo schermo è acceso; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo di \_ supporto di stato VCR \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei seguenti elementi:

-   \_Supporti VCR \_ MCI \_ 8mm
-   \_ \_ Hi8 supporti VCR \_ MCI
-   \_VCR \_ dei supporti \_ VCR MCI
-   \_ \_ SVHS supporti VCR \_ MCI
-   \_supporto VCR \_ MCI \_ beta
-   \_ \_ EDBETA supporti VCR \_ MCI
-   \_ \_ altri supporti VCR \_ MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_ \_ numero stato VCR \_ MCI
</dt> <dd>

Il membro **dwNumber** è impostato sul numero di sintonizzatori logici quando si usa questo flag con il \_ flag del canale del \_ sintonizzatore di stato di MCI VCR \_ \_ .

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ numero \_ di \_ tracce audio del \_ VCR MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di tracce audio selezionabili in modo indipendente.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ stato del videoregistratore \_ MCI \_ numero \_ di \_ tracce video
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di tracce video che sono selezionabili in modo indipendente.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_timeout di \_ \_ sospensione stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sulla durata massima, in millisecondi, di un comando pause. Il valore restituito zero indica che non si verificherà alcun timeout.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_ \_ \_ formato riproduzione stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei seguenti elementi:

-   \_EP del \_ formato \_ VCR MCI
-   \_ \_ LP formato VCR \_ MCI
-   \_ \_ altro formato VCR \_ MCI
-   \_ \_ SP formato VCR \_ MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_durata del \_ \_ postroll stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sulla lunghezza del nastro che verrà riprodotto dopo il punto in cui è stato arrestato, nel formato dell'ora corrente. Questa operazione è necessaria per frenare il trasporto del nastro VCR da un comando stop o pause.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>acceso \_ \_ stato VCR \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se l'alimentazione è attiva; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_ \_ \_ durata preregistrazione stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla lunghezza del nastro che verrà riprodotto prima del punto in cui è stato avviato, nel formato dell'ora corrente. Questa operazione è necessaria per stabilizzare l'output del videoregistratore.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_ \_ formato record di stato VCR \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei seguenti elementi:

-   \_EP del \_ formato \_ VCR MCI
-   \_ \_ LP formato VCR \_ MCI
-   \_ \_ altro formato VCR \_ MCI
-   \_ \_ SP formato VCR \_ MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_ \_ velocità stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla velocità corrente. Per ulteriori informazioni, vedere il \_ flag MCI VCR \_ set \_ Speed del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_ \_ \_ modalità ora stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su uno dei seguenti elementi:

-   \_ \_ contatore tempo VCR \_ MCI
-   \_ \_ rilevamento ora VCR \_ MCI
-   \_ \_ timecode ora VCR \_ MCI

Per ulteriori informazioni, vedere il \_ flag MCI VCR \_ set \_ time \_ mode del comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_ \_ \_ tipo ora stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che descrive il tipo di ora corrente in uso (usato da [Play](play.md), [record](record.md), [Seek](seek.md)e così via) ed è uno dei seguenti:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ contatore tempo VCR \_ MCI
</dt> <dd>

Il contatore è in uso.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_ \_ timecode ora VCR \_ MCI
</dt> <dd>

Il codice temporale è in uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_ \_ timecode stato VCR \_ MCI \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il codice temporale è presente nella posizione corrente nel contenuto; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_record del \_ timecode di stato VCR \_ MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il codice temporale viene registrato quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo di \_ \_ timecode stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato su una costante, che descrive il tipo di codice temporale supportato direttamente dal dispositivo ed è uno dei seguenti:

-   \_Tipo di timecode VCR del videoregistratore MCI \_ \_ \_ : questo dispositivo non usa un timecode.
-   \_ \_ Tipo di codice temporale VCR MCI \_ \_ : questo dispositivo usa un timecode non specificato.
-   MCI \_ VCR \_ tipo di codice \_ \_ SMPTE: questo dispositivo usa il timecode SMPTE.
-   MCI \_ VCR \_ \_ Type timecode \_ \_ Drop: questo dispositivo usa il timecode di rilascio SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_ \_ \_ canale Tuner stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di canale corrente. Se si specifica il \_ \_ numero di stato VCR MCI \_ nel parametro *dwFlags* di questo comando, **dwNumber** contiene il numero di Tuner logico a cui si applica questo comando.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_ \_ \_ monitoraggio video stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che indica il tipo di monitoraggio video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_numero di \_ \_ monitor video \_ stato \_ VCR MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul numero del tipo di monitor video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ \_ record video stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se viene registrato il video quando viene specificato il comando record successivo. in caso contrario, viene impostato su **false** . Se si specifica la \_ traccia MCI nel parametro *dwFlags* di questo comando, **dwTrack** contiene la traccia a cui si applica questa richiesta.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_ \_ \_ origine video stato VCR \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su una costante che indica il tipo di origine video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_numero di \_ \_ origine video \_ di stato VCR MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul numero del tipo di origine video attualmente selezionato.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_ \_ \_ scrittura \_ protetta stato VCR MCI
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto è protetto da scrittura; in caso contrario, viene impostato su **false** .

</dd> </dl>

Per i dispositivi VCR, il parametro *lpStatus* punta a una struttura [**\_ \_ \_ parametri di stato VCR di MCI**](mci-vcr-status-parms.md) .

\_Se si utilizza il flag di lunghezza stato MCI \_ per determinare la lunghezza del supporto, vengono restituiti sempre 2 ore per i dispositivi VCR, a meno che la lunghezza non sia stata modificata in modo esplicito utilizzando il comando [MCI \_ set](mci-set.md) .

I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **overlay** . Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_ \_ HWND stato OVLY \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sull'handle della finestra associata al dispositivo di sovrimpressione video.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_ \_ estensione stato OVLY \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se l'estensione è abilitata; in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .

</dd> </dl>

I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **videodisco** . Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_supporto di stato MCI \_ \_ presente
</dt> <dd>

Il membro **dwReturn** è impostato su **true** se il supporto viene inserito nel dispositivo. in caso contrario, viene impostato su **false** .

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modalità stato \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sulla modalità corrente del dispositivo. I dispositivi videodisco possono restituire la \_ \_ costante del Parco della modalità di MCI VD \_ , oltre alle costanti che qualsiasi dispositivo può restituire, come documentato con il parametro *dwFlags* .

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_dimensioni del \_ disco di stato MCI VD \_ \_
</dt> <dd>

Il membro **dwReturn** è impostato sulla dimensione del disco caricato in pollici (8 o 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>stato di MCI \_ VD \_ \_
</dt> <dd>

Il membro **dwReturn** è impostato su **true** in caso di riproduzione. in caso contrario, viene impostato su **false** .

Il dispositivo videodisco MCI non supporta questo flag.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo di \_ supporto di stato MCI VD \_ \_
</dt> <dd>

Il membro **dwReturn** è impostato sul tipo di supporto del supporto inserito. È possibile restituire i tipi di supporto seguenti:

MCI \_ VD \_ media \_ CAV

MCI \_ VD \_ media \_ CLV

\_ \_ altri supporti MCI \_ VD

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ lato stato di MCI VD \_
</dt> <dd>

Il membro **dwReturn** è impostato su 1 o 2 per indicare quale lato del disco è caricato. Questo flag non è supportato da tutti i dispositivi videodisco.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>\_ \_ velocità stato MCI \_ VD
</dt> <dd>

Il membro **dwReturn** è impostato sulla velocità di riproduzione in frame al secondo. MCIPIONR. Il driver di dispositivo DRV restituisce MCIERR \_ funzione non supportata \_ .

</dd> </dl>

I flag aggiuntivi seguenti vengono utilizzati con il tipo di dispositivo **WaveAudio** . Queste costanti vengono usate nel membro **dwItem** della struttura a cui punta il parametro *lpStatus* quando \_ \_ si specifica l'elemento di stato MCI per il parametro *dwFlags* .

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul tag di formato corrente usato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul dispositivo di input wave usato per la registrazione. Se non è in uso alcun dispositivo e non è stato impostato in modo esplicito alcun dispositivo, il risultato dell'errore è MCIERR \_ Wave \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI
</dt> <dd>

Il membro **dwReturn** è impostato sul dispositivo di output wave usato per la riproduzione. Se non è in uso alcun dispositivo e non è stato impostato in modo esplicito alcun dispositivo, il risultato dell'errore è MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>\_stato dell'onda MCI \_ \_ AVGBYTESPERSEC
</dt> <dd>

Il membro **dwReturn** è impostato sui byte correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_stato dell'onda MCI \_ \_ BitsPerSample
</dt> <dd>

Il membro **dwReturn** è impostato sui bit correnti per campione usato per la riproduzione, la registrazione e il salvataggio dei dati in formato PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>\_stato dell'onda MCI \_ \_ BLOCKALIGN
</dt> <dd>

Il membro **dwReturn** è impostato sull'allineamento a blocchi corrente utilizzato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canali di \_ stato dell'onda MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul numero di canali corrente usato per la riproduzione, la registrazione e il salvataggio.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_livello di \_ stato dell'onda MCI \_
</dt> <dd>

Il membro **dwReturn** è impostato sul livello di riproduzione o record corrente dei dati in formato PCM. Il valore viene restituito come valore a 8 o a 16 bit, a seconda delle dimensioni del campione utilizzate. Il livello di canale destro o mono viene restituito nella parola di ordine inferiore. Il livello di canale sinistro viene restituito nella parola più ordinata.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>\_stato dell'onda MCI \_ \_ SAMPLESPERSEC
</dt> <dd>

Il membro **dwReturn** è impostato sugli esempi correnti al secondo usati per la riproduzione, la registrazione e il salvataggio.

</dd> </dl>

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
</dt> <dt>

[\_taglia MCI](mci-cut.md)
</dt> <dt>

[eliminazione di MCI \_](mci-delete.md)
</dt> <dt>

[\_Incolla MCI](mci-paste.md)
</dt> <dt>

[\_riserva MCI](mci-reserve.md)
</dt> <dt>

[SET di MCI \_](mci-set.md)
</dt> <dt>

[Play](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[cercare](seek.md)
</dt> </dl>

 

