---
title: comando set
description: Il comando set stabilisce le impostazioni di controllo per il dispositivo. Cd audio, digital-video, sequencer MIDI, VCR, videodisc, sovrapposizione video e dispositivi audio waveform riconoscono questo comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- comando set Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc9263ace043f938c8d793b2ceef5ad70264bb1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479487"
---
# <a name="set-command"></a>comando set

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo riconosce come una parola di esclusione.  Questa formulazione viene usata perché è attualmente la formulazione usata all'interno dei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo che sia allineato.


Il comando set stabilisce le impostazioni di controllo per il dispositivo. Cd audio, digital-video, sequencer MIDI, VCR, videodisc, sovrapposizione video e dispositivi audio waveform riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Flag per stabilire le impostazioni di controllo. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando set** e i flag usati da ogni tipo.




| Tipo di dispositivo | Flag di comando | 
|-------------|---------------|
| cdaudio | <ul><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>porta chiusa</li><li>porta aperta</li><li>millisecondi di formato dell'ora</li><li>formato dell'ora msf</li><li>formato ora tmsf</li></ul> | 
| digitalvideo | <ul><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>porta chiusa</li><li>porta aperta</li><li>formato di <em>file</em></li><li>cercare esattamente in</li><li>cercare esattamente off</li><li>fattore di <em>velocità</em></li><li>formato di file <em>still</em></li><li>fotogrammi in formato ora</li><li>millisecondi di formato dell'ora</li><li>video disattivato</li><li>video su</li></ul> | 
| overlay | <ul><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>porta chiusa</li><li>porta aperta</li><li>video disattivato</li><li>video su</li></ul> | 
| sequencer | <ul><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>porta chiusa</li><li>porta aperta</li><li>MASTER MIDI</li><li>master none</li><li>master SMPTE</li><li>tempo <em></em> di offset</li><li>mapper di porte</li><li>porta nessuna</li><li>porta <em>port_number</em></li><li>file slave</li><li>SLAVE MIDI</li><li>slave none</li><li>slave SMPTE</li><li>tempo <em>tempo_value</em></li><li>millisecondi di formato dell'ora</li><li>formato ora SMPTE <em>fps</em></li><li>formato ora SMPTE 30 drop</li><li>puntatore del brano in formato ora</li></ul> | 
| <strong>Vcr</strong> | <ul><li>assemblare record in</li><li>assemblare record off</li><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>ora <em>dell'orologio</em></li><li>formato contatore</li><li>valore <em>del contatore</em></li><li>porta chiusa</li><li>porta aperta</li><li>contatore dell'indice</li><li>data dell'indice</li><li>ora dell'indice</li><li>ora dell'indice</li><li>durata <em>codelength</em></li><li>timeout <em>di sospensione</em></li><li>Durata post-registrazione -</li><li><em>duration</em></li><li>accensione</li><li>power off</li><li>durata della <em>pre-registrazione</em></li><li>formato di record SP</li><li>formato di record LP</li><li>formato di record EP</li><li>fattore di <em>velocità</em></li><li>fotogrammi in formato ora</li><li>formato ora hms</li><li>millisecondi di formato dell'ora</li><li>formato dell'ora msf</li><li>formato ora SMPTE <em>fps</em></li><li>formato ora SMPTE 30 drop</li><li>formato ora tmsf</li><li>contatore della modalità tempo</li><li>rilevamento della modalità temporale</li><li>time mode timecode</li><li>tracking plus</li><li>rilevamento meno</li><li>reimpostazione del rilevamento</li></ul> | 
| videodisc | <ul><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>porta chiusa</li><li>porta aperta</li><li>fotogrammi in formato ora</li><li>formato ora hms</li><li>millisecondi di formato dell'ora</li><li>traccia del formato dell'ora</li><li>video disattivato</li><li>video su</li></ul> | 
| Waveaudio | <ul><li>intero di <em>allineamento</em></li><li>qualsiasi input</li><li>qualsiasi output</li><li>audio tutto disattivato</li><li>audio all on</li><li>audio disattivato</li><li>audio lasciato in</li><li>audio subito spento</li><li>audio a destra su</li><li>bitspersample <em>bit_count</em></li><li>bytepersec <em>byte_rate</em></li><li>canali <em>channel_count</em></li><li>porta chiusa</li><li>porta aperta</li><li>tag di formato pcm</li><li>tag di <em>formato</em></li><li>input <em>integer</em></li><li>output <em>integer</em></li><li>samplespersec <em>integer</em></li><li>byte in formato ora</li><li>millisecondi di formato dell'ora</li><li>esempi di formato ora</li></ul> | 




 

Nella tabella seguente sono elencati i flag che è possibile specificare nel **parametro lpszSetting** e i relativi significati.




| valore | Significato | 
|-------|---------|
| intero di <em>allineamento</em> | Imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati passati al dispositivo waveform-audio. Il file viene salvato in questo formato. | 
| qualsiasi input | Usare qualsiasi input che supporti il formato corrente durante la registrazione. Si tratta dell'impostazione predefinita. | 
| qualsiasi output | Usare qualsiasi output che supporti il formato corrente durante la riproduzione. Questo è il valore predefinito. | 
| assemblare record in <br /> assemblare record off <br /> | In modalità di assemblaggio, tutte le tracce vengono registrate come definito dal dispositivo. La maggior parte dei videoregistratori è in modalità di assemblaggio per impostazione predefinita. | 
| audio tutto disattivato <br /> audio all on <br /> | Disabilita o abilita l'output audio. I dispositivi di sovrapposizione video, il sequencer MCISEQ e il dispositivo audio con forma d'onda MCIWAVE non supportano questo flag. | 
| audio disattivato <br /> audio lasciato in <br /> audio subito spento <br /> audio a destra su <br /> | Disabilita o abilita l'output a sinistra o al canale audio destro. I dispositivi di sovrapposizione video, il sequencer MCISEQ e il dispositivo audio con forma d'onda MCIWAVE non supportano questo flag. | 
| bitspersample <em>bit_count</em> | Imposta il numero di bit per campione PCM (Pulse Code Modulation) riprodotto o registrato. Il file viene salvato in questo formato. | 
| bytepersec <em>byte_rate</em> | Imposta il numero medio di byte riprodotti o registrati al secondo. Il file viene salvato in questo formato. | 
| Canali <em>channel_count</em> | Imposta i canali per la riproduzione e la registrazione. Il file viene salvato in questo formato. | 
| clock <em>time</em> | Imposta l'ora dell'orologio esterno su <em>time.</em> Il formato viene specificato come long unsigned integer. | 
| formato contatore | Impostare il formato dell'ora per il contatore, come restituito <a href="status.md">dallo stato</a> "counter". Per informazioni sui tipi applicabili, vedere il <strong>comando set</strong> "time format". | 
| valore <em>contatore</em> | Imposta il contatore vcr sul valore specificato. Il valore deve essere specificato nel formato del contatore corrente. Per altre informazioni, vedere il <strong>comando set</strong> "counter format". | 
| door closed | Ritira la barra e chiude la porta, se possibile. Per le videoregistratori, carica automaticamente il nastro. | 
| door open | Apre la porta e, se possibile, espulse l'area di notifica o il nastro. | 
| formato di <em>file</em> | Specifica un formato di file utilizzato per i <a href="save.md">comandi di salvataggio</a> <a href="capture.md">o</a> acquisizione. Se omesso, il valore predefinito potrebbe essere un formato definito dal driver di dispositivo. Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, vengono modificati i valori predefiniti per il formato di file. Vengono definiti i formati di file seguenti:<ul><li>avi: specifica il formato AVI.</li><li>avss: specifica il formato AVSS.</li><li>dib: specifica il formato DIB.</li><li>jfif: specifica il formato JFIF.</li><li>jpeg: specifica il formato JPEG.</li><li>mpeg: specifica il formato MPEG.</li><li>rdib: specifica il formato DIB RLE.</li><li>rjpeg: specifica il formato RJPEG.</li></ul> | 
| format tag pcm | Imposta il tipo di formato su PCM per la riproduzione e la registrazione. Il file viene salvato in questo formato. | 
| tag di <em>formato</em> | Imposta il tipo di formato per la riproduzione e la registrazione. Il file viene salvato in questo formato. | 
| codice temporale dell'indice <br /> contatore dell'indice <br /> index date <br /> ora dell'indice <br /> | Imposta la schermata di visualizzazione corrente nel videoregistratore. | 
| input <em>integer</em> | Imposta il canale audio utilizzato come input. | 
| durata <em></em> | Imposta la lunghezza specificata dall'utente del nastro nel videoregistratore. Questa lunghezza viene restituita dal comando <a href="status.md">di</a> stato "length" e viene fornita per la compatibilità con le applicazioni che richiedono che questo comando restituirà una lunghezza valida. | 
| master midi | Imposta il sequencer MIDI come origine di sincronizzazione. I dati di sincronizzazione vengono inviati in formato MIDI. Il sequencer MCISEQ non supporta questo flag. | 
| master none | Impedisce al sequencer MIDI di inviare dati di sincronizzazione. Il sequencer MCISEQ non supporta questo flag. | 
| master smpte | Imposta il sequencer MIDI come origine di sincronizzazione. I dati di sincronizzazione vengono inviati in formato SMPTE (Society of Motion Picture and Engineers). Il sequencer MCISEQ non supporta questo flag. | 
| offset <em>time</em> | Imposta l'ora di <em>offset</em>SMPTE. L'offset è l'ora di inizio di una sequenza basata su SMPTE. <em>L'ora</em> è espressa come <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è frame. | 
| output <em>integer</em> | Imposta il canale audio usato come output. | 
| timeout <em>di sospensione</em> | Imposta la durata massima, in millisecondi, di un <a href="pause.md">comando di</a> sospensione. Un <em>valore</em> di timeout pari a zero indica che non si verificherà alcun timeout. | 
| durata postroll <em></em> | Imposta la lunghezza, nel formato di ora corrente, necessaria per bloccare il trasporto vcr quando viene eseguito un <strong>comando</strong> <a href="stop.md">di</a> arresto o sospensione. | 
| mapper di porte | Imposta il mapper MIDI come porta che riceve i messaggi MIDI. Questo comando ha esito negativo se il mapper MIDI o una porta richiesta viene usata da un'altra applicazione. | 
| porta none | Disabilita l'invio di messaggi MIDI. Questo comando chiude anche una porta MIDI. | 
| Porta <em>port_number</em> | Imposta la porta MIDI che riceve i messaggi MIDI. Questo comando ha esito negativo se la porta che si sta tentando di aprire viene usata da un'altra applicazione. | 
| accensione <br /> power off <br /> | Imposta l'alimentazione del dispositivo su on o off. | 
| durata della <em>pre-registrazione</em> | Imposta la lunghezza, nel formato di ora corrente, necessaria per stabilizzare l'output del videoregistratore. | 
| formato record SP <br /> formato record LP <br /> Formato record EP <br /> | Imposta la modalità di registrazione per il videoregistratore su SP per la riproduzione standard, EP per la riproduzione estesa o LP per la riproduzione prolungata. Questi valori non sono destinati a essere specifici del disco rigido virtuale. Vengono mappati a tre modalità appropriate con altri formati di nastro. Ad esempio, SP esegue il mapping alla registrazione più veloce e di massima qualità. | 
| samplespersec <em>integer</em> | Imposta la frequenza di campionamento per la riproduzione e la registrazione. Il file viene salvato in questo formato. | 
| seek exactly on<br /> seek exactly off <br /> | Seleziona una delle due modalità di ricerca. Con "seek exactly on", seek si sposterà sempre nel frame specificato. Con "seek exactly off", seek si sposterà nel fotogramma chiave più vicino prima del fotogramma specificato. | 
| file slave | Imposta il sequencer MIDI per usare i dati del file come origine di sincronizzazione. Si tratta dell'impostazione predefinita. | 
| slave midi | Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato MIDI. Il sequencer MCISEQ non supporta questo flag. | 
| slave none | Imposta il sequencer MIDI per ignorare la sincronizzazione | 
| slave smpte | Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato SMPTE. Il sequencer MCISEQ non supporta questo flag. | 
| fattore di velocità | Imposta la velocità relativa della riproduzione di video e audio dall'area di lavoro. Il fattore è il rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata, dove la frequenza dei fotogrammi nominali è designata come 1000. Una velocità di 500 è metà velocità normale, 2000 è il doppio della velocità normale e così via. Impostando la velocità su zero, il video viene riprodotto il più velocemente possibile senza eliminare fotogrammi e senza audio. | 
| formato di file <em>still</em> | Specifica il formato di file usato per i comandi di acquisizione. | 
| tempo tempo_value | Imposta il tempo della sequenza in base al formato di ora corrente. Per un file basato su PPQN, il tempo_value viene interpretato come picchi al minuto. Per un file basato su SMPTE, il tempo_value viene interpretato come frame al secondo. | 
| byte di formato ora | In un formato di file PCM, imposta il formato dell'ora su byte. Tutte le informazioni sulla posizione vengono specificate come byte dopo questo comando. | 
| frame di formato ora | Imposta il formato dell'ora su frame. Tutti i comandi che usano valori di posizione presupporranno frame. Quando il dispositivo viene aperto, la modalità predefinita è frame. Supportato da videodiscs con il formato CAV. | 
| formato ora hms | Imposta il formato dell'ora su ore, minuti e secondi. Tutti i comandi che usano valori di posizione presupporranno HMS. HMS è il formato predefinito per videodiscs CLV. Specificare un valore HMS come hh:mm:ss, dove hh è ore, mm è minuti e ss è secondi. È possibile omettere un campo se questo e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono tutti modi validi per esprimere 3 ore. <br /> | 
| formato dell'ora millisecondi | Imposta il formato dell'ora su millisecondi. Tutti i comandi che usano valori di posizione presuppongono millisecondi. È possibile abbreviare i millisecondi come "ms". Per i dispositivi Sequencer, il file di sequenza imposta il formato predefinito su PPQN o SMPTE. I dispositivi con sovrimpressione video non supportano questo flag.<br /> | 
| formato ora msf | Imposta il formato dell'ora su minuti, secondi e fotogrammi. Tutti i comandi che usano valori di posizione presupporranno MSF (il formato predefinito per l'audio CD). Specificare un valore MSF come mm:ss:ff, dove mm è minuti, ss è secondi e ff è frame. È possibile omettere un campo se questo e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono modi validi per esprimere 3 minuti.<br /> I campi MSF hanno i valori massimi seguenti:<br /><ul><li>Minuti 99</li><li>Secondi 59</li><li>Frame 74</li></ul> | 
| esempi di formato ora | Imposta il formato dell'ora su samples. Tutte le informazioni sulla posizione vengono specificate come esempi dopo questo comando. | 
| time format smpte 24<br /> time format smpte 25<br /> time format smpte 30<br /> | Imposta il formato dell'ora su una frequenza dei fotogrammi SMPTE. Per le videoregistratori, imposta il formato dell'ora su hh:mm:ss:ff, dove i valori validi sono da 00:00:00:00 a 23:59:59:xx e xx è minore di uno dei fotogrammi al secondo come specificato dal numero 24, 25 o 30 come specificato nel flag . In caso di input, i due punti (:) sono necessari per separare i componenti. Le unità meno significative possono essere omesse se sono 00; Ad esempio, 02:00 corrisponde a 02:00:00:00. Tutti i comandi che usano valori di posizione presupporranno il formato SMPTE.<br /> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br /> | 
| time format smpte 30 drop | Imposta il formato dell'ora su SMPTE 30 drop frame rate. Per le videoregistratori, come SMPTE 30, ad eccezione del fatto che determinate posizioni del timecode vengono eliminate dal formato in modo che le posizioni del timecode registrate per ogni fotogramma (alla frequenza dei fotogrammi NTSC di 29,97 fps) corrispondano in tempo reale (a 30 fps). Le posizioni dei timecode eliminate sono le seguenti: due ogni minuto, al minuto, per le prime nove di ogni dieci minuti di contenuto registrato. Ad esempio, alle 01:04:59:29 la posizione successiva del timecode sarà 01:05:00:02, non 01:05:00:00. Tutti i comandi che usano valori di posizione presupporranno il formato SMPTE.<br /> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br /> | 
| puntatore del brano formato ora | Imposta il formato dell'ora sul puntatore del brano (sedicesima nota). Tutti i comandi che usano valori di posizione presupporranno unità puntatore del brano. Questo flag è valido solo per una sequenza di tipo di divisione PPQN. | 
| time format tmsf | Imposta il formato dell'ora su tracce, minuti, secondi e fotogrammi. Tutti i comandi che usano valori di posizione presupporranno TMSF. Specificare un valore TMSF come tt:mm:ss:ff, dove tt è traccia, mm è minuti, ss è secondi e ff è frame. È possibile omettere un campo se questo e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0, 3:0:0 e 3:0:0:0 sono tutti modi validi per esprimere la traccia 3. <br /> I campi TMSF hanno i valori massimi seguenti:<br /><ul><li>Tracce 99</li><li>Minuti 90</li><li>Secondi 59</li><li>Frame 74</li></ul> | 
| time format track | Imposta il formato di posizione su tracks. Tutti i comandi che usano valori di posizione presupporranno tracce. | 
| contatore della modalità tempo | Imposta la modalità di informazioni sulla posizione per l'utilizzo dei contatori vcr. | 
| rilevamento della modalità ora | Imposta la modalità di informazioni sulla posizione in base al rilevamento delle informazioni sul timecode sul nastro. Se vengono rilevate informazioni sul timecode, il tipo di ora viene impostato su "timecode"; In caso contrario, il tipo di ora è impostato su "counter". "Detect" è una modalità speciale. Ogni volta che il driver viene aperto, viene inserito un nuovo nastro o viene eseguito il comando "time mode", il driver controlla la modalità ora corrente disponibile sul nastro e imposta "time type" su "timecode" o "counter". Una volta impostato il "tipo di ora", il driver non lo modifica fino a quando non si verifica di nuovo una delle condizioni precedenti.<br /> | 
| time mode timecode | Imposta la modalità di informazioni sulla posizione per l'utilizzo delle informazioni sul "timecode" sul nastro. | 
| tracking plus <br /> rilevamento meno <br /> reimpostazione del rilevamento <br /> | Regola la velocità del trasporto di videotape in incrementi fine. Usare i flag di "rilevamento" quando si ottiene un'immagine rumorosa da un videoregistratore. "Tracking plus" aumenta la velocità di trasporto. Il "rilevamento meno" riduce la velocità di trasporto. "Tracking Reset" restituisce la regolazione del rilevamento su zero. | 
| video off | Disabilita l'output video. | 
| video on | Abilita l'output video. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio waveform. Queste proprietà descrivono il modo in cui i dati sono strutturati all'interno del file e non possono essere modificati una volta avviata la registrazione. Nell'elenco seguente vengono identificate queste proprietà:

-   allineamento
-   bitspersample
-   bytespersec
-   channels
-   tag format
-   esempipersec

## <a name="examples"></a>Esempio

Il comando seguente imposta il formato dell'ora su millisecondi e il formato audio della forma d'onda su 8 bit, mono, 11 kHz.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[Catturare](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

