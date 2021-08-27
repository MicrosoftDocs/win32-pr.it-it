---
title: comando status
description: Il comando status richiede informazioni sullo stato da un dispositivo. Tutti i dispositivi riconoscono questo comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando status Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd209ed04e51671ce7d9c8a7ae88a79073836c2e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626116"
---
# <a name="status-command"></a>comando status

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo riconosce come una parola di esclusione.  Questa formulazione viene usata perché è attualmente la formulazione usata all'interno dei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo che sia allineato.

Il comando status richiede informazioni sullo stato da un dispositivo. Tutti i dispositivi riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag per la richiesta di informazioni sullo stato. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando status** e i flag usati da ogni tipo.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di dispositivo</th>
<th>Flag di richiesta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>Cdaudio type track <em>number</em></li>
<li>traccia corrente</li>
<li>length</li>
<li>numero di traccia <em>di lunghezza</em></li>
<li>supporti presenti</li>
<li>mode</li>
<li>numero di tracce</li>
<li>position</li>
<li>numero di traccia <em>di posizione</em></li>
<li>Pronto</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>Audio</li>
<li>allineamento audio</li>
<li>bit audiopersample</li>
<li>interruzioni audio</li>
<li>byte audiopersec</li>
<li>input audio</li>
<li>registrazione audio</li>
<li>origine audio</li>
<li>esempi audiopersec</li>
<li>flusso audio</li>
<li>Basso</li>
<li>bitsperpel</li>
<li>luminosità</li>
<li>color</li>
<li>elevato</li>
<li>traccia corrente</li>
<li>unità spazio <em>su disco</em></li>
<li>completamento dei file</li>
<li>formato file</li>
<li>modalità file</li>
<li>forward</li>
<li>frame ignorati</li>
<li>gamma</li>
<li>input</li>
<li>volume a sinistra</li>
<li>length</li>
<li>numero di traccia <em>di lunghezza</em></li>
<li>supporti presenti</li>
<li>mode</li>
<li>monitoraggio</li>
<li>metodo monitor</li>
<li>Nominale</li>
<li>frequenza fotogrammi nominale</li>
<li>frequenza fotogrammi record nominale</li>
<li>numero di tracce</li>
<li>output</li>
<li>Handle del riquadro</li>
<li>modalità di sospensione</li>
<li>velocità di riproduzione</li>
<li>position</li>
<li>numero di traccia <em>di posizione</em></li>
<li>Pronto</li>
<li>frequenza fotogrammi record</li>
<li>frame di <em>riferimento</em></li>
<li>dimensioni riservate</li>
<li>volume a destra</li>
<li>cercare esattamente</li>
<li>Nitidezza</li>
<li>Smpte</li>
<li>velocità</li>
<li>posizione iniziale</li>
<li>formato di file still</li>
<li>formato dell'ora</li>
<li>Tinta</li>
<li>Alti</li>
<li>non salvato</li>
<li>Video</li>
<li>indice delle chiavi video</li>
<li>colore della chiave video</li>
<li>registrazione video</li>
<li>origine video</li>
<li>numero di origine video</li>
<li>flusso video</li>
<li>volume</li>
<li>handle di finestra</li>
<li>finestra visibile</li>
<li>finestra ridotta a icona</li>
<li>finestra ingrandita</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>media present</li>
<li>mode</li>
<li>numero di tracce</li>
<li>Pronto</li>
<li>adattamento</li>
<li>handle di finestra</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>traccia corrente</li>
<li>tipo di divisione</li>
<li>length</li>
<li>length track <em>number</em> master</li>
<li>media present</li>
<li>mode</li>
<li>numero di tracce</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li>position track <em>number</em></li>
<li>Pronto</li>
<li>Schiavo</li>
<li>posizione iniziale</li>
<li>tempo</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vcr</td>
<td><ul>
<li>assemblare un record</li>
<li>monitor audio</li>
<li>numero di monitor audio</li>
<li>record audio</li>
<li>numero di traccia del record <em>audio</em></li>
<li>origine audio</li>
<li>numero di origine audio</li>
<li>channel</li>
<li>channel tuner <em>number</em></li>
<li>clock</li>
<li>id orologio</li>
<li>counter</li>
<li>formato contatore</li>
<li>risoluzione del contatore</li>
<li>traccia corrente</li>
<li>frequenza dei fotogrammi</li>
<li>index</li>
<li>index on</li>
<li>length</li>
<li>length track <em>number</em></li>
<li>media present</li>
<li>tipo di supporto</li>
<li>mode</li>
<li>numero di tracce audio</li>
<li>numero di tracce</li>
<li>numero di tracce video</li>
<li>timeout <em>di sospensione</em></li>
<li>formato di riproduzione</li>
<li>position</li>
<li>position start</li>
<li>position track <em>number</em></li>
<li>postroll duration (Durata <em>postroll)</em></li>
<li>accensione</li>
<li>durata <em>preroll</em></li>
<li>Pronto</li>
<li>formato di record</li>
<li>velocità</li>
<li>formato dell'ora</li>
<li>modalità ora</li>
<li>tipo di ora</li>
<li>timecode present</li>
<li>record timecode</li>
<li>tipo timecode</li>
<li>numero di tuner</li>
<li>monitoraggio video</li>
<li>numero di monitoraggio video</li>
<li>registrazione video</li>
<li>numero di traccia del <em>record video</em></li>
<li>origine video</li>
<li>numero di origine video</li>
<li>scrittura protetta</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>traccia corrente</li>
<li>dimensioni disco</li>
<li>forward</li>
<li>length</li>
<li>length track <em>number</em></li>
<li>media present</li>
<li>tipo di supporto</li>
<li>mode</li>
<li>numero di tracce</li>
<li>position</li>
<li>position track <em>number</em></li>
<li>Pronto</li>
<li>Lato</li>
<li>velocità</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td><ul>
<li>allineamento</li>
<li>bitspersample</li>
<li>bytespersec</li>
<li>channels</li>
<li>traccia corrente</li>
<li>tag format</li>
<li>input</li>
<li>length</li>
<li>length track <em>number</em></li>
<li>livello</li>
<li>media present</li>
<li>mode</li>
<li>numero di tracce</li>
<li>output</li>
<li>position</li>
<li>position track <em>number</em></li>
<li>Pronto</li>
<li>esempipersec</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
</tbody>
</table>



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszRequest** e i relativi significati.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>allineamento</td>
<td>Restituisce l'allineamento in blocchi dei dati, in byte.</td>
</tr>
<tr class="even">
<td>assemblare un record</td>
<td>Restituisce <strong>TRUE se</strong> il dispositivo è impostato per assemblare la registrazione in modalità.</td>
</tr>
<tr class="odd">
<td>Audio</td>
<td>Restituisce &quot; on o off a seconda del comando &quot; &quot; &quot; <a href="setaudio.md">setaudio</a> &quot; on o off più &quot; &quot; &quot; recente. Restituisce on &quot; se uno o entrambi gli &quot; altoparlanti sono abilitati e disattivato &quot; in caso &quot; contrario.</td>
</tr>
<tr class="even">
<td>allineamento audio</td>
<td>Restituisce l'allineamento dei blocchi di dati rispetto all'inizio dei dati audio della forma d'onda di input.</td>
</tr>
<tr class="odd">
<td>bit audiopersample</td>
<td>Restituisce il numero di bit per campione utilizzato dal dispositivo per la registrazione. Questo flag si applica solo ai dispositivi che supportano &quot; l'algoritmo &quot; pcm.</td>
</tr>
<tr class="even">
<td>interruzioni audio</td>
<td>Restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI si è erta. Il sistema conta un'interruzione audio ogni volta che tenta di scrivere dati audio nel driver di dispositivo e rileva che il driver ha già riprodotto tutti i dati disponibili. Questo flag viene riconosciuto solo dal driver video digitale MCIAVI. È destinato solo alla valutazione delle prestazioni. Il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="odd">
<td>byte audiopersec</td>
<td>Restituisce il numero medio di byte al secondo utilizzato per la registrazione.</td>
</tr>
<tr class="even">
<td>input audio</td>
<td>Restituisce il livello audio istantaneo approssimativo del segnale audio di input analogico. Un valore maggiore di 1000 implica una distorsione di ritaglio. Alcuni dispositivi possono restituire questo valore solo durante la registrazione dell'audio. Al valore non è associato <a href="set.md">alcun set</a> o <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="odd">
<td>monitor audio</td>
<td>Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi. Per altre informazioni, vedere il <strong>comando setaudio</strong> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>numero di monitor audio</td>
<td>Restituisce il numero di video monitorato del tipo specificato dal <strong>monitor</strong> &quot; audio di &quot; stato. Per altre informazioni, vedere il <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="odd">
<td>record audio</td>
<td>Restituisce &quot; on o off , che riflette lo stato impostato dal record &quot; &quot; &quot; <strong>setaudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>numero di traccia del record <em>audio</em></td>
<td>Restituisce <strong>TRUE se</strong> il videoregistratore è impostato per registrare l'audio. Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</td>
</tr>
<tr class="odd">
<td>esempi audiopersec</td>
<td>Restituisce il numero di campioni registrati al secondo.</td>
</tr>
<tr class="even">
<td>origine audio</td>
<td>Restituisce l'origine del digitalizzatore audio corrente: &quot; &quot; sinistra, &quot; &quot; destra, &quot; media o &quot; &quot; &quot; stereo.</td>
</tr>
<tr class="odd">
<td>numero di origine audio</td>
<td>Restituisce il numero di origine audio del tipo restituito <strong>dall'origine</strong> &quot; audio di stato &quot; . Per altre informazioni, vedere il <a href="setaudio.md">comando setaudio.</a></td>
</tr>
<tr class="even">
<td>flusso audio</td>
<td>Restituisce il numero del flusso audio corrente.</td>
</tr>
<tr class="odd">
<td>Basso</td>
<td>Restituisce il livello audio corrente.</td>
</tr>
<tr class="even">
<td>bitsperpel</td>
<td>Restituisce il numero di bit per pixel per il salvataggio dei dati acquisiti o registrati.</td>
</tr>
<tr class="odd">
<td>bitspersample</td>
<td>Restituisce i bit per campione.</td>
</tr>
<tr class="even">
<td>luminosità</td>
<td>Restituisce il livello di luminosità video corrente.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Restituisce il numero medio di byte riprodotti o registrati al secondo.</td>
</tr>
<tr class="even">
<td>cdaudio type track <em>number</em></td>
<td>Restituisce il tipo del numero di traccia specificato. Può trattarsi di &quot; audio &quot; o &quot; altro.&quot;</td>
</tr>
<tr class="odd">
<td>channel</td>
<td>Restituisce il valore intero del canale impostato sul siner.</td>
</tr>
<tr class="even">
<td>channel tuner <em>number</em></td>
<td>Se &quot; viene specificato il &quot; <em>numero</em> del siner, verrà <em></em> restituito il canale attualmente selezionato sul numero di siner logico. Si noti che possono essere presenti diversi ottimizzatori logici.</td>
</tr>
<tr class="odd">
<td>channels</td>
<td>Restituisce il numero di canali impostati (1 per mono, 2 per stereo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Restituisce l'ora esterna. L'ora deve essere un valore senza long integer che esprime gli incrementi totali. Per altre informazioni, vedere il <a href="capability.md">comando capability</a> &quot; clock increment &quot; rate.</td>
</tr>
<tr class="odd">
<td>id orologio</td>
<td>Restituisce un intero univoco che identifica l'orologio.</td>
</tr>
<tr class="even">
<td>color</td>
<td>Restituisce il livello di colore corrente.</td>
</tr>
<tr class="odd">
<td>elevato</td>
<td>Restituisce il livello di contrasto corrente.</td>
</tr>
<tr class="even">
<td>counter</td>
<td>Restituisce la posizione del contatore, nel formato del contatore corrente.</td>
</tr>
<tr class="odd">
<td>formato contatore</td>
<td>Restituisce il formato del contatore corrente. Per altre informazioni, vedere il <a href="set.md">comando set</a> &quot; counter &quot; format.</td>
</tr>
<tr class="even">
<td>risoluzione dei contatori</td>
<td>Restituisce &quot; &quot; fotogrammi &quot; o &quot; secondi, che indicano la risoluzione del contatore. Non è uguale all'accuratezza.</td>
</tr>
<tr class="odd">
<td>traccia corrente</td>
<td>Restituisce la traccia corrente. Il sequencer MCISEQ restituisce 1.</td>
</tr>
<tr class="even">
<td>dimensioni del disco</td>
<td>Restituisce 8 o 12, che indica le dimensioni del disco caricato in pollici.</td>
</tr>
<tr class="odd">
<td>unità spazio <em>su disco</em></td>
<td>Restituisce lo spazio su disco approssimativo, nel formato ora corrente, che può essere ottenuto da un comando <a href="reserve.md">reserve</a> per l'unità disco <em>specificata.</em> <em>L'unità</em> viene in genere specificata come una singola lettera o una singola lettera seguita da due punti (:). Alcuni dispositivi, tuttavia, potrebbero usare un percorso.</td>
</tr>
<tr class="even">
<td>tipo di divisione</td>
<td>Restituisce uno dei tipi di divisione di file seguenti:
<ul>
<li>PPQN</li>
<li>Frame SMPTE 24</li>
<li>Frame SMPTE 25</li>
<li>Drop frame SMPTE 30</li>
<li>Frame SMPTE 30</li>
</ul>
<br/> Usare queste informazioni per determinare il formato del file MIDI e il significato delle informazioni sul tempo e sulla posizione.<br/></td>
</tr>
<tr class="odd">
<td>completamento dei file</td>
<td>Restituisce la percentuale stimata dell'avanzamento dell'operazione di <a href="save.md">caricamento,</a> <a href="capture.md">salvataggio,</a> <a href="cut.md">acquisizione,</a> <a href="copy.md">taglia,</a> <a href="delete.md">copia,</a> <a href="paste.md">eliminazione,</a>incolla o annullamento. <a href="load.md"></a> <a href="undo.md"></a> Le applicazioni possono usarlo per fornire un indicatore visivo dello stato di avanzamento.</td>
</tr>
<tr class="even">
<td>formato file</td>
<td>Restituisce il formato di file corrente per i <a href="record.md">comandi di record</a> <strong>o</strong> salvataggio.</td>
</tr>
<tr class="odd">
<td>modalità file</td>
<td>Restituisce &quot; il &quot; caricamento, il &quot; &quot; salvataggio, la modifica o &quot; &quot; &quot; l'inattività. &quot; Durante <a href="load.md"><strong>un'operazione di</strong></a> caricamento, restituisce &quot; il caricamento di &quot; . Durante <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>le operazioni</strong></a> di salvataggio <a href="capture.md"><strong>e</strong></a> acquisizione, restituisce il salvataggio &quot; di &quot; . Durante <a href="cut.md"><strong>le operazioni</strong></a> <a href="copy.md"><strong>taglia, copia,</strong></a> <a href="delete.md"><strong>eliminazione,</strong></a> <a href="paste.md"><strong>incolla</strong></a> <a href="undo.md"><strong>o annullamento,</strong></a> restituisce la modifica &quot; di &quot; .</td>
</tr>
<tr class="even">
<td>tag format</td>
<td>Restituisce il tag di formato.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Restituisce <strong>TRUE se</strong> la direzione di riproduzione è in avanti o se il dispositivo non è in riproduzione.</td>
</tr>
<tr class="even">
<td>frequenza dei fotogrammi</td>
<td>Restituisce il numero di fotogrammi al secondo che il dispositivo userà per impostazione predefinita. I dispositivi NTSC restituiscono 30, PAL 25 e così via.</td>
</tr>
<tr class="odd">
<td>frame ignorati</td>
<td>Restituisce il numero di fotogrammi che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI. Questo flag è riconosciuto solo dal driver video digitale MCIAVI. È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Restituisce il valore impostato con <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma sul &quot; <em>valore</em>.</td>
</tr>
<tr class="odd">
<td>index</td>
<td>Restituisce la visualizzazione dell'indice corrente. Per altre informazioni, vedere il <a href="set.md"><strong>comando set</strong></a> &quot; &quot; index.</td>
</tr>
<tr class="even">
<td>index on</td>
<td>Restituisce <strong>TRUE se</strong> l'indice è on.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Restituisce il set di input. Se non è impostata, l'errore restituito indica che è possibile usare qualsiasi dispositivo. Per i dispositivi digital-video, modifica il &quot; flag bass &quot; , treble , volume , brightness , color , contrast , gamma , sharpness o tint in modo che si applichi solo &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; all'input. Si tratta dell'impostazione predefinita quando si monitora l'input.</td>
</tr>
<tr class="even">
<td>volume a sinistra</td>
<td>Restituisce il volume impostato per il canale audio sinistro.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Restituisce la lunghezza totale del supporto, nel formato di ora corrente. Per i file PPQN, la lunghezza viene restituita in unità puntatore del brano. Per i file SMPTE, viene restituito come <em>hh:mm:ss:ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è frame. Per i dispositivi vcr, la lunghezza è di 2 ore (a meno che la lunghezza non sia stata modificata in modo esplicito usando il <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>comando set).</strong></a></td>
</tr>
<tr class="even">
<td>numero di traccia <em>di lunghezza</em></td>
<td>Restituisce la lunghezza della traccia, in tempo o fotogrammi, specificata dal <em>numero</em>. Per i file PPQN, la lunghezza viene restituita in unità puntatore del brano. Per i file SMPTE, viene restituito come <em>hh:mm:ss:ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è frame.<br/></td>
</tr>
<tr class="odd">
<td>livello</td>
<td>Restituisce il valore di esempio audio PCM corrente.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Restituisce &quot; &quot; midi, &quot; none o &quot; &quot; smpte &quot; a seconda del tipo di set di sincronizzazione.</td>
</tr>
<tr class="odd">
<td>supporti presenti</td>
<td>Restituisce <strong>TRUE se</strong> il supporto viene inserito nel dispositivo o FALSE in caso <strong>contrario.</strong> Sequencer, video-overlay, digital-video e waveform-audio restituiscono <strong>TRUE.</strong></td>
</tr>
<tr class="even">
<td>tipo di supporto</td>
<td>Restituisce il tipo di supporto. Per VCRS, si tratta di &quot; 8mm, &quot; &quot; vhs, &quot; &quot; svhs, &quot; &quot; &quot; beta, &quot; &quot; Hi8, &quot; edbeta &quot; o altro &quot; &quot; . Per videodiscs, si tratta &quot; di CAV, CLV o altro , a &quot; seconda del tipo di &quot; &quot; &quot; &quot; videodisc.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Restituisce la modalità corrente del dispositivo. Tutti i dispositivi possono restituire &quot; i valori non &quot; pronti, &quot; &quot; sospesi, &quot; in riproduzione e &quot; &quot; &quot; arrestati. Alcuni dispositivi possono restituire i valori &quot; aggiuntivi &quot; aperti, &quot; &quot; parcheggiati, &quot; di registrazione e di &quot; &quot; &quot; ricerca.</td>
</tr>
<tr class="even">
<td>monitoraggio</td>
<td>Restituisce &quot; il file o &quot; &quot; l'input &quot; . Il valore restituito indica l'origine della presentazione corrente.</td>
</tr>
<tr class="odd">
<td>metodo monitor</td>
<td>Restituisce &quot; &quot; pre, &quot; post o direct &quot; &quot; &quot; . Il valore restituito indica il metodo utilizzato per il monitoraggio dell'input.</td>
</tr>
<tr class="even">
<td>Nominale</td>
<td>L'elemento modifica i flag &quot; bass , brightness , color , contrast , &quot; gamma &quot; , &quot; &quot; &quot; &quot; &quot; &quot; sharpness , tint , &quot; &quot; &quot; &quot; treble &quot; &quot; &quot; &quot; e volume &quot; in modo da restituire il valore nominale anziché l'impostazione corrente.</td>
</tr>
<tr class="odd">
<td>frequenza fotogrammi nominale</td>
<td>Restituisce la frequenza fotogrammi nominale associata al file. Le unità sono in fotogrammi al secondo moltiplicate per 1000.</td>
</tr>
<tr class="even">
<td>frequenza fotogrammi record nominale</td>
<td>Restituisce la frequenza fotogrammi nominale associata al segnale video di input. Le unità sono in fotogrammi al secondo moltiplicate per 1000.</td>
</tr>
<tr class="odd">
<td>numero di tracce audio</td>
<td>Restituisce il numero di tracce audio nel supporto.</td>
</tr>
<tr class="even">
<td>numero di tracce</td>
<td>Restituisce il numero di tracce nel supporto. I dispositivi MCISEQ e MCIWAVE restituiscono 1, come la maggior parte dei dispositivi vcr. Il dispositivo MCIPIONR non supporta questo flag.</td>
</tr>
<tr class="odd">
<td>numero di tracce video</td>
<td>Restituisce il numero di tracce video nel supporto.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Restituisce l'offset di un file basato su SMPTE. L'offset è l'ora di inizio di una sequenza basata su SMPTE. L'ora viene restituita come <em>hh:mm:ss:ff,</em>dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è fotogrammi.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Restituisce l'output attualmente impostato. Se non è impostato alcun output, l'errore restituito indica che è possibile usare qualsiasi dispositivo. Per i dispositivi video digitali, modifica il flag di tinta, acuto, &quot; &quot; volume, &quot; &quot; &quot; &quot; &quot; luminosità, &quot; &quot; &quot; colore, contrasto, gamma, &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; nitidezza o flag di tinta in modo che si applichi solo all'output. Questa è l'impostazione predefinita quando si monitora un file.</td>
</tr>
<tr class="even">
<td>modalità di sospensione</td>
<td>Restituisce &quot; la registrazione se il dispositivo è in pausa durante la &quot; registrazione. La riproduzione &quot; viene &quot; restituita se il dispositivo è in pausa durante la riproduzione. Restituisce l'errore &quot; Azione non applicabile in modalità &quot; corrente se il dispositivo non è in pausa.</td>
</tr>
<tr class="odd">
<td>timeout di sospensione</td>
<td>Restituisce la durata massima, in millisecondi, di un <a href="pause.md"><strong>comando di</strong></a> sospensione.</td>
</tr>
<tr class="even">
<td>formato di riproduzione</td>
<td>Restituisce un codice che indica il formato in cui verrà riprodotta la videotape, se rilevabile: &quot; lp &quot; , &quot; ep &quot; , sp o &quot; altro &quot; &quot; &quot; . Per altre informazioni, vedere il &quot; flag di formato del &quot; record.</td>
</tr>
<tr class="odd">
<td>velocità di riproduzione</td>
<td>Restituisce un valore che rappresenta il tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione. Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali. Un valore pari a 2000, ad esempio, indicherebbe che la riproduzione della sequenza AVI ha richiesto il doppio del tempo necessario per la riproduzione. Questo flag viene riconosciuto solo dal driver video digitale MCIAVI. È destinato solo alla valutazione delle prestazioni. Il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Restituisce il numero di porta MIDI assegnato alla sequenza.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Restituisce la posizione corrente. Per i file PPQN, la posizione viene restituita in unità puntatore del brano. Per i file SMPTE, viene restituito come <em>hh:mm:ss:ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, ss è secondi e <em>ff</em> è frame.<br/></td>
</tr>
<tr class="even">
<td>position start</td>
<td>Restituisce la posizione dell'inizio del supporto utilizzabile.</td>
</tr>
<tr class="odd">
<td>position track <em>number</em></td>
<td>Restituisce la posizione dell'inizio della traccia specificata dal <em>numero</em>. Per i file PPQN, il formato dell'ora viene restituito in unità puntatore del brano. Per i file SMPTE, viene restituito come <em>hh:mm:ss:ff</em>, dove <em>hh</em> è ore, <em>mm</em> è minuti, <em>ss</em> è secondi e <em>ff</em> è frame. Il sequencer MCISEQ restituisce zero. Il dispositivo MCIPIONR non supporta questo flag. Il dispositivo MCIWAVE restituisce zero.</td>
</tr>
<tr class="even">
<td>postroll duration (Durata postroll)</td>
<td>Restituisce la lunghezza della videotape, nel formato di ora corrente, necessaria <a href="pause.md"><strong></strong></a> per bloccare il trasporto vcr quando viene eseguito un comando <a href="stop.md"><strong>di</strong></a> arresto o sospensione.</td>
</tr>
<tr class="odd">
<td>accensione</td>
<td>Restituisce <strong>TRUE</strong> se l'alimentazione del videoregistratore è on.</td>
</tr>
<tr class="even">
<td>durata preroll</td>
<td>Restituisce la lunghezza della videotape, nel formato di ora corrente, necessaria per stabilizzare l'output del videoregistratore.</td>
</tr>
<tr class="odd">
<td>Pronto</td>
<td>Restituisce <strong>TRUE</strong> se il dispositivo è pronto ad accettare un altro comando.</td>
</tr>
<tr class="even">
<td>formato di record</td>
<td>Restituisce un codice che indica il formato in cui verrà registrata la videotape. I tipi restituiti correnti &quot; sono lp &quot; , &quot; ep , sp o &quot; &quot; altri &quot; &quot; &quot; . Questi formati non sono specifici del disco rigido virtuale e possono essere applicati a qualsiasi videoregistratore con più formati di registrazione selezionabili. Il tipo sp è il formato di registrazione più veloce e di massima qualità e viene usato come impostazione predefinita nelle videoregistratori &quot; &quot; a formato singolo.</td>
</tr>
<tr class="odd">
<td>frequenza dei fotogrammi di record</td>
<td>Restituisce la frequenza dei fotogrammi, in fotogrammi al secondo moltiplicata per 1000, usata per la compressione.</td>
</tr>
<tr class="even">
<td>frame di <em>riferimento</em></td>
<td>Restituisce il numero di fotogramma per l'immagine del fotogramma chiave più vicina che precede il <em>frame specificato.</em></td>
</tr>
<tr class="odd">
<td>dimensioni riservate</td>
<td>Restituisce le dimensioni, nel formato di ora corrente, dell'area di lavoro riservata. Le dimensioni corrispondono al tempo approssimativo necessario per riprodurre i dati compressi da un'area di lavoro completa. Restituisce zero se non è disponibile spazio su disco riservato. Questo flag restituisce le dimensioni approssimative perché lo spazio su disco preciso per i dati compressi non può essere previsto, in generale, fino a dopo la compressione dei dati.</td>
</tr>
<tr class="even">
<td>volume destro</td>
<td>Restituisce il volume impostato per il canale audio destro.</td>
</tr>
<tr class="odd">
<td>esempipersec</td>
<td>Restituisce il numero di campioni riprodotti o registrati al secondo.</td>
</tr>
<tr class="even">
<td>seek exactly</td>
<td>Restituisce on o off , che indica se il flag seek è impostato &quot; o &quot; meno &quot; &quot; &quot; &quot; esattamente.</td>
</tr>
<tr class="odd">
<td>Nitidezza</td>
<td>Restituisce il livello di nitidezza corrente del dispositivo.</td>
</tr>
<tr class="even">
<td>Lato</td>
<td>Restituisce 1 o 2 per indicare quale lato del file videodisc viene caricato.</td>
</tr>
<tr class="odd">
<td>Schiavo</td>
<td>Restituisce &quot; il file , &quot; &quot; midi , &quot; &quot; none o &quot; &quot; smpte &quot; a seconda del tipo di set di sincronizzazione.</td>
</tr>
<tr class="even">
<td>Smpte</td>
<td>Restituisce il timecode SMPTE associato alla posizione corrente nell'area di lavoro. Si tratta di una stringa nel formato <em>dd:dd:dd:dd,</em>dove <em>d indica</em> una cifra da 0 a 9. Se i dati dell'area di lavoro non includono dati del timecode, questo flag restituisce 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocità</td>
<td>Restituisce la velocità corrente del dispositivo in fotogrammi al secondo (o nello stesso formato usato dal <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>comando imposta</strong></a> &quot; &quot; velocità). Il lettore videodisc MCIPIONR non supporta questo flag.</td>
</tr>
<tr class="even">
<td>posizione iniziale</td>
<td>Restituisce la posizione iniziale del supporto.</td>
</tr>
<tr class="odd">
<td>formato di file still</td>
<td>Restituisce il formato di file corrente per il <a href="capture.md"><strong>comando di</strong></a> acquisizione.</td>
</tr>
<tr class="even">
<td>adattamento</td>
<td>Restituisce <strong>TRUE se</strong> l'estensione è abilitata.</td>
</tr>
<tr class="odd">
<td>tempo</td>
<td>Restituisce il tempo corrente di una sequenza MIDI nel formato di ora corrente. Per i file in formato PPQN, il tempo è in picchi al minuto. Per i file in formato SMPTE, il tempo è in fotogrammi al secondo.</td>
</tr>
<tr class="even">
<td>formato dell'ora</td>
<td>Restituisce il formato dell'ora corrente. Per altre informazioni, vedere i formati di ora nel <a href="set.md"><strong>comando set.</strong></a></td>
</tr>
<tr class="odd">
<td>modalità ora</td>
<td>Restituisce la modalità temporale della posizione corrente. Può essere il &quot; &quot; rilevamento, &quot; il timecode &quot; o il &quot; contatore &quot; .</td>
</tr>
<tr class="even">
<td>tipo di ora</td>
<td>Restituisce il tempo di posizione corrente in uso: &quot; timecode &quot; o &quot; contatore &quot; .</td>
</tr>
<tr class="odd">
<td>timecode present</td>
<td>Restituisce <strong>TRUE</strong> se il timecode è stato registrato nella posizione corrente sul nastro. Il timecode deve avanzare dalla posizione corrente. Potrebbe essere necessario riprodurre un videoregistratore per controllare questa condizione.</td>
</tr>
<tr class="even">
<td>record timecode</td>
<td>Restituisce <strong>TRUE se</strong> il videoregistratore è impostato per registrare il codice temporale.</td>
</tr>
<tr class="odd">
<td>tipo di codice temporale</td>
<td>Restituisce &quot; smpte, &quot; &quot; smpte &quot; drop, other &quot; o &quot; &quot; &quot; none. Si noti che i fotogrammi al secondo possono essere ottenuti dal comando status frame rate e l'accuratezza del dispositivo può essere restituita dal comando &quot; &quot; <a href="capability.md"><strong>capability</strong></a> &quot; seek &quot; accuracy.</td>
</tr>
<tr class="even">
<td>Tinta</td>
<td>Restituisce il livello di tinta video corrente.</td>
</tr>
<tr class="odd">
<td>Alti</td>
<td>Restituisce il livello audio acuto corrente.</td>
</tr>
<tr class="even">
<td>numero di siner</td>
<td>Restituisce il numero di siner logico corrente.</td>
</tr>
<tr class="odd">
<td>non salvato</td>
<td>Restituisce <strong>TRUE</strong> se nell'area di lavoro sono presenti dati registrati che potrebbero essere persi a causa di un comando close <a href="close.md"><strong>,</strong></a> <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve,</strong></a> <a href="cut.md"><strong>cut,</strong></a> <a href="delete.md"><strong>delete</strong></a> <a href="paste.md"><strong>o paste.</strong></a> Restituisce <strong>FALSE in caso contrario.</strong></td>
</tr>
<tr class="even">
<td>Video</td>
<td>Restituisce &quot; on o off , che riflette lo stato impostato dal comando &quot; &quot; &quot; <a href="setvideo.md"><strong>setvideo.</strong></a></td>
</tr>
<tr class="odd">
<td>colore della chiave video</td>
<td>Restituisce il valore per il colore della chiave.</td>
</tr>
<tr class="even">
<td>indice delle chiavi video</td>
<td>Restituisce il valore per l'indice della chiave.</td>
</tr>
<tr class="odd">
<td>monitoraggio video</td>
<td>Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi. Per altre informazioni, vedere il <a href="setvideo.md"><strong>comando setvideo</strong></a> &quot; &quot; monitor.</td>
</tr>
<tr class="even">
<td>numero di monitoraggio video</td>
<td>Restituisce il numero video monitorato del tipo restituito dal &quot; monitoraggio video di &quot; stato. Per altre informazioni, vedere il <a href="setvideo.md">comando setvideo.</a></td>
</tr>
<tr class="odd">
<td>registrazione video</td>
<td>Restituisce &quot; on o off , che riflette lo stato corrente impostato da &quot; &quot; &quot; <a href="setvideo.md"><strong>setvideo</strong></a> &quot; record &quot; .</td>
</tr>
<tr class="even">
<td>numero di traccia del record <em>video</em></td>
<td>Restituisce <strong>TRUE</strong> se il videoregistratore è impostato per registrare il video. Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</td>
</tr>
<tr class="odd">
<td>origine video</td>
<td>Restituisce il tipo di origine video. Per altre informazioni, vedere il <a href="setvideo.md"><strong>comando setvideo.</strong></a></td>
</tr>
<tr class="even">
<td>numero di origine video</td>
<td>Restituisce un numero corrispondente all'origine video del tipo in uso. Ad esempio, restituisce 2 se viene usato il secondo input di origine video NTSC.</td>
</tr>
<tr class="odd">
<td>flusso video</td>
<td>Restituisce il numero di flusso video corrente.</td>
</tr>
<tr class="even">
<td>volume</td>
<td>Restituisce il volume medio al parlante sinistro e destro. Verrà restituito un errore se il dispositivo non è stato riprodotto o se il volume non è stato impostato.</td>
</tr>
<tr class="odd">
<td>handle di finestra</td>
<td>Restituisce il valore decimale ASCII per l'handle della finestra nella parola di ordine basso del valore restituito.</td>
</tr>
<tr class="even">
<td>finestra ingrandita</td>
<td>Restituisce <strong>TRUE se</strong> la finestra è ingrandita.</td>
</tr>
<tr class="odd">
<td>finestra ridotta a icona</td>
<td>Restituisce <strong>TRUE se</strong> la finestra è ridotta a icona.</td>
</tr>
<tr class="even">
<td>finestra visibile</td>
<td>Restituisce <strong>TRUE</strong> se la finestra non è nascosta.</td>
</tr>
<tr class="odd">
<td>protetto da scrittura</td>
<td>Restituisce <strong>TRUE</strong> se il dispositivo rileva che non è in grado di registrare, ovvero se la protezione da scrittura è impostata su . Se è in grado di registrare o se non è in grado di determinare se può registrare (senza scrivere effettivamente), il driver restituisce <strong>FALSE.</strong></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce informazioni nel *parametro lpszReturnString* di [**mciSendString**](/previous-versions//dd757161(v=vs.85)). Le informazioni dipendono dal tipo di richiesta.

## <a name="remarks"></a>Commenti

Prima di eseguire comandi che usano valori di posizione, è necessario impostare il formato ora desiderato usando il [comando set.](set.md)

## <a name="examples"></a>Esempio

Il comando seguente restituisce la modalità corrente del dispositivo "mysound".

``` syntax
status mysound mode
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[Catturare](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[Tagliare](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[carico](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Incollare](paste.md)
</dt> <dt>

[Registrazione](record.md)
</dt> <dt>

[Riserva](reserve.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[cancella](undo.md)
</dt> </dl>

 

