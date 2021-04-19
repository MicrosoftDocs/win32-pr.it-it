---
title: comando status
description: Il comando di stato richiede informazioni sullo stato da un dispositivo. Tutti i dispositivi riconoscono questo comando.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- comando di stato Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320054"
---
# <a name="status-command"></a>comando status

> [!NOTE]
> Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.  Questo testo viene usato in quanto è attualmente il testo usato nei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.

Il comando di stato richiede informazioni sullo stato da un dispositivo. Tutti i dispositivi riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag per la richiesta delle informazioni sullo stato. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando di **stato** e i flag utilizzati da ogni tipo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<li><em>numero</em> di traccia del tipo CDAudio</li>
<li>traccia corrente</li>
<li>length</li>
<li><em>numero</em> traccia lunghezza</li>
<li>supporti presenti</li>
<li>mode</li>
<li>numero di tracce</li>
<li>position</li>
<li><em>numero</em> di traccia posizione</li>
<li>pronto</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>Audio</li>
<li>allineamento audio</li>
<li>BitsPerSample audio</li>
<li>interruzioni audio</li>
<li>bytespersec audio</li>
<li>input audio</li>
<li>record audio</li>
<li>origine audio</li>
<li>samplespersec audio</li>
<li>flusso audio</li>
<li>basso</li>
<li>BitsPerPel</li>
<li>luminosità</li>
<li>color</li>
<li>elevato</li>
<li>traccia corrente</li>
<li><em>unità</em> spazio su disco</li>
<li>completamento file</li>
<li>formato file</li>
<li>modalità file</li>
<li>forward</li>
<li>frame ignorati</li>
<li>gamma</li>
<li>input</li>
<li>volume sinistro</li>
<li>length</li>
<li><em>numero</em> traccia lunghezza</li>
<li>supporti presenti</li>
<li>mode</li>
<li>monitoraggio</li>
<li>Metodo Monitor</li>
<li>nominale</li>
<li>frequenza fotogrammi nominale</li>
<li>frequenza fotogrammi record nominale</li>
<li>numero di tracce</li>
<li>output</li>
<li>handle tavolozza</li>
<li>modalità di sospensione</li>
<li>velocità di riproduzione</li>
<li>position</li>
<li><em>numero</em> di traccia posizione</li>
<li>pronto</li>
<li>frequenza fotogrammi record</li>
<li><em>frame</em> di riferimento</li>
<li>dimensioni riservate</li>
<li>volume giusto</li>
<li>ricerca esatta</li>
<li>nitidezza</li>
<li>SMPTE</li>
<li>velocità</li>
<li>posizione iniziale</li>
<li>formato file ancora</li>
<li>formato dell'ora</li>
<li>tinta</li>
<li>acuti</li>
<li>unsaved</li>
<li>Video</li>
<li>indice chiave video</li>
<li>colore della chiave video</li>
<li>record video</li>
<li>origine video</li>
<li>numero di origine video</li>
<li>flusso video</li>
<li>volume</li>
<li>handle finestra</li>
<li>finestra visibile</li>
<li>finestra ridotta a icona</li>
<li>finestra ingrandita</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>supporti presenti</li>
<li>mode</li>
<li>numero di tracce</li>
<li>pronto</li>
<li>adattamento</li>
<li>handle finestra</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>traccia corrente</li>
<li>tipo divisione</li>
<li>length</li>
<li>Master <em>numero</em> traccia lunghezza</li>
<li>supporti presenti</li>
<li>mode</li>
<li>numero di tracce</li>
<li>offset</li>
<li>port</li>
<li>position</li>
<li><em>numero</em> di traccia posizione</li>
<li>pronto</li>
<li>schiavo</li>
<li>posizione iniziale</li>
<li>tempo</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>assembla record</li>
<li>monitoraggio audio</li>
<li>numero di monitor audio</li>
<li>record audio</li>
<li><em>numero</em> di traccia del record audio</li>
<li>origine audio</li>
<li>numero di origine audio</li>
<li>channel</li>
<li><em>numero</em> Tuner del canale</li>
<li>clock</li>
<li>ID Clock</li>
<li>counter</li>
<li>formato contatore</li>
<li>risoluzione del contatore</li>
<li>traccia corrente</li>
<li>frequenza fotogrammi</li>
<li>indice</li>
<li>Indice in</li>
<li>length</li>
<li><em>numero</em> traccia lunghezza</li>
<li>supporti presenti</li>
<li>tipo di supporto</li>
<li>mode</li>
<li>numero di tracce audio</li>
<li>numero di tracce</li>
<li>numero di tracce video</li>
<li><em>timeout</em> pausa</li>
<li>formato di riproduzione</li>
<li>position</li>
<li>inizio posizione</li>
<li><em>numero</em> di traccia posizione</li>
<li><em>durata</em> postroll</li>
<li>accensione</li>
<li><em>durata</em> preroll</li>
<li>pronto</li>
<li>formato record</li>
<li>velocità</li>
<li>formato dell'ora</li>
<li>modalità ora</li>
<li>tipo Time</li>
<li>codice temporale presente</li>
<li>record timecode</li>
<li>tipo di timecode</li>
<li>numero Tuner</li>
<li>monitoraggio video</li>
<li>numero di monitor video</li>
<li>record video</li>
<li><em>numero</em> di traccia del record video</li>
<li>origine video</li>
<li>numero di origine video</li>
<li>scrittura protetta</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>traccia corrente</li>
<li>dimensioni del disco</li>
<li>forward</li>
<li>length</li>
<li><em>numero</em> traccia lunghezza</li>
<li>supporti presenti</li>
<li>tipo di supporto</li>
<li>mode</li>
<li>numero di tracce</li>
<li>position</li>
<li><em>numero</em> di traccia posizione</li>
<li>pronto</li>
<li>lato</li>
<li>velocità</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li>allineamento</li>
<li>BitsPerSample</li>
<li>bytespersec</li>
<li>channels</li>
<li>traccia corrente</li>
<li>Tag di formato</li>
<li>input</li>
<li>length</li>
<li><em>numero</em> traccia lunghezza</li>
<li>livello</li>
<li>supporti presenti</li>
<li>mode</li>
<li>numero di tracce</li>
<li>output</li>
<li>position</li>
<li><em>numero</em> di traccia posizione</li>
<li>pronto</li>
<li>samplespersec</li>
<li>posizione iniziale</li>
<li>formato dell'ora</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRequest** e i relativi significati.



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
<td>allineamento</td>
<td>Restituisce l'allineamento del blocco dei dati in byte.</td>
</tr>
<tr class="even">
<td>assembla record</td>
<td>Restituisce <strong>true</strong> se il dispositivo è impostato per assemblare la registrazione in modalità.</td>
</tr>
<tr class="odd">
<td>Audio</td>
<td>Restituisce &quot; on &quot; o &quot; off &quot; a seconda del <a href="setaudio.md"></a> &quot; &quot; comando di &quot; disconnessione o disattivazione più recente &quot; . Restituisce &quot; on &quot; se uno o entrambi gli altoparlanti sono abilitati e &quot; disattivato &quot; in caso contrario.</td>
</tr>
<tr class="even">
<td>allineamento audio</td>
<td>Restituisce l'allineamento dei blocchi di dati rispetto all'inizio dei dati audio della forma d'onda di input.</td>
</tr>
<tr class="odd">
<td>BitsPerSample audio</td>
<td>Restituisce il numero di bit per campione usato dal dispositivo per la registrazione. Questo flag si applica solo ai dispositivi che supportano l' &quot; &quot; algoritmo PCM.</td>
</tr>
<tr class="even">
<td>interruzioni audio</td>
<td>Restituisce il numero di volte in cui la parte audio dell'ultima sequenza AVI è stata interrotta. Il sistema conta un'interruzioni audio ogni volta che tenta di scrivere i dati audio nel driver di dispositivo e rileva che il driver ha già eseguito tutti i dati disponibili. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI. È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="odd">
<td>bytespersec audio</td>
<td>Restituisce il numero medio di byte al secondo usati per la registrazione.</td>
</tr>
<tr class="even">
<td>input audio</td>
<td>Restituisce il livello di audio istantaneo approssimativo del segnale audio di input analogico. Un valore maggiore di 1000 implica la distorsione di ritaglio. Alcuni dispositivi possono restituire questo valore solo durante la registrazione dell'audio. Al valore non è associato alcun comando <a href="set.md">set</a> o <a href="setaudio.md">seaudio</a> .</td>
</tr>
<tr class="odd">
<td>monitoraggio audio</td>
<td>Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi. Per ulteriori informazioni, vedere il comando di monitoraggio <strong>sefonica</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td>numero di monitor audio</td>
<td>Restituisce il numero del video monitorato del tipo specificato dal <strong></strong> &quot; monitoraggio audio di stato &quot; . Per ulteriori informazioni, vedere il comando <a href="setaudio.md">seaudio</a> .</td>
</tr>
<tr class="odd">
<td>record audio</td>
<td>Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato impostato dal record <strong>seaudio</strong> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>numero</em> di traccia del record audio</td>
<td>Restituisce <strong>true</strong> se il VCR è impostato per registrare l'audio. Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</td>
</tr>
<tr class="odd">
<td>samplespersec audio</td>
<td>Restituisce il numero di campioni al secondo registrati.</td>
</tr>
<tr class="even">
<td>origine audio</td>
<td>Restituisce l'origine del digitalizzatore audio corrente: a &quot; sinistra &quot; , a &quot; destra &quot; , a &quot; media &quot; o &quot; stereo &quot; .</td>
</tr>
<tr class="odd">
<td>numero di origine audio</td>
<td>Restituisce il numero di origine audio del tipo restituito dall' <strong></strong> &quot; origine audio di stato &quot; . Per ulteriori informazioni, vedere il comando <a href="setaudio.md">seaudio</a> .</td>
</tr>
<tr class="even">
<td>flusso audio</td>
<td>Restituisce il numero di flusso audio corrente.</td>
</tr>
<tr class="odd">
<td>basso</td>
<td>Restituisce il livello di bassi audio corrente.</td>
</tr>
<tr class="even">
<td>BitsPerPel</td>
<td>Restituisce il numero di bit per pixel per il salvataggio dei dati acquisiti o registrati.</td>
</tr>
<tr class="odd">
<td>BitsPerSample</td>
<td>Restituisce i bit per campione.</td>
</tr>
<tr class="even">
<td>luminosità</td>
<td>Restituisce il livello di luminosità video corrente.</td>
</tr>
<tr class="odd">
<td>bytespersec</td>
<td>Restituisce il numero medio di byte al secondo riprodotti o registrati.</td>
</tr>
<tr class="even">
<td><em>numero</em> di traccia del tipo CDAudio</td>
<td>Restituisce il tipo del numero di traccia specificato. Può trattarsi di un &quot; audio o di un &quot; &quot; altro.&quot;</td>
</tr>
<tr class="odd">
<td>channel</td>
<td>Restituisce il valore intero del set di canali sul sintonizzatore.</td>
</tr>
<tr class="even">
<td><em>numero</em> Tuner del canale</td>
<td>Se &quot; &quot; viene specificato un <em>numero</em> di Tuner, viene restituito il canale attualmente selezionato sul <em>numero</em> di sintonizzatore logico. Si noti che possono essere presenti diversi sintonizzatori logici.</td>
</tr>
<tr class="odd">
<td>channels</td>
<td>Restituisce il numero di canali impostati (1 per mono, 2 per stereo).</td>
</tr>
<tr class="even">
<td>clock</td>
<td>Restituisce l'ora esterna. L'ora deve essere un unsigned long integer che esprime gli incrementi totali. Per ulteriori informazioni, vedere il comando <a href="capability.md">Capability</a> &quot; Clock rate rate &quot; .</td>
</tr>
<tr class="odd">
<td>ID Clock</td>
<td>Restituisce un intero univoco che identifica il clock.</td>
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
<td>Restituisce il formato del contatore corrente. Per ulteriori informazioni, vedere il comando <a href="set.md">imposta</a> &quot; formato contatore &quot; .</td>
</tr>
<tr class="even">
<td>risoluzione del contatore</td>
<td>Restituisce &quot; &quot; i frame &quot; o &quot; i secondi, che indicano la risoluzione del contatore. Questa operazione non è identica a quella dell'accuratezza.</td>
</tr>
<tr class="odd">
<td>traccia corrente</td>
<td>Restituisce la traccia corrente. Il sequencer MCISEQ restituisce 1.</td>
</tr>
<tr class="even">
<td>dimensioni del disco</td>
<td>Restituisce 8 o 12, che indica le dimensioni in pollici del disco caricato.</td>
</tr>
<tr class="odd">
<td><em>unità</em> spazio su disco</td>
<td>Restituisce lo spazio su disco approssimativo, nel formato dell'ora corrente, che può essere ottenuto da un comando di <a href="reserve.md">riserva</a> per l'unità disco specificata <em>.</em> L' <em>unità</em> viene in genere specificata come una singola lettera o una singola lettera seguita da due punti (:). Alcuni dispositivi, tuttavia, potrebbero usare un percorso.</td>
</tr>
<tr class="even">
<td>tipo divisione</td>
<td>Restituisce uno dei seguenti tipi di divisione file:
<ul>
<li>PPQN</li>
<li>Frame SMPTE 24</li>
<li>Frame SMPTE 25</li>
<li>Frame di rilascio SMPTE 30</li>
<li>Frame SMPTE 30</li>
</ul>
<br/> Usare queste informazioni per determinare il formato del file MIDI e il significato delle informazioni sul tempo e sulla posizione.<br/></td>
</tr>
<tr class="odd">
<td>completamento file</td>
<td>Restituisce la percentuale stimata di un'operazione di <a href="load.md">caricamento</a>, <a href="save.md">salvataggio</a>, <a href="capture.md">acquisizione</a>, <a href="cut.md">taglia</a>, <a href="copy.md">copia</a>, <a href="delete.md">eliminazione</a>, <a href="paste.md">Incolla</a>o <a href="undo.md">annullamento</a> . (Le applicazioni possono usare questa operazione per fornire un indicatore visivo dello stato di avanzamento).</td>
</tr>
<tr class="even">
<td>formato file</td>
<td>Restituisce il formato di file corrente per i comandi <a href="record.md">record</a> o <strong>Save</strong> .</td>
</tr>
<tr class="odd">
<td>modalità file</td>
<td>Restituisce il &quot; caricamento &quot; , il &quot; salvataggio, la modifica o il tempo &quot; &quot; &quot; di &quot; inattività &quot; . Durante un'operazione di <a href="load.md"><strong>caricamento</strong></a> , viene restituito il &quot; caricamento &quot; . Durante le operazioni di <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>salvataggio</strong></a> e <a href="capture.md"><strong>acquisizione</strong></a> , viene restituito il &quot; salvataggio &quot; . Durante le operazioni <a href="cut.md"><strong>Cut</strong></a>, <a href="copy.md"><strong>Copy</strong></a>, <a href="delete.md"><strong>Delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>o <a href="undo.md"><strong>Undo</strong></a> , viene restituita la &quot; modifica &quot; .</td>
</tr>
<tr class="even">
<td>Tag di formato</td>
<td>Restituisce il tag di formato.</td>
</tr>
<tr class="odd">
<td>forward</td>
<td>Restituisce <strong>true</strong> se la direzione di riproduzione è diretta o se il dispositivo non viene riprodotto.</td>
</tr>
<tr class="even">
<td>frequenza fotogrammi</td>
<td>Restituisce il numero di fotogrammi al secondo che il dispositivo utilizzerà per impostazione predefinita. I dispositivi NTSC restituiscono 30, PAL 25 e così via.</td>
</tr>
<tr class="odd">
<td>frame ignorati</td>
<td>Restituisce il numero di frame che non sono stati disegnati quando è stata riprodotta l'ultima sequenza AVI. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI. È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="even">
<td>gamma</td>
<td>Restituisce il valore impostato con <a href="setvideo.md"><strong>sevideo</strong></a> &quot; gamma su &quot; <em>value</em>.</td>
</tr>
<tr class="odd">
<td>indice</td>
<td>Restituisce la visualizzazione dell'indice corrente. Per ulteriori informazioni, vedere il comando <a href="set.md"><strong>set</strong></a> &quot; index &quot; .</td>
</tr>
<tr class="even">
<td>Indice in</td>
<td>Restituisce <strong>true</strong> se l'indice è impostato su on.</td>
</tr>
<tr class="odd">
<td>input</td>
<td>Restituisce il set di input. Se non è impostata, l'errore restituito indica che è possibile usare qualsiasi dispositivo. Per i dispositivi digitali video, modifica il &quot; &quot; flag Bass, &quot; Treble &quot; , &quot; volume &quot; , &quot; luminosità &quot; , &quot; colore &quot; , &quot; contrasto &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; o &quot; tinta, &quot; in modo che venga applicato solo all'input. Si tratta dell'impostazione predefinita durante il monitoraggio dell'input.</td>
</tr>
<tr class="even">
<td>volume sinistro</td>
<td>Restituisce il set di volumi per il canale audio sinistro.</td>
</tr>
<tr class="odd">
<td>length</td>
<td>Restituisce la lunghezza totale del supporto, nel formato dell'ora corrente. Per i file PPQN, la lunghezza viene restituita nelle unità del puntatore del brano. Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames. Per i dispositivi VCR, la lunghezza è di 2 ore, a meno che la lunghezza non sia stata modificata in modo esplicito con il comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> .</td>
</tr>
<tr class="even">
<td><em>numero</em> traccia lunghezza</td>
<td>Restituisce la lunghezza della traccia, nel tempo o nei frame, specificata per <em>numero</em>. Per i file PPQN, la lunghezza viene restituita nelle unità del puntatore del brano. Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.<br/></td>
</tr>
<tr class="odd">
<td>livello</td>
<td>Restituisce il valore di esempio dell'audio PCM corrente.</td>
</tr>
<tr class="even">
<td>master</td>
<td>Restituisce &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE &quot; a seconda del tipo di set di sincronizzazione.</td>
</tr>
<tr class="odd">
<td>supporti presenti</td>
<td>Restituisce <strong>true</strong> se il supporto viene inserito nel dispositivo o <strong>false</strong> in caso contrario. Sequencer, video overlay, Digital-video e waveform-i dispositivi audio restituiscono <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>tipo di supporto</td>
<td>Restituisce il tipo di supporto. Per i VCR, questo è &quot; 8 mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; o &quot; altro &quot; . Per videodischi, si tratta di &quot; CAV &quot; , &quot; CLV &quot; o &quot; other &quot; , a seconda del tipo di videodisco.</td>
</tr>
<tr class="odd">
<td>mode</td>
<td>Restituisce la modalità corrente del dispositivo. Tutti i dispositivi possono restituire i &quot; valori non pronti &quot; , &quot; sospesi, in &quot; &quot; riproduzione &quot; e &quot; interrotti &quot; . Alcuni dispositivi possono restituire &quot; &quot; valori aperti, &quot; parcheggiati, &quot; &quot; di registrazione &quot; e di &quot; ricerca aggiuntivi &quot; .</td>
</tr>
<tr class="even">
<td>monitoraggio</td>
<td>Restituisce un &quot; file &quot; o un &quot; input &quot; . Il valore restituito indica l'origine della presentazione corrente.</td>
</tr>
<tr class="odd">
<td>Metodo Monitor</td>
<td>Restituisce &quot; pre &quot; , &quot; Post &quot; o &quot; diretto &quot; . Il valore restituito indica il metodo utilizzato per il monitoraggio dell'input.</td>
</tr>
<tr class="even">
<td>nominale</td>
<td>L'elemento modifica i &quot; &quot; flag Bass, &quot; luminosità &quot; , &quot; Color &quot; , &quot; Contrast &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; , &quot; tinta, &quot; &quot; Treble &quot; e &quot; volume &quot; per restituire il valore nominale anziché l'impostazione corrente.</td>
</tr>
<tr class="odd">
<td>frequenza fotogrammi nominale</td>
<td>Restituisce la frequenza dei fotogrammi nominale associata al file. Le unità sono in frame al secondo moltiplicate per 1000.</td>
</tr>
<tr class="even">
<td>frequenza fotogrammi record nominale</td>
<td>Restituisce la frequenza di fotogrammi nominale associata al segnale video di input. Le unità sono in frame al secondo moltiplicate per 1000.</td>
</tr>
<tr class="odd">
<td>numero di tracce audio</td>
<td>Restituisce il numero di tracce audio sul supporto.</td>
</tr>
<tr class="even">
<td>numero di tracce</td>
<td>Restituisce il numero di tracce sui supporti. I dispositivi MCISEQ e MCIWAVE restituiscono 1, come per la maggior parte dei dispositivi VCR. Il dispositivo MCIPIONR non supporta questo flag.</td>
</tr>
<tr class="odd">
<td>numero di tracce video</td>
<td>Restituisce il numero di tracce video sui supporti.</td>
</tr>
<tr class="even">
<td>offset</td>
<td>Restituisce l'offset di un file basato su SMPTE. L'offset è l'ora di inizio di una sequenza basata su SMPTE. L'ora viene restituita <em>come HH: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</td>
</tr>
<tr class="odd">
<td>output</td>
<td>Restituisce l'output attualmente impostato. Se non è impostato alcun output, l'errore restituito indica che è possibile usare qualsiasi dispositivo. Per i dispositivi digitali video, modifica il &quot; &quot; flag Bass, &quot; Treble &quot; , &quot; volume &quot; , &quot; luminosità &quot; , &quot; colore &quot; , &quot; contrasto &quot; , &quot; gamma &quot; , &quot; nitidezza &quot; o &quot; tinta, &quot; in modo che venga applicato solo all'output. Si tratta dell'impostazione predefinita durante il monitoraggio di un file.</td>
</tr>
<tr class="even">
<td>modalità di sospensione</td>
<td>Restituisce &quot; &quot; la registrazione se il dispositivo viene sospeso durante la registrazione. Restituisce &quot; la riproduzione &quot; se il dispositivo viene sospeso durante la riproduzione. Restituisce l' &quot; azione di errore non applicabile nella modalità corrente &quot; se il dispositivo non è sospeso.</td>
</tr>
<tr class="odd">
<td>timeout pausa</td>
<td>Restituisce la durata massima, in millisecondi, di un comando di <a href="pause.md"><strong>sospensione</strong></a> .</td>
</tr>
<tr class="even">
<td>formato di riproduzione</td>
<td>Restituisce un codice che indica il formato in cui verrà riprodotto il nastro, se rilevabile: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; o &quot; altro &quot; . Per ulteriori informazioni, vedere il &quot; flag del formato di record &quot; .</td>
</tr>
<tr class="odd">
<td>velocità di riproduzione</td>
<td>Restituisce un valore che rappresenta la precisione del tempo di riproduzione effettivo dell'ultima sequenza AVI corrispondente al tempo di riproduzione di destinazione. Il valore 1000 indica che l'ora di destinazione e l'ora effettiva sono uguali. Il valore 2000, ad esempio, indicherebbe che la sequenza AVI ha richiesto due volte la riproduzione del tempo necessario. Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI. È destinato solo alla valutazione delle prestazioni. il valore restituito è difficile da interpretare.</td>
</tr>
<tr class="even">
<td>port</td>
<td>Restituisce il numero di porta MIDI assegnato alla sequenza.</td>
</tr>
<tr class="odd">
<td>position</td>
<td>Restituisce la posizione corrente. Per i file PPQN, la posizione viene restituita nelle unità del puntatore del brano. Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, SS è seconds e <em>FF</em> è frames.<br/></td>
</tr>
<tr class="even">
<td>inizio posizione</td>
<td>Restituisce la posizione dell'inizio del supporto utilizzabile.</td>
</tr>
<tr class="odd">
<td><em>numero</em> di traccia posizione</td>
<td>Restituisce la posizione dell'inizio della traccia specificata dal <em>numero</em>. Per i file PPQN, il formato dell'ora viene restituito nelle unità del puntatore del brano. Per i file SMPTE, viene restituito come <em>hh: mm: SS: FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames. MCISEQ Sequencer restituisce zero. Il dispositivo MCIPIONR non supporta questo flag. Il dispositivo MCIWAVE restituisce zero.</td>
</tr>
<tr class="even">
<td>durata postroll</td>
<td>Restituisce la lunghezza del nastro, nel formato ora corrente, necessario per bloccare il trasporto del videoregistratore quando viene emesso un comando di <a href="stop.md"><strong>arresto</strong></a> o <a href="pause.md"><strong>sospensione</strong></a> .</td>
</tr>
<tr class="odd">
<td>accensione</td>
<td>Restituisce <strong>true</strong> se l'alimentazione del VCR è accesa.</td>
</tr>
<tr class="even">
<td>durata preroll</td>
<td>Restituisce la lunghezza del nastro, nel formato dell'ora corrente, necessario per stabilizzare l'output del videoregistratore.</td>
</tr>
<tr class="odd">
<td>pronto</td>
<td>Restituisce <strong>true</strong> se il dispositivo è pronto per accettare un altro comando.</td>
</tr>
<tr class="even">
<td>formato record</td>
<td>Restituisce un codice che indica il formato in cui verrà registrato il nastro. I tipi restituiti correnti sono &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; o &quot; other &quot; . Questi formati non sono specifici di VHS e possono essere applicati a qualsiasi VCR con più formati di registrazione selezionabili. Il &quot; &quot; tipo SP è il formato di registrazione più veloce e di alta qualità e viene usato come impostazione predefinita nel VCR con singolo formato.</td>
</tr>
<tr class="odd">
<td>frequenza fotogrammi record</td>
<td>Restituisce la frequenza dei fotogrammi, in frame al secondo moltiplicata per 1000, utilizzata per la compressione.</td>
</tr>
<tr class="even">
<td><em>frame</em> di riferimento</td>
<td>Restituisce il numero di frame per l'immagine del fotogramma chiave più vicina che precede il <em>frame</em>specificato.</td>
</tr>
<tr class="odd">
<td>dimensioni riservate</td>
<td>Restituisce la dimensione, nel formato dell'ora corrente, dell'area di lavoro riservata. Le dimensioni corrispondono al tempo approssimativo necessario per riprodurre i dati compressi da un'area di lavoro completa. Restituisce zero se non è disponibile spazio su disco riservato. Questo flag restituisce le dimensioni approssimative perché lo spazio su disco preciso per i dati compressi non può essere stimato, in generale, fino a quando i dati non sono stati compressi.</td>
</tr>
<tr class="even">
<td>volume giusto</td>
<td>Restituisce il set di volumi per il canale audio destro.</td>
</tr>
<tr class="odd">
<td>samplespersec</td>
<td>Restituisce il numero di campioni al secondo riprodotti o registrati.</td>
</tr>
<tr class="even">
<td>ricerca esatta</td>
<td>Restituisce &quot; on &quot; o &quot; off &quot; , che indica se &quot; è impostato il flag Seek exactly &quot; .</td>
</tr>
<tr class="odd">
<td>nitidezza</td>
<td>Restituisce il livello di nitidezza corrente del dispositivo.</td>
</tr>
<tr class="even">
<td>lato</td>
<td>Restituisce 1 o 2 per indicare quale lato di videodisco è caricato.</td>
</tr>
<tr class="odd">
<td>schiavo</td>
<td>Restituisce &quot; file &quot; , &quot; MIDI &quot; , &quot; None &quot; o &quot; SMPTE, &quot; a seconda del tipo di set di sincronizzazione.</td>
</tr>
<tr class="even">
<td>SMPTE</td>
<td>Restituisce il timecode SMPTE associato alla posizione corrente nell'area di lavoro. Si tratta di una stringa nel formato <em>GG: DD: DD</em>: DD, dove ogni <em>d</em> indica una cifra da 0 a 9. Se i dati dell'area di lavoro non includono i dati del timecode, questo flag restituisce 00:00:00:00.</td>
</tr>
<tr class="odd">
<td>velocità</td>
<td>Restituisce la velocità corrente del dispositivo in frame al secondo (o nello stesso formato utilizzato dal comando <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot; Speed &quot; ). Il lettore videodisco MCIPIONR non supporta questo flag.</td>
</tr>
<tr class="even">
<td>posizione iniziale</td>
<td>Restituisce la posizione iniziale del supporto.</td>
</tr>
<tr class="odd">
<td>formato file ancora</td>
<td>Restituisce il formato di file corrente per il comando di <a href="capture.md"><strong>acquisizione</strong></a> .</td>
</tr>
<tr class="even">
<td>adattamento</td>
<td>Restituisce <strong>true</strong> se l'estensione è abilitata.</td>
</tr>
<tr class="odd">
<td>tempo</td>
<td>Restituisce il tempo corrente di una sequenza MIDI nel formato dell'ora corrente. Per i file con formato PPQN, il tempo è in battute al minuto. Per i file con formato SMPTE, il tempo è in frame al secondo.</td>
</tr>
<tr class="even">
<td>formato dell'ora</td>
<td>Restituisce il formato dell'ora corrente. Per ulteriori informazioni, vedere i formati di ora nel comando <a href="set.md"><strong>set</strong></a> .</td>
</tr>
<tr class="odd">
<td>modalità ora</td>
<td>Restituisce la modalità temporale di posizione corrente. Può essere &quot; Detect &quot; , &quot; timecode &quot; o &quot; Counter &quot; .</td>
</tr>
<tr class="even">
<td>tipo Time</td>
<td>Restituisce il tempo di posizione corrente in uso: &quot; timecode &quot; o &quot; contatore &quot; .</td>
</tr>
<tr class="odd">
<td>codice temporale presente</td>
<td>Restituisce <strong>true</strong> se il codice temporale è stato registrato nella posizione corrente sul nastro. Il codice temporale deve avanzare dalla posizione corrente. Potrebbe essere necessario riprodurre un VCR per verificare questa condizione.</td>
</tr>
<tr class="even">
<td>record timecode</td>
<td>Restituisce <strong>true</strong> se il VCR è impostato in modo da registrare il codice temporale.</td>
</tr>
<tr class="odd">
<td>tipo di timecode</td>
<td>Restituisce &quot; SMPTE &quot; , &quot; SMPTE Drop &quot; , &quot; other &quot; o &quot; None &quot; . Si noti che i frame al secondo possono essere ottenuti dal &quot; comando della frequenza dei fotogrammi di stato &quot; e l'accuratezza del dispositivo può essere restituita dal comando <a href="capability.md"><strong>Capability</strong></a> &quot; Seek accuratezza &quot; .</td>
</tr>
<tr class="even">
<td>tinta</td>
<td>Restituisce il livello di tinta del video corrente.</td>
</tr>
<tr class="odd">
<td>acuti</td>
<td>Restituisce il livello audio-acuti corrente.</td>
</tr>
<tr class="even">
<td>numero Tuner</td>
<td>Restituisce il numero del sintonizzatore logico corrente.</td>
</tr>
<tr class="odd">
<td>unsaved</td>
<td>Restituisce <strong>true</strong> se nell'area di lavoro sono presenti dati registrati che potrebbero andare perduti a seguito di un comando <a href="close.md"><strong>Close</strong></a>, <a href="load.md"><strong>Load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>Reserve</strong></a>, <a href="cut.md"><strong>Cut</strong></a>, <a href="delete.md"><strong>Delete</strong></a>o <a href="paste.md"><strong>paste</strong></a> . In caso contrario, restituisce <strong>false</strong> .</td>
</tr>
<tr class="even">
<td>Video</td>
<td>Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato impostato dal comando <a href="setvideo.md"><strong>sevideo</strong></a> .</td>
</tr>
<tr class="odd">
<td>colore della chiave video</td>
<td>Restituisce il valore per il colore della chiave.</td>
</tr>
<tr class="even">
<td>indice chiave video</td>
<td>Restituisce il valore per l'indice della chiave.</td>
</tr>
<tr class="odd">
<td>monitoraggio video</td>
<td>Restituisce &quot; &quot; l'output o uno dei tipi di input di origine validi. Per ulteriori informazioni, vedere il comando <a href="setvideo.md"><strong>sevideo</strong></a> &quot; Monitor &quot; .</td>
</tr>
<tr class="even">
<td>numero di monitor video</td>
<td>Restituisce il numero del video monitorato del tipo restituito dal &quot; monitoraggio video di stato &quot; . Per ulteriori informazioni, vedere il comando <a href="setvideo.md">sevideo</a> .</td>
</tr>
<tr class="odd">
<td>record video</td>
<td>Restituisce &quot; on &quot; o &quot; off &quot; , che riflette lo stato corrente impostato dal record <a href="setvideo.md"><strong>sevideo</strong></a> &quot; &quot; .</td>
</tr>
<tr class="even">
<td><em>numero</em> di traccia del record video</td>
<td>Restituisce <strong>true</strong> se il VCR è impostato per registrare il video. Se non viene specificato alcun numero di traccia, viene utilizzato il valore predefinito 1.</td>
</tr>
<tr class="odd">
<td>origine video</td>
<td>Restituisce il tipo di origine video. Per ulteriori informazioni, vedere il comando <a href="setvideo.md"><strong>sevideo</strong></a> .</td>
</tr>
<tr class="even">
<td>numero di origine video</td>
<td>Restituisce un numero corrispondente all'origine video del tipo in uso. Ad esempio, restituisce 2 Se viene usato il secondo input di origine video NTSC.</td>
</tr>
<tr class="odd">
<td>flusso video</td>
<td>Restituisce il numero corrente del flusso video.</td>
</tr>
<tr class="even">
<td>volume</td>
<td>Restituisce il volume medio all'altoparlante sinistro e destro. Viene restituito un errore se il dispositivo non è stato riprodotto o il volume non è stato impostato.</td>
</tr>
<tr class="odd">
<td>handle finestra</td>
<td>Restituisce il valore decimale ASCII per l'handle di finestra nella parola di basso livello del valore restituito.</td>
</tr>
<tr class="even">
<td>finestra ingrandita</td>
<td>Restituisce <strong>true</strong> se la finestra è ingrandita.</td>
</tr>
<tr class="odd">
<td>finestra ridotta a icona</td>
<td>Restituisce <strong>true</strong> se la finestra è ridotta a icona.</td>
</tr>
<tr class="even">
<td>finestra visibile</td>
<td>Restituisce <strong>true</strong> se la finestra non è nascosta.</td>
</tr>
<tr class="odd">
<td>scrittura protetta</td>
<td>Restituisce <strong>true</strong> se il dispositivo rileva che non è in grado di registrare, ovvero se la protezione da scrittura è impostata su on. Se può registrare o se non è in grado di determinare se può registrare o meno (senza scrivere effettivamente), il driver restituisce <strong>false</strong>.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le informazioni nel parametro *lpszReturnString* di [**mciSendString**](/previous-versions//dd757161(v=vs.85)). Le informazioni dipendono dal tipo di richiesta.

## <a name="remarks"></a>Commenti

Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .

## <a name="examples"></a>Esempio

Il seguente comando restituisce la modalità corrente del dispositivo "audio".

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

[catturare](capture.md)
</dt> <dt>

[close](close.md)
</dt> <dt>

[tagliare](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[carico](load.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Incolla](paste.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[riserva](reserve.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[video](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> <dt>

[cancella](undo.md)
</dt> </dl>

 

