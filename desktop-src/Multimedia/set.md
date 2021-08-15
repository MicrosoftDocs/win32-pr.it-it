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
ms.openlocfilehash: 75f407a1e360cfbd6407f7ada29192addece7f7a968a2437326dc091fe0d9522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371013"
---
# <a name="set-command"></a>comando set

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo riconosce come parola di esclusione.  Questa formulazione viene usata perché è attualmente la formulazione usata all'interno dei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo che sia allineato.


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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di dispositivo</th>
<th>Flag di comando</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio lasciato in</li>
<li>audio subito spento</li>
<li>audio a destra su</li>
<li>porta chiusa</li>
<li>porta aperta</li>
<li>millisecondi di formato dell'ora</li>
<li>formato dell'ora msf</li>
<li>formato ora tmsf</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio lasciato in</li>
<li>audio subito spento</li>
<li>audio a destra su</li>
<li>porta chiusa</li>
<li>porta aperta</li>
<li>formato di <em>file</em></li>
<li>cercare esattamente su</li>
<li>cercare esattamente off</li>
<li>fattore di <em>velocità</em></li>
<li>formato di file <em>still</em></li>
<li>fotogrammi in formato ora</li>
<li>millisecondi di formato dell'ora</li>
<li>video disattivato</li>
<li>video su</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio lasciato in</li>
<li>audio subito spento</li>
<li>audio a destra su</li>
<li>porta chiusa</li>
<li>porta aperta</li>
<li>video disattivato</li>
<li>video su</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio lasciato in</li>
<li>audio subito spento</li>
<li>audio a destra su</li>
<li>porta chiusa</li>
<li>porta aperta</li>
<li>MASTER MIDI</li>
<li>master none</li>
<li>master SMPTE</li>
<li>tempo <em></em> di offset</li>
<li>mapper di porte</li>
<li>porta nessuna</li>
<li>porta <em>port_number</em></li>
<li>file slave</li>
<li>SLAVE MIDI</li>
<li>slave none</li>
<li>slave SMPTE</li>
<li>tempo <em>tempo_value</em></li>
<li>millisecondi di formato dell'ora</li>
<li>formato ora SMPTE <em>fps</em></li>
<li>formato ora SMPTE 30 drop</li>
<li>puntatore del brano in formato ora</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Vcr</strong></td>
<td><ul>
<li>assemblare record in</li>
<li>assemblare record off</li>
<li>audio tutto disattivato</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio lasciato in</li>
<li>audio subito spento</li>
<li>audio a destra su</li>
<li>ora <em>dell'orologio</em></li>
<li>formato contatore</li>
<li>valore <em>contatore</em></li>
<li>door closed</li>
<li>door open</li>
<li>contatore dell'indice</li>
<li>index date</li>
<li>ora dell'indice</li>
<li>ora dell'indice</li>
<li>codelength <em>duration</em></li>
<li>timeout <em>di sospensione</em></li>
<li>Postroll duration (Durata postroll) -</li>
<li><em>duration</em></li>
<li>accensione</li>
<li>power off</li>
<li>durata della <em>pre-registrazione</em></li>
<li>formato record SP</li>
<li>formato record LP</li>
<li>Formato record EP</li>
<li>fattore di <em>velocità</em></li>
<li>frame di formato ora</li>
<li>formato ora hms</li>
<li>formato dell'ora millisecondi</li>
<li>formato ora msf</li>
<li>formato ora SMPTE <em>fps</em></li>
<li>time format SMPTE 30 drop</li>
<li>time format tmsf</li>
<li>contatore della modalità tempo</li>
<li>rilevamento della modalità ora</li>
<li>time mode timecode</li>
<li>tracking plus</li>
<li>rilevamento meno</li>
<li>reimpostazione del rilevamento</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>audio all off</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio left on</li>
<li>audio right off</li>
<li>audio a destra su</li>
<li>door closed</li>
<li>door open</li>
<li>frame di formato ora</li>
<li>formato ora hms</li>
<li>formato dell'ora millisecondi</li>
<li>time format track</li>
<li>video off</li>
<li>video on</li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td><ul>
<li>alignment <em>integer</em></li>
<li>qualsiasi input</li>
<li>qualsiasi output</li>
<li>audio all off</li>
<li>audio all on</li>
<li>audio disattivato</li>
<li>audio left on</li>
<li>audio right off</li>
<li>audio a destra su</li>
<li>bitspersample <em>bit_count</em></li>
<li>bytepersec <em>byte_rate</em></li>
<li>Canali <em>channel_count</em></li>
<li>door closed</li>
<li>door open</li>
<li>format tag pcm</li>
<li>tag di <em>formato</em></li>
<li>input <em>integer</em></li>
<li>output <em>integer</em></li>
<li>samplespersec <em>integer</em></li>
<li>byte di formato ora</li>
<li>formato dell'ora millisecondi</li>
<li>esempi di formato ora</li>
</ul></td>
</tr>
</tbody>
</table>



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszSetting** e i relativi significati.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>alignment <em>integer</em></td>
<td>Imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati passati al dispositivo audio waveform. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td>qualsiasi input</td>
<td>Usare qualsiasi input che supporti il formato corrente durante la registrazione. Si tratta dell'impostazione predefinita.</td>
</tr>
<tr class="odd">
<td>qualsiasi output</td>
<td>Usare qualsiasi output che supporti il formato corrente durante la riproduzione. Questo è il valore predefinito.</td>
</tr>
<tr class="even">
<td>assemble record on <br/> assemble record off <br/></td>
<td>In modalità di assemblaggio, tutte le tracce vengono registrate come definito dal dispositivo. La maggior parte delle vcr è in modalità assemble per impostazione predefinita.</td>
</tr>
<tr class="odd">
<td>audio all off <br/> audio all on <br/></td>
<td>Disabilita o abilita l'output audio. I dispositivi di sovrapposizione video, il sequencer MCISEQ e il dispositivo audio waveform MCIWAVE non supportano questo flag.</td>
</tr>
<tr class="even">
<td>audio disattivato <br/> audio left on <br/> audio right off <br/> audio a destra su <br/></td>
<td>Disabilita o abilita l'output sul canale audio sinistro o destro. I dispositivi di sovrapposizione video, il sequencer MCISEQ e il dispositivo audio waveform MCIWAVE non supportano questo flag.</td>
</tr>
<tr class="odd">
<td>bitspersample <em>bit_count</em></td>
<td>Imposta il numero di bit per campione PCM (Pulse Code Modulation) riprodotto o registrato. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td>bytepersec <em>byte_rate</em></td>
<td>Imposta il numero medio di byte riprodotti o registrati al secondo. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td>Canali <em>channel_count</em></td>
<td>Imposta i canali per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td>clock <em>time</em></td>
<td>Imposta l'ora dell'orologio esterno su <em>time.</em> Il formato viene specificato come long unsigned integer.</td>
</tr>
<tr class="odd">
<td>formato contatore</td>
<td>Impostare il formato dell'ora per il contatore, come restituito dal <a href="status.md">contatore di</a> &quot; stato &quot; . Per informazioni sui tipi applicabili, vedere il <strong>comando set</strong> &quot; time &quot; format.</td>
</tr>
<tr class="even">
<td>valore <em>contatore</em></td>
<td>Imposta il contatore vcr sul valore specificato. Il valore deve essere specificato nel formato del contatore corrente. Per altre informazioni, vedere il <strong>comando set</strong> &quot; counter &quot; format.</td>
</tr>
<tr class="odd">
<td>door closed</td>
<td>Ritira la barra e chiude la porta, se possibile. Per le videoregistratori, carica automaticamente il nastro.</td>
</tr>
<tr class="even">
<td>door open</td>
<td>Apre la porta e, se possibile, espulse l'area di notifica o il nastro.</td>
</tr>
<tr class="odd">
<td>formato di <em>file</em></td>
<td>Specifica un formato di file utilizzato per i <a href="save.md">comandi di salvataggio</a> <a href="capture.md">o</a> acquisizione. Se omesso, il valore predefinito potrebbe essere un formato definito dal driver di dispositivo. Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, vengono modificati i valori predefiniti per il formato di file. Vengono definiti i formati di file seguenti:
<ul>
<li>avi: specifica il formato AVI.</li>
<li>avss: specifica il formato AVSS.</li>
<li>dib: specifica il formato DIB.</li>
<li>jfif: specifica il formato JFIF.</li>
<li>jpeg: specifica il formato JPEG.</li>
<li>mpeg: specifica il formato MPEG.</li>
<li>rdib: specifica il formato DIB RLE.</li>
<li>rjpeg: specifica il formato RJPEG.</li>
</ul></td>
</tr>
<tr class="even">
<td>format tag pcm</td>
<td>Imposta il tipo di formato su PCM per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td>tag di <em>formato</em></td>
<td>Imposta il tipo di formato per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td>codice temporale dell'indice <br/> contatore dell'indice <br/> index date <br/> ora dell'indice <br/></td>
<td>Imposta la schermata di visualizzazione corrente nel videoregistratore.</td>
</tr>
<tr class="odd">
<td>input <em>integer</em></td>
<td>Imposta il canale audio utilizzato come input.</td>
</tr>
<tr class="even">
<td>durata <em></em></td>
<td>Imposta la lunghezza specificata dall'utente del nastro nel videoregistratore. Questa lunghezza viene restituita dal comando <a href="status.md">status</a> length e viene fornita per la compatibilità con le applicazioni che richiedono che questo &quot; comando &quot; restituirà una lunghezza valida.</td>
</tr>
<tr class="odd">
<td>master midi</td>
<td>Imposta il sequencer MIDI come origine di sincronizzazione. I dati di sincronizzazione vengono inviati in formato MIDI. Il sequencer MCISEQ non supporta questo flag.</td>
</tr>
<tr class="even">
<td>master none</td>
<td>Impedisce al sequencer MIDI di inviare dati di sincronizzazione. Il sequencer MCISEQ non supporta questo flag.</td>
</tr>
<tr class="odd">
<td>master smpte</td>
<td>Imposta il sequencer MIDI come origine di sincronizzazione. I dati di sincronizzazione vengono inviati in formato SMPTE (Society of Motion Picture and Engineers). Il sequencer MCISEQ non supporta questo flag.</td>
</tr>
<tr class="even">
<td>offset <em>time</em></td>
<td>Imposta l'ora di <em>offset</em>SMPTE. L'offset è l'ora di inizio di una sequenza basata su SMPTE. <em>L'ora</em> è espressa come <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è frame.</td>
</tr>
<tr class="odd">
<td>output <em>integer</em></td>
<td>Imposta il canale audio usato come output.</td>
</tr>
<tr class="even">
<td>timeout <em>di sospensione</em></td>
<td>Imposta la durata massima, in millisecondi, di un <a href="pause.md">comando di</a> sospensione. Un <em>valore</em> di timeout pari a zero indica che non si verificherà alcun timeout.</td>
</tr>
<tr class="odd">
<td>durata postroll <em></em></td>
<td>Imposta la lunghezza, nel formato di ora corrente, necessaria per bloccare il trasporto vcr quando viene eseguito un <strong>comando</strong> <a href="stop.md">di</a> arresto o sospensione.</td>
</tr>
<tr class="even">
<td>mapper di porte</td>
<td>Imposta il mapper MIDI come porta che riceve i messaggi MIDI. Questo comando ha esito negativo se il mapper MIDI o una porta richiesta viene usata da un'altra applicazione.</td>
</tr>
<tr class="odd">
<td>porta none</td>
<td>Disabilita l'invio di messaggi MIDI. Questo comando chiude anche una porta MIDI.</td>
</tr>
<tr class="even">
<td>porta <em>port_number</em></td>
<td>Imposta la porta MIDI che riceve i messaggi MIDI. Questo comando ha esito negativo se la porta che si sta tentando di aprire viene usata da un'altra applicazione.</td>
</tr>
<tr class="odd">
<td>accensione <br/> power off <br/></td>
<td>Imposta l'alimentazione del dispositivo su on o off.</td>
</tr>
<tr class="even">
<td>durata della <em>pre-registrazione</em></td>
<td>Imposta la lunghezza, nel formato di ora corrente, necessaria per stabilizzare l'output del videoregistratore.</td>
</tr>
<tr class="odd">
<td>formato record SP <br/> formato record LP <br/> Formato record EP <br/></td>
<td>Imposta la modalità di registrazione per il videoregistratore su SP per la riproduzione standard, EP per la riproduzione estesa o LP per la riproduzione prolungata. Questi valori non sono destinati a essere specifici del disco rigido virtuale. Vengono mappati a tre modalità appropriate con altri formati di nastro. Ad esempio, SP esegue il mapping alla registrazione più veloce e di massima qualità.</td>
</tr>
<tr class="even">
<td>samplespersec <em>integer</em></td>
<td>Imposta la frequenza di campionamento per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td>seek exactly on<br/> seek exactly off <br/></td>
<td>Seleziona una delle due modalità di ricerca. Con &quot; seek esattamente su , seek si &quot; sposterà sempre nel frame specificato. Con &quot; seek exactly &quot; off, seek si sposterà nel fotogramma chiave più vicino prima del fotogramma specificato.</td>
</tr>
<tr class="even">
<td>file slave</td>
<td>Imposta il sequencer MIDI per l'uso dei dati dei file come origine di sincronizzazione. Si tratta dell'impostazione predefinita.</td>
</tr>
<tr class="odd">
<td>slave midi</td>
<td>Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato MIDI. Il sequencer MCISEQ non supporta questo flag.</td>
</tr>
<tr class="even">
<td>slave none</td>
<td>Imposta il sequencer MIDI per ignorare la sincronizzazione</td>
</tr>
<tr class="odd">
<td>slave smpte</td>
<td>Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato SMPTE. Il sequencer MCISEQ non supporta questo flag.</td>
</tr>
<tr class="even">
<td>fattore di velocità</td>
<td>Imposta la velocità relativa della riproduzione video e audio dall'area di lavoro. Fattore è il rapporto tra la frequenza fotogrammi nominale e la frequenza fotogrammi desiderata, in cui la frequenza fotogrammi nominale è designata come 1000. Una velocità di 500 è la metà della velocità normale, 2000 è due volte la velocità normale e così via. Se si imposta la velocità su zero, il video viene riprodotto il più velocemente possibile senza rilasciare fotogrammi e senza audio.</td>
</tr>
<tr class="odd">
<td>formato di file <em>still</em></td>
<td>Specifica il formato di file utilizzato per i comandi di acquisizione.</td>
</tr>
<tr class="even">
<td>tempo tempo_value</td>
<td>Imposta il tempo della sequenza in base al formato di ora corrente. Per un file basato su PPQN, la tempo_value viene interpretata come beat al minuto. Per un file basato su SMPTE, il tempo_value viene interpretato come frame al secondo.</td>
</tr>
<tr class="odd">
<td>byte in formato ora</td>
<td>In un formato di file PCM, imposta il formato dell'ora su byte. Tutte le informazioni sulla posizione vengono specificate come byte dopo questo comando.</td>
</tr>
<tr class="even">
<td>fotogrammi in formato ora</td>
<td>Imposta il formato dell'ora su fotogrammi. Tutti i comandi che usano valori di posizione presupporranno fotogrammi. Quando il dispositivo viene aperto, i frame sono la modalità predefinita. Supportato da videodiscs con il formato CAV.</td>
</tr>
<tr class="odd">
<td>formato ora hms</td>
<td>Imposta il formato dell'ora su ore, minuti e secondi. Tutti i comandi che usano valori di posizione presupporranno HMS. HMS è il formato predefinito per videodiscs CLV. Specificare un valore HMS come hh:mm:ss, dove hh è ore, mm è minuti e ss è secondi. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono tutti modi validi per esprimere 3 ore. <br/></td>
</tr>
<tr class="even">
<td>millisecondi di formato dell'ora</td>
<td>Imposta il formato dell'ora su millisecondi. Tutti i comandi che usano valori di posizione presupporranno millisecondi. È possibile abbreviare i millisecondi &quot; come ms &quot; . Per i dispositivi sequencer, il file di sequenza imposta il formato predefinito su PPQN o SMPTE. I dispositivi con sovrimpressione video non supportano questo flag.<br/></td>
</tr>
<tr class="odd">
<td>formato dell'ora msf</td>
<td>Imposta il formato dell'ora su minuti, secondi e fotogrammi. Tutti i comandi che usano valori di posizione presupporranno MSF (il formato predefinito per l'audio CD). Specificare un valore MSF come mm:ss:ff, dove mm è minuti, ss è secondi e ff è frame. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono modi validi per esprimere 3 minuti.<br/> I campi MSF hanno i valori massimi seguenti:<br/>
<ul>
<li>Minuti 99</li>
<li>Secondi 59</li>
<li>Fotogrammi 74</li>
</ul></td>
</tr>
<tr class="even">
<td>esempi di formato ora</td>
<td>Imposta il formato dell'ora su samples. Tutte le informazioni sulla posizione vengono specificate come esempi che segue questo comando.</td>
</tr>
<tr class="odd">
<td>formato ora smpte 24<br/> formato ora smpte 25<br/> formato ora smpte 30<br/></td>
<td>Imposta il formato dell'ora su una frequenza fotogrammi SMPTE. Per i videoregistratori, imposta il formato dell'ora su hh:mm:ss:ff, dove i valori validi sono da 00:00:00:00 a 23:59:59:xx e xx è minore dei fotogrammi al secondo, come specificato dal numero 24, 25 o 30 come specificato nel flag. In input i due punti (:) sono necessari per separare i componenti. Le unità meno significative possono essere omesse se sono 00. ad esempio, 02:00 è uguale a 02:00:00:00. Tutti i comandi che usano valori di posizione presupporranno il formato SMPTE.<br/> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br/></td>
</tr>
<tr class="even">
<td>time format smpte 30 drop</td>
<td>Imposta il formato dell'ora su SMPTE 30 drop frame rate. Per i videoregistratori, come SMPTE 30, ad eccezione del fatto che determinate posizioni del codice temporale vengono eliminate dal formato per avere le posizioni del codice temporale registrate per ogni fotogramma (alla frequenza dei fotogrammi NTSC di 29,97 fps) corrispondono in tempo reale (a 30 fps). Le posizioni del codice temporale eliminate sono le seguenti: due ogni minuto, al minuto, per i primi nove ogni dieci minuti di contenuto registrato. Ad esempio, alle 01:04:59:29, la posizione del codice temporale successiva sarà 01:05:00:02, non 01:05:00:00. Tutti i comandi che usano valori di posizione presupporranno il formato SMPTE.<br/> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br/></td>
</tr>
<tr class="odd">
<td>puntatore del brano in formato ora</td>
<td>Imposta il formato dell'ora sul puntatore del brano (sedicesima nota). Tutti i comandi che usano valori di posizione presupporranno unità puntatore del brano. Questo flag è valido solo per una sequenza di tipo PPQN di divisione.</td>
</tr>
<tr class="even">
<td>formato ora tmsf</td>
<td>Imposta il formato dell'ora su tracce, minuti, secondi e fotogrammi. Tutti i comandi che usano valori di posizione presupporranno TMSF. Specificare un valore TMSF come tt:mm:ss:ff, dove tt è tracks, mm è minutes, ss è secondi e ff è frames. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0, 3:0:0 e 3:0:0:0 sono tutti modi validi per esprimere la traccia 3. <br/> I campi TMSF hanno i valori massimi seguenti:<br/>
<ul>
<li>Tracce 99</li>
<li>Minuti 90</li>
<li>Secondi 59</li>
<li>Fotogrammi 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>traccia del formato dell'ora</td>
<td>Imposta il formato della posizione sulle tracce. Tutti i comandi che usano valori di posizione presupporranno tracce.</td>
</tr>
<tr class="even">
<td>contatore della modalità tempo</td>
<td>Imposta la modalità position-information per l'uso dei contatori vcr.</td>
</tr>
<tr class="odd">
<td>rilevamento della modalità temporale</td>
<td>Imposta la modalità di informazioni sulla posizione in base al rilevamento delle informazioni sul codice temporale sul nastro. Se vengono rilevate informazioni sul codice temporale, il tipo di ora viene impostato su timecode ; in caso contrario, il tipo di ora &quot; viene impostato su counter &quot; &quot; &quot; . &quot;Il &quot; rilevamento è una modalità speciale. Ogni volta che il driver viene aperto, viene inserito un nuovo nastro o viene eseguito il comando in modalità ora, il driver controlla la modalità ora corrente disponibile sul nastro e imposta il tipo di ora sul codice temporale o sul &quot; &quot; &quot; &quot; &quot; &quot; &quot; contatore &quot; . Una volta impostato il tipo di ora, il driver non lo modifica fino a quando non si verifica di nuovo una &quot; &quot; delle condizioni precedenti.<br/></td>
</tr>
<tr class="even">
<td>time mode timecode</td>
<td>Imposta la modalità di informazioni sulla posizione per &quot; l'uso delle &quot; informazioni sul codice temporale sul nastro.</td>
</tr>
<tr class="odd">
<td>tracking plus <br/> rilevamento meno <br/> reimpostazione del rilevamento <br/></td>
<td>Regola la velocità del trasporto videotape in incrementi fini. Usare i &quot; flag di rilevamento quando &quot; un'immagine rumorosa viene ottenuta da un videoregistratore. &quot;Il rilevamento e &quot; aumenta la velocità di trasporto. &quot;Il rilevamento meno &quot; riduce la velocità di trasporto. &quot;La &quot; reimpostazione del rilevamento restituisce la regolazione del rilevamento su zero.</td>
</tr>
<tr class="even">
<td>video disattivato</td>
<td>Disabilita l'output video.</td>
</tr>
<tr class="odd">
<td>video su</td>
<td>Abilita l'output video.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati waveform-audio. Queste proprietà descrivono come i dati sono strutturati all'interno del file e non possono essere modificati all'inizio della registrazione. L'elenco seguente identifica queste proprietà:

-   allineamento
-   bitspersample
-   bytepersec
-   channels
-   tag format
-   samplespersec

## <a name="examples"></a>Esempio

Il comando seguente imposta il formato dell'ora su millisecondi e imposta il formato waveform-audio su 8 bit, mono, 11 kHz.

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
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

 

