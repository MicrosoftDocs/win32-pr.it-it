---
title: imposta comando
description: Il comando set stabilisce le impostazioni di controllo per il dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- impostazione del comando Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320056"
---
# <a name="set-command"></a>imposta comando

> [!NOTE]
> Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.  Questo testo viene usato in quanto è attualmente il testo usato nei comandi. Per coerenza, questo documento contiene questa parola. Quando questa parola viene modificata nei comandi, il documento verrà corretto in modo da essere in allineamento.


Il comando set stabilisce le impostazioni di controllo per il dispositivo. CD audio, Digital-video, MIDI sequencer, VCR, videodisco, video-overlay e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*
</dt> <dd>

Flag per la definizione delle impostazioni di controllo. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **set** e i flag utilizzati da ogni tipo.



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
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>millisecondi formato ora</li>
<li>formato ora MSF</li>
<li>formato ora TMSF</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li><em>formato</em> formato file</li>
<li>Cerca esattamente in</li>
<li>Cerca esattamente fuori</li>
<li><em>fattore</em> di velocità</li>
<li><em>formato</em> file ancora</li>
<li>frame formato ora</li>
<li>millisecondi formato ora</li>
<li>video disattivato</li>
<li>video su</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>video disattivato</li>
<li>video su</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>MIDI Master</li>
<li>nessuno Master</li>
<li>SMPTE Master</li>
<li><em>tempo</em> di offset</li>
<li>Mapper porta</li>
<li>Nessuna porta</li>
<li><em>port_number</em> porta</li>
<li>file slave</li>
<li>MIDI slave</li>
<li>slave None</li>
<li>SMPTE slave</li>
<li><em>tempo_value</em> tempo</li>
<li>millisecondi formato ora</li>
<li>formato ora SMPTE <em>fps</em></li>
<li>formato ora SMPTE 30 drop</li>
<li>puntatore al formato dell'ora</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>VCR</strong></td>
<td><ul>
<li>assembla record su</li>
<li>assembla record disattivato</li>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li><em>ora</em> di clock</li>
<li>formato contatore</li>
<li><em>valore</em> contatore</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>contatore indice</li>
<li>Data di indice</li>
<li>tempo di indicizzazione</li>
<li>tempo di indicizzazione</li>
<li><em>durata</em> CodeLength</li>
<li><em>timeout</em> pausa</li>
<li>durata postroll-</li>
<li><em>duration</em></li>
<li>accensione</li>
<li>spegnimento</li>
<li><em>durata</em> della preregistrazione</li>
<li>SP formato record</li>
<li>formato record LP</li>
<li>formato record EP</li>
<li><em>fattore</em> di velocità</li>
<li>frame formato ora</li>
<li>formato ora HMS</li>
<li>millisecondi formato ora</li>
<li>formato ora MSF</li>
<li>formato ora SMPTE <em>fps</em></li>
<li>formato ora SMPTE 30 drop</li>
<li>formato ora TMSF</li>
<li>contatore modalità ora</li>
<li>rilevamento modalità tempo</li>
<li>timecode modalità ora</li>
<li>rilevamento e</li>
<li>meno rilevamento</li>
<li>rilevamento reimpostazione</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>frame formato ora</li>
<li>formato ora HMS</li>
<li>millisecondi formato ora</li>
<li>traccia formato ora</li>
<li>video disattivato</li>
<li>video su</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li><em>Integer</em> allineamento</li>
<li>qualsiasi input</li>
<li>qualsiasi output</li>
<li>audio tutto disattivato</li>
<li>audio tutto su</li>
<li>Audio interrotto</li>
<li>audio lasciato acceso</li>
<li>audio a destra</li>
<li>audio a destra</li>
<li><em>bit_count</em> BitsPerSample</li>
<li><em>byte_rate</em> bytespersec</li>
<li>canali <em>channel_count</em></li>
<li>sportello chiuso</li>
<li>sportello aperto</li>
<li>formato PCM Tag</li>
<li><em>tag</em> di formato tag</li>
<li><em>Integer</em> di input</li>
<li><em>intero</em> di output</li>
<li>samplespersec <em>Integer</em></li>
<li>byte formato ora</li>
<li>millisecondi formato ora</li>
<li>esempi di formato time</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszSetting** e i relativi significati.



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
<td><em>Integer</em> allineamento</td>
<td>Imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati passati al dispositivo Waveform-Audio. Il file viene salvato in questo formato.</td>
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
<td>assembla record su <br/> assembla record disattivato <br/></td>
<td>In modalità assembla tutte le tracce vengono registrate come definito dal dispositivo. Per impostazione predefinita, la maggior parte dei VCR è in modalità assembler.</td>
</tr>
<tr class="odd">
<td>audio tutto disattivato <br/> audio tutto su <br/></td>
<td>Disabilita o Abilita l'output audio. I dispositivi overlay video, MCISEQ sequencer e MCIWAVE Waveform-Audio Device non supportano questo flag.</td>
</tr>
<tr class="even">
<td>Audio interrotto <br/> audio lasciato acceso <br/> audio a destra <br/> audio a destra <br/></td>
<td>Disabilita o Abilita l'output sul canale audio a sinistra o a destra. I dispositivi overlay video, MCISEQ sequencer e MCIWAVE Waveform-Audio Device non supportano questo flag.</td>
</tr>
<tr class="odd">
<td><em>bit_count</em> BitsPerSample</td>
<td>Imposta il numero di bit per PCM (Pulse Code Modulation) campione riprodotto o registrato. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td><em>byte_rate</em> bytespersec</td>
<td>Imposta il numero medio di byte al secondo riprodotti o registrati. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td>canali <em>channel_count</em></td>
<td>Imposta i canali per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td><em>ora</em> di clock</td>
<td>Imposta l'ora sul clock esterno per il <em>tempo.</em> Il formato è specificato come Long Unsigned Integer.</td>
</tr>
<tr class="odd">
<td>formato contatore</td>
<td>Imposta il formato dell'ora per il contatore, come restituito dal contatore di <a href="status.md">stato</a> &quot; &quot; . Per informazioni sui tipi applicabili, vedere il comando <strong>set</strong> &quot; Time Format &quot; .</td>
</tr>
<tr class="even">
<td><em>valore</em> contatore</td>
<td>Imposta il contatore VCR sul valore specificato. Il valore deve essere specificato nel formato del contatore corrente. Per ulteriori informazioni, vedere il comando <strong>imposta</strong> &quot; formato contatore &quot; .</td>
</tr>
<tr class="odd">
<td>sportello chiuso</td>
<td>Ritrae la barra e chiude la porta, se possibile. Per i VCR, carica il nastro automaticamente.</td>
</tr>
<tr class="even">
<td>sportello aperto</td>
<td>Apre lo sportello ed espelle la barra o il nastro, se possibile.</td>
</tr>
<tr class="odd">
<td><em>formato</em> formato file</td>
<td>Specifica un formato di file utilizzato per i comandi di <a href="save.md">salvataggio</a> o <a href="capture.md">acquisizione</a> . Se omesso, per impostazione predefinita è possibile che sia un formato definito dal driver di dispositivo. Se il formato di file specificato è in conflitto con l'algoritmo e la qualità attualmente selezionati, verranno modificati nei valori predefiniti per il formato di file. Sono definiti i formati di file seguenti:
<ul>
<li>AVI: specifica il formato AVI.</li>
<li>avss: specifica il formato di AVSS.</li>
<li>DIB: specifica il formato DIB.</li>
<li>JFIF: specifica il formato di JFIF.</li>
<li>JPEG: specifica il formato JPEG.</li>
<li>MPEG: specifica il formato MPEG.</li>
<li>rdib: specifica il formato DIB di RLE.</li>
<li>rjpeg: specifica il formato di RJPEG.</li>
</ul></td>
</tr>
<tr class="even">
<td>formato PCM Tag</td>
<td>Imposta il tipo di formato su PCM per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td><em>tag</em> di formato tag</td>
<td>Imposta il tipo di formato per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="even">
<td>codice temporale indice <br/> contatore indice <br/> Data di indice <br/> tempo di indicizzazione <br/></td>
<td>Imposta la schermata di visualizzazione corrente sul videoregistratore.</td>
</tr>
<tr class="odd">
<td><em>Integer</em> di input</td>
<td>Imposta il canale audio utilizzato come input.</td>
</tr>
<tr class="even">
<td><em>durata</em> lunghezza</td>
<td>Imposta la lunghezza del nastro specificata dall'utente nel VCR. Questa lunghezza viene restituita dal comando di lunghezza <a href="status.md">dello stato</a> &quot; &quot; e viene fornita per la compatibilità con le applicazioni che richiedono che questo comando restituisca una lunghezza valida.</td>
</tr>
<tr class="odd">
<td>MIDI Master</td>
<td>Imposta il sequencer MIDI come origine della sincronizzazione. I dati di sincronizzazione vengono inviati in formato MIDI. MCISEQ sequencer non supporta questo flag.</td>
</tr>
<tr class="even">
<td>nessuno Master</td>
<td>Impedisce al sequencer MIDI di inviare i dati di sincronizzazione. MCISEQ sequencer non supporta questo flag.</td>
</tr>
<tr class="odd">
<td>SMPTE Master</td>
<td>Imposta il sequencer MIDI come origine della sincronizzazione. I dati di sincronizzazione vengono inviati in formato SMPTE (Society of Motion Picture and Television Engineers). MCISEQ sequencer non supporta questo flag.</td>
</tr>
<tr class="even">
<td><em>tempo</em> di offset</td>
<td>Imposta il <em>tempo</em>di offset SMPTE. L'offset è l'ora di inizio di una sequenza basata su SMPTE. Il <em>tempo</em> è espresso come <em>HH</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, dove <em>HH</em> è hours, <em>mm</em> è minutes, <em>SS</em> è seconds e <em>FF</em> è frames.</td>
</tr>
<tr class="odd">
<td><em>intero</em> di output</td>
<td>Imposta il canale audio utilizzato come output.</td>
</tr>
<tr class="even">
<td><em>timeout</em> pausa</td>
<td>Imposta la durata massima, in millisecondi, di un comando di <a href="pause.md">sospensione</a> . Un valore di <em>timeout</em> pari a zero indica che non si verificherà alcun timeout.</td>
</tr>
<tr class="odd">
<td><em>durata</em> della durata del postroll</td>
<td>Imposta la lunghezza, nel formato dell'ora corrente, necessaria per bloccare il trasporto del videoregistratore quando viene eseguito un comando di <a href="stop.md">arresto</a> o <strong>sospensione</strong> .</td>
</tr>
<tr class="even">
<td>Mapper porta</td>
<td>Imposta il mapper MIDI come la porta che riceve i messaggi MIDI. Questo comando non riesce se il mapper MIDI o una porta necessaria è usato da un'altra applicazione.</td>
</tr>
<tr class="odd">
<td>Nessuna porta</td>
<td>Disabilita l'invio di messaggi MIDI. Questo comando chiude anche una porta MIDI.</td>
</tr>
<tr class="even">
<td><em>port_number</em> porta</td>
<td>Imposta la porta MIDI che riceve i messaggi MIDI. Questo comando ha esito negativo se la porta che si sta tentando di aprire è utilizzata da un'altra applicazione.</td>
</tr>
<tr class="odd">
<td>accensione <br/> spegnimento <br/></td>
<td>Imposta l'alimentazione del dispositivo su on o off.</td>
</tr>
<tr class="even">
<td><em>durata</em> della preregistrazione</td>
<td>Imposta la lunghezza, nel formato dell'ora corrente, necessaria per stabilizzare l'output del VCR.</td>
</tr>
<tr class="odd">
<td>SP formato record <br/> formato record LP <br/> formato record EP <br/></td>
<td>Imposta la modalità di registrazione per il VCR su SP per la riproduzione standard, EP for Extended Play o LP per la riproduzione a lungo termine. Questi valori non sono destinati a essere specifici della VHS. Eseguono il mapping a tre modalità appropriate con altri formati di nastro. Ad esempio, SP esegue il mapping alla registrazione più veloce e di qualità superiore.</td>
</tr>
<tr class="even">
<td>samplespersec <em>Integer</em></td>
<td>Imposta la frequenza di campionamento per la riproduzione e la registrazione. Il file viene salvato in questo formato.</td>
</tr>
<tr class="odd">
<td>Cerca esattamente in<br/> Cerca esattamente fuori <br/></td>
<td>Seleziona una delle due modalità di ricerca. Con &quot; Seek exactly on &quot; , Seek viene sempre spostato nel frame specificato. Con la &quot; ricerca esatta &quot; , la ricerca viene spostata nel fotogramma chiave più vicino prima del frame specificato.</td>
</tr>
<tr class="even">
<td>file slave</td>
<td>Imposta MIDI sequencer in modo che utilizzi i dati dei file come origine della sincronizzazione. Si tratta dell'impostazione predefinita.</td>
</tr>
<tr class="odd">
<td>MIDI slave</td>
<td>Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato MIDI. MCISEQ sequencer non supporta questo flag.</td>
</tr>
<tr class="even">
<td>slave None</td>
<td>Imposta il sequencer MIDI per ignorare la sincronizzazione</td>
</tr>
<tr class="odd">
<td>SMPTE slave</td>
<td>Imposta il sequencer MIDI per l'uso dei dati MIDI in ingresso per l'origine di sincronizzazione. Sequencer riconosce i dati di sincronizzazione con il formato SMPTE. MCISEQ sequencer non supporta questo flag.</td>
</tr>
<tr class="even">
<td>fattore di velocità</td>
<td>Imposta la velocità relativa della riproduzione video e audio dall'area di lavoro. Factor è il rapporto tra la frequenza dei fotogrammi nominale e la frequenza dei fotogrammi desiderata, in cui la frequenza dei fotogrammi nominale viene designata come 1000. Una frequenza di 500 è la velocità della metà normale, 2000 è due volte la velocità normale e così via. Impostando la velocità su zero, il video viene riprodotto il più rapidamente possibile senza eliminare i frame e senza audio.</td>
</tr>
<tr class="odd">
<td><em>formato</em> file ancora</td>
<td>Specifica il formato di file utilizzato per i comandi di acquisizione.</td>
</tr>
<tr class="even">
<td>tempo_value tempo</td>
<td>Imposta il tempo della sequenza in base al formato dell'ora corrente. Per un file basato su PPQN, il tempo_value viene interpretato come un battito al minuto. Per un file basato su SMPTE, il tempo_value viene interpretato come frame al secondo.</td>
</tr>
<tr class="odd">
<td>byte formato ora</td>
<td>In un formato di file PCM, imposta il formato dell'ora su byte. Tutte le informazioni sulla posizione vengono specificate come byte dopo questo comando.</td>
</tr>
<tr class="even">
<td>frame formato ora</td>
<td>Imposta il formato dell'ora su frame. Tutti i comandi che usano valori di posizione presuppongono frame. Quando il dispositivo viene aperto, i frame sono la modalità predefinita. Supportato da videodischi con formato CAV.</td>
</tr>
<tr class="odd">
<td>formato ora HMS</td>
<td>Imposta il formato dell'ora su ore, minuti e secondi. Tutti i comandi che usano i valori di posizione presuppongono la funzione HMS. HMS è il formato predefinito per CLV videodischi. Specificare un valore HMS come HH: mm: SS, dove HH è hours, mm è minutes e SS è seconds. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono tutti modi validi per esprimere 3 ore. <br/></td>
</tr>
<tr class="even">
<td>millisecondi formato ora</td>
<td>Imposta il formato dell'ora su millisecondi. Per tutti i comandi che usano valori di posizione si presuppone un millisecondo. È possibile abbreviare i millisecondi come &quot; MS &quot; . Per i dispositivi sequencer, il file di sequenza imposta il formato predefinito su PPQN o SMPTE. I dispositivi overlay video non supportano questo flag.<br/></td>
</tr>
<tr class="odd">
<td>formato ora MSF</td>
<td>Imposta il formato dell'ora su minuti, secondi e frame. Per tutti i comandi che usano valori di posizione si presuppone MSF (il formato predefinito per audio CD). Specificare un valore MSF come mm: SS: FF, dove mm è minutes, SS è seconds e FF è frames. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0 e 3:0:0 sono modi validi per esprimere 3 minuti.<br/> I campi MSF presentano i valori massimi seguenti:<br/>
<ul>
<li>Minuti 99</li>
<li>Secondi 59</li>
<li>Frame 74</li>
</ul></td>
</tr>
<tr class="even">
<td>esempi di formato time</td>
<td>Imposta il formato dell'ora sugli esempi. Tutte le informazioni sulla posizione vengono specificate come campioni che seguono questo comando.</td>
</tr>
<tr class="odd">
<td>formato ora SMPTE 24<br/> formato ora SMPTE 25<br/> formato ora SMPTE 30<br/></td>
<td>Imposta il formato dell'ora su una frequenza dei fotogrammi SMPTE. Per i VCR, imposta il formato dell'ora su HH: mm: SS: FF, dove i valori validi sono compresi tra 00:00:00:00 e 23:59:59: XX, mentre XX è inferiore al numero di fotogrammi al secondo, come specificato dal numero 24, 25 o 30, come specificato nel flag. In input, i due punti (:) sono necessari per separare i componenti. Le unità meno significative possono essere omesse se sono 00; 02:00, ad esempio, corrisponde a 02:00:00:00. Tutti i comandi che usano valori di posizione presuppongono il formato SMPTE.<br/> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br/></td>
</tr>
<tr class="even">
<td>formato ora SMPTE 30 drop</td>
<td>Imposta il formato dell'ora su SMPTE 30 drop frame rate. Per i VCR, uguale a SMPTE 30, con la differenza che alcune posizioni del timecode vengono eliminate dal formato in modo che le posizioni del timecode registrate per ogni fotogramma (alla frequenza dei fotogrammi NTSC di 29,97 fps) corrispondano a tempo reale (a 30 fps). Le posizioni del timecode eliminate sono le seguenti: due al minuto, per i primi nove di ogni dieci minuti di contenuto registrato. Ad esempio, alle 01:04:59:29, la posizione del timecode successiva sarà 01:05:00:02, non 01:05:00:00. Tutti i comandi che usano valori di posizione presuppongono il formato SMPTE.<br/> Il file di sequenza imposta il formato predefinito su PPQN o SMPTE.<br/></td>
</tr>
<tr class="odd">
<td>puntatore al formato dell'ora</td>
<td>Imposta il formato dell'ora su puntatore al brano (sedicesimi). Per tutti i comandi che usano valori di posizione si presuppone che le unità del puntatore del brano. Questo flag è valido solo per una sequenza di tipo PPQN di divisione.</td>
</tr>
<tr class="even">
<td>formato ora TMSF</td>
<td>Imposta il formato dell'ora su Tracks, minutes, seconds e frames. Per tutti i comandi che usano valori di posizione si presuppone TMSF. Specificare un valore TMSF come TT: mm: SS: FF, dove TT è Tracks, mm è minutes, SS is seconds e FF is frames. È possibile omettere un campo se e tutti i campi seguenti sono pari a zero. Ad esempio, 3, 3:0, 3:0:0 e 3:0:0:0 sono tutti modi validi per esprimere Track 3. <br/> I campi TMSF hanno i valori massimi seguenti:<br/>
<ul>
<li>Tracce 99</li>
<li>Minuti 90</li>
<li>Secondi 59</li>
<li>Frame 74</li>
</ul></td>
</tr>
<tr class="odd">
<td>traccia formato ora</td>
<td>Imposta il formato di posizione su Tracks. Tutti i comandi che usano valori di posizione presuppongono le tracce.</td>
</tr>
<tr class="even">
<td>contatore modalità ora</td>
<td>Imposta la modalità position-Information per l'uso dei contatori VCR.</td>
</tr>
<tr class="odd">
<td>rilevamento modalità tempo</td>
<td>Imposta la modalità informazioni sulla posizione in base al rilevamento delle informazioni sul timecode sul nastro. Se vengono rilevate informazioni sul timecode, il tipo di ora è impostato su &quot; timecode &quot; ; in caso contrario, il tipo di ora è impostato su &quot; Counter &quot; . &quot;&quot;Il rilevamento è una modalità speciale. Ogni volta che il driver viene aperto, viene inserito un nuovo nastro o &quot; viene eseguito il comando della modalità ora &quot; , il driver controlla la modalità ora corrente disponibile sul nastro e imposta il &quot; tipo di ora sul &quot; &quot; timecode &quot; o sul &quot; contatore &quot; . Una volta &quot; &quot; impostato il tipo time, il driver non lo modifica fino a quando non si verifica una delle condizioni precedenti.<br/></td>
</tr>
<tr class="even">
<td>timecode modalità ora</td>
<td>Imposta la modalità informazioni sulla posizione per utilizzare le &quot; &quot; informazioni sul timecode sul nastro.</td>
</tr>
<tr class="odd">
<td>rilevamento e <br/> meno rilevamento <br/> rilevamento reimpostazione <br/></td>
<td>Regola la velocità del trasporto di nastri in incrementi. Usare i &quot; &quot; flag di rilevamento quando si ottiene un'immagine rumorosa da un videoregistratore. &quot;Il rilevamento e &quot; la velocità di trasporto aumentano. &quot;Il rilevamento meno &quot; diminuisce la velocità del trasporto. &quot;La reimpostazione &quot; del rilevamento restituisce zero per la regolazione del rilevamento.</td>
</tr>
<tr class="even">
<td>video disattivato</td>
<td>Disabilita l'output del video.</td>
</tr>
<tr class="odd">
<td>video su</td>
<td>Abilita l'output del video.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Quando viene creato il file in cui archiviare i dati, vengono definite diverse proprietà dei dati audio della forma d'onda. Queste proprietà descrivono la struttura dei dati all'interno del file e non possono essere modificate una volta avviata la registrazione. L'elenco seguente identifica queste proprietà:

-   allineamento
-   BitsPerSample
-   bytespersec
-   channels
-   Tag di formato
-   samplespersec

## <a name="examples"></a>Esempio

Il seguente comando imposta il formato dell'ora su millisecondi e imposta il formato dell'audio della forma d'onda su 8 bit, mono, 11 kHz.

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[catturare](capture.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

