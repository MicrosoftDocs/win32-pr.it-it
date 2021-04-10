---
title: Servizi VCR
description: Servizi VCR
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Architettura del controllo del sistema video (VISCA)
- VISCA (architettura di controllo del sistema video)
- Driver VISCA MCI
- Driver VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d884c38d224182db7eef8db0f0cd80b14e3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856550"
---
# <a name="vcr-services"></a>Servizi VCR

Windows fornisce servizi VCR tramite un driver di dispositivo basato sul set di comandi MCI per i VCR. In questa sezione viene descritto il driver VISCA (video System Control Architecture) MCI e viene illustrato come utilizzarlo per controllare un videoregistratore.

Il tipo di dispositivo *VCR* controlla i VCR. Per un elenco dei comandi MCI riconosciuti dai dispositivi VCR, vedere [set](vcr-command-set.md)di comandi VCR.

## <a name="the-mci-visca-driver"></a>Driver VISCA MCI

Il driver VISCA MCI Controlla i VCR compatibili con Sony VISCA, ad esempio CVD-1000 VDeck. Il driver VISCA controlla il trasporto del nastro, i sintonizzatori del canale e i canali di input e di output VCR.

## <a name="searching-and-positioning-with-a-vcr"></a>Ricerca e posizionamento con un VCR

Il driver VISCA usa due metodi per tenere traccia del movimento del nastro all'interno del nastro VCR: *informazioni sul timecode* e *contatori dei nastri*. Le informazioni sul timecode sono informazioni sulla temporizzazione registrate nel nastro. La maggior parte dei VCR consente la registrazione dei timecode senza eliminare le tracce audio e video. I contatori di nastri stimano la quantità di nastri che si spostano oltre la testa della cassetta per ottenere una posizione.

Le informazioni sul timecode e i contatori nastro aumentano quando il nastro si sposta dall'inizio alla fine. A causa dell'accuratezza, l'uso delle informazioni del timecode per posizionare un nastro è quasi sempre preferibile all'uso dei contatori di nastri.

I flag di comando MCI per specificare le informazioni sul posizionamento sono espressi come dipendenze temporali: "formato ora", "durata", "da", "a" e "seek". Inoltre, il comando "position" [**dello stato**](status.md) restituisce il relativo valore di ora nel formato dell'ora corrente.

Il driver VISCA usa il comando [**set**](set.md) "Time Mode" per selezionare il tipo di posizionamento da usare con un nastro. Quando la modalità ora è impostata su "timecode", i comandi **status** "position" e **set** "Time Format" usano il timecode sul nastro. Quando la modalità ora è impostata su "Counter", i comandi **status** "position" e **set** "Time Format" usano i contatori.

Un'applicazione può impostare la modalità temporale su "rileva" se non è importante che ci siano due origini di informazioni sulla posizione. In modalità di rilevamento, il driver VISCA usa le informazioni sul timecode per il posizionamento quando si verifica una delle condizioni seguenti:

-   Le informazioni sul timecode sono presenti al momento dell'apertura del driver.
-   Si modifica un nastro con il comando **imposta** "sportello aperto" e le informazioni sul timecode sono presenti nel nastro.
-   Il comando [**set**](set.md) "Time Mode" viene riemesso.

Se non è possibile trovare informazioni sul timecode, il driver usa i contatori del nastro.

Per determinare il metodo di posizionamento corrente, eseguire il comando [**stato**](status.md) "tipo di ora", che restituisce "timecode" o "contatore". È anche possibile identificare la modalità di posizionamento corrente usando il comando **status** "Time Mode", che restituisce "timecode", "Counter" o "Detect".

Il comando "contatore" **dello stato** Recupera il valore del contatore del nastro corrente, indipendentemente dal metodo di posizionamento corrente. Tuttavia, è possibile usare questo contatore solo con il comando [**set**](set.md) "Counter".

Il driver VISCA può recuperare il formato del timecode nativo registrato in un nastro **usando i comandi "tipo** di timecode" e "frequenza dei fotogrammi" **di stato insieme** . Ad esempio, se il tipo di codice temporale è "SMPTE" e la frequenza dei fotogrammi è 25, il formato del timecode nativo registrato sul nastro è SMPTE 25.

Il driver VISCA può anche recuperare la risoluzione del contatore usando il comando **stato** "contatore risoluzione", che restituisce "secondi" o "frame". Il formato del contatore potrebbe ancora essere impostato su SMPTE 30, ma il valore restituito restituisce solo un frame di 0. Se il tipo di ora corrente è Counter, questa risoluzione viene applicata anche al valore restituito dallo **stato** "position".

## <a name="capturing-frames"></a>Acquisizione di frame

I comandi di acquisizione frame forniscono ancora le immagini per un *dispositivo di acquisizione frame*. Un dispositivo di acquisizione frame è un componente hardware separato in grado di leggere e archiviare l'immagine del video. Il driver VISCA supporta il comando [**Freeze**](freeze.md) ([**MCI \_ Freeze**](mci-freeze.md)) per stabilizzare un'immagine ancora per l'acquisizione. Inoltre, è possibile utilizzare il comando Sblocca ([**MCI \_ Unfreeze**](mci-unfreeze.md)) per [**riavviare il trasporto**](unfreeze.md) del nastro dopo un comando **Freeze** .

Il comando **Freeze** fornisce un'immagine di alta qualità, stabilizzata e con correzione del tempo di base per un dispositivo di acquisizione frame. Questo comando esiste perché un dispositivo potrebbe non consegnare sempre l'immagine di output di qualità massima durante la riproduzione o durante la pausa; tale immagine video non è adatta per l'acquisizione.

Il comando **Unfreeze** Sblocca il trasporto del nastro e riprende la modalità di trasporto attiva prima del comando **Freeze** .

Quando l'applicazione deve registrare un'immagine video nel VCR, usare il comando **Freeze** "input" o [**cue**](cue.md) ([**MCI \_ cue**](mci-cue.md)) per registrare l'immagine.

## <a name="selecting-inputs"></a>Selezione degli input

Il driver VISCA supporta tre tipi di input: video, audio e timecode. Gli input video includono due canali standard (righe 1 e 2), un canale SVideo, un canale ausiliario e un canale da un sintonizzatore interno. Gli input audio includono due canali standard (righe 1 e 2) e un canale da un sintonizzatore interno. L'input del timecode è interno al videoregistratore.

Gli output normali contengono gli input attualmente selezionati quando il videoregistratore viene registrato o quando il trasporto del nastro viene interrotto e il contenuto del nastro viene registrato quando il trasporto del nastro viene riprodotto o sospeso. Gli output monitorati contengono le stesse informazioni degli output normali più le informazioni sul timecode e sul canale correnti.

Supponendo che gli input esterni appropriati siano connessi al videoregistratore ed è stato deciso che cosa si vuole registrare, è possibile selezionare gli input da registrare. Ad esempio, per registrare o visualizzare dal video "SVIDEO" e dagli input audio "line 1", è necessario utilizzare i comandi [**sevideo**](setvideo.md) ([**MCI \_ sevideo**](mci-setvideo.md)) e [**seaudio**](setaudio.md) ([**MCI \_ sefonica**](mci-setaudio.md)) per selezionare queste origini di input. È possibile verificare queste selezioni usando il comando [**stato**](status.md) ([**\_ stato MCI**](mci-status.md)).

Per impostazione predefinita, il monitoraggio Mostra esattamente cosa appare come output. In alcuni casi, tuttavia, potrebbe essere necessario visualizzare un'origine durante la registrazione di un altro. Si tratta di una pratica comune nell'uso del sintonizzatore. Ad esempio, si potrebbe voler guardare Channel 4 mentre si registra Channel 7. In questo caso, sono disponibili due input del sintonizzatore logico. È possibile configurare il VCR usando i comandi seguenti:

## <a name="to-review-one-source-while-recording-from-another"></a>Per esaminare un'origine durante la registrazione da un altro

1.  Usare il comando [**setuner**](settuner.md) ([**MCI \_ setuner**](mci-settuner.md)) per selezionare i canali da controllare e registrare.
2.  Usare il comando **sevideo** per selezionare l'origine di registrazione video.
3.  Usare il comando [**seaudio**](setaudio.md) per selezionare l'origine di registrazione audio.
4.  Usare il comando [**sevideo**](setvideo.md) per indirizzare l'input video di Channel 4 all'output monitorato per visualizzarlo sullo schermo.
5.  Usare il comando [**seaudio**](setaudio.md) per indirizzare l'input audio Channel 4 all'output monitorato per riprodurre l'audio.
6.  Verificare le selezioni tramite il comando [**status**](status.md) .

Il driver VISCA supporta anche un tipo di input speciale per audio e video, denominato *mute*. Il silenziamento consente la selezione di "nessun input", utile quando si registra un segnale vuoto.

## <a name="selecting-recording-tracks"></a>Selezione delle tracce di registrazione

In un nastro sono disponibili tre tipi di tracce di registrazione: video, audio e timecode. Si dispone solo di una traccia video o timecode, ma è possibile usare più di una traccia audio. Quando si esegue questa operazione, è necessario tenere traccia 1 della traccia audio principale.

Il driver VISCA supporta due modalità operative: assemblaggio e inserimento. In *modalità assembla* tutte le tracce vengono selezionate per la registrazione. In *modalità di inserimento*, le tracce possono essere selezionate in modo indipendente per la registrazione. Per impostazione predefinita, la maggior parte dei VCR è in modalità assembler. Usare il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) per modificare queste modalità.

## <a name="recording-and-editing"></a>Registrazione e modifica

Il comando [**record**](record.md) ([**\_ record MCI**](mci-record.md)) fornisce una registrazione semplice ed è preciso a circa 1 secondo della posizione iniziale. Per registrare in modo più accurato o se si prevede di modificare il contenuto video mentre si operano contemporaneamente più Deck, è necessario usare il comando [**cue**](cue.md) ([**MCI \_ cue**](mci-cue.md)).

Il comando **cue** prepara il dispositivo per la registrazione o la riproduzione. Usare il comando **cue** "input" per preparare il dispositivo per la registrazione. Il comando **cue** è obbligatorio perché un'applicazione deve essere in grado di stabilire quando il dispositivo è pronto per eseguire il comando (e perché la preparazione per un comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) o **record** potrebbe richiedere diversi minuti.

Il videoregistratore si prepara per la registrazione o la riproduzione cercando al *punto*, ovvero la posizione corrente o la posizione specificata tramite il comando **cue** "from". Se il flag "preroll" viene specificato con il comando **cue** , tuttavia, il VCR posiziona la distanza preroll dal punto di partenza. Il flag "preroll" indica anche che il VCR usa qualsiasi modalità di modifica applicabile, quindi è importante usare "preroll", soprattutto quando si desidera la registrazione più accurata. Usare il comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) con il flag "Can preroll" per verificare se la modalità di preroll è supportata.

> [!Note]  
> Quando si registra usando le posizioni "from" e "to", la posizione "from" è inclusa nella modifica e la posizione "to" non è.

 

Per ulteriori informazioni sulla registrazione, vedere [registrazione](recording.md).

## <a name="using-the-clock-while-editing"></a>Uso dell'orologio durante la modifica

Quando si modifica, potrebbe essere necessario registrare i segmenti da un videoregistratore a un altro. È possibile iniziare la registrazione in un momento specifico e in una posizione in un VCR mentre un'altra inizia a giocare nello stesso momento e nella stessa posizione specificando un'azione (riproduzione o record), una posizione e un'ora per ogni VCR.

Entrambi i VCR devono usare lo stesso clock per questo tipo di modifica; il clock consente di sincronizzare entrambi i dispositivi. È possibile determinare se due VCR condividono lo stesso clock usando il comando [**stato**](status.md) ([**\_ stato MCI**](mci-status.md)) con il flag "clock ID" per eseguire una query su ogni videoregistratore. Se i numeri di identificazione restituiti dal comando **status** sono uguali, i dispositivi usano lo stesso clock. Come risorsa condivisa, il clock può essere connesso a più VCR. Il driver VISCA supporta un solo Clock condiviso.

È anche possibile determinare la risoluzione del clock usando il comando **stato** "frequenza di incremento Clock". Questo comando restituisce il numero di incrementi supportati dal clock al secondo. Se, ad esempio, il clock viene aggiornato ogni millisecondo, il comando restituisce 1000 come frequenza di incremento dell'orologio. Il vantaggio dell'utilizzo della velocità di incremento è che la velocità è espressa come numero intero. in caso contrario, l'incremento è un valore a virgola mobile a precisione singola o doppia. Come Integer, la modifica della frequenza di incremento è un'operazione semplice e non è soggetta a errori di arrotondamento. È possibile reimpostare l'orologio usando il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) con il flag "Clock 0" (zero).

Quando si emette un comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**record**](record.md) ([**\_ record MCI**](mci-record.md)) o [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), è possibile specificare quando eseguire il comando. Le caratteristiche dei VCR utilizzati determinano quando avviare ogni VCR. L'intervallo deve tenere conto della quantità di preroll necessaria per ogni dispositivo e della quantità di tempo necessaria per completare i comandi MCI usati per configurare la sessione di modifica. A tale scopo, recuperare l'ora dell'orologio e aggiungere un intervallo di attesa compreso tra 5 e 10 secondi. L'intervallo di attesa deve essere sufficientemente lungo per consentire il completamento dell'esecuzione del preroll e di tutti i comandi MCI in sospeso.

Per assicurarsi che il periodo di attesa sia sufficiente, inserire il comando **record** per ultimo nell'applicazione e controllare l'ora immediatamente prima. Se l'intervallo è troppo breve, riavviare il comando **Play** . In alternativa, è possibile controllare l'ora immediatamente dopo l'ultimo comando dello script per verificare che sia disponibile tempo sufficiente per l'invio e il completamento di tutti i comandi.

 

 




