---
title: Servizi vcr
description: Servizi vcr
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Architettura di controllo del sistema video (VISCA)
- VISCA (Architettura di controllo del sistema video)
- Driver MCI VISCA
- Driver VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0397e56c589c357edc9e0be1999b51d358f8caced60117af5c20c7954a1edb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804521"
---
# <a name="vcr-services"></a>Servizi vcr

Windows fornisce servizi vcr tramite un driver di dispositivo basato sul set di comandi MCI per i videoregistratori. Questa sezione descrive il driver MCI Video System Control Architecture (VISCA) e spiega come usarlo per controllare un videoregistratore.

Il *tipo di dispositivo vcr* controlla i videoregistratori. Per un elenco dei comandi MCI riconosciuti dai dispositivi VCR, vedere [Set di comandi vcr](vcr-command-set.md).

## <a name="the-mci-visca-driver"></a>The MCI VISCA Driver

Il driver MCI VISCA controlla i videoregistratori compatibili con ViSCA di Sony, ad esempio il VDeck CVD-1000. Il driver VISCA controlla il trasporto su nastro, i silezionatori dei canali e i canali di input e output del videoregistratore.

## <a name="searching-and-positioning-with-a-vcr"></a>Ricerca e posizionamento con un videoregistratore

Il driver VISCA usa due metodi per tenere traccia dello spostamento di videocassetta all'interno del trasporto nastro vcr: informazioni sul *codice* temporale e *contatori dei nastri.* Le informazioni sul codice temporale sono informazioni di temporizzazione registrate nella videotape. La maggior parte dei videoregistratori consente di registrare i codici temporali senza eliminare le tracce audio e video. I contatori dei nastri stimano la quantità di videocassetta che passa oltre la testa della videocassetta per ottenere una posizione.

Le informazioni sul codice temporale e i contatori dei nastri aumentano quando la videocassetta passa dall'inizio alla fine. A causa della precisione, l'uso delle informazioni sul codice temporale per posizionare una videocassetta è quasi sempre preferibile all'uso dei contatori dei nastri.

I flag di comando MCI per specificare le informazioni di posizionamento sono espressi come dipendenze temporiche: "time format", "duration", "from", "to" e "seek". Inoltre, il [**comando**](status.md) "position" di stato restituisce il relativo valore di ora nel formato di ora corrente.

Il driver VISCA usa [**il comando set**](set.md) "time mode" per selezionare il tipo di posizionamento da usare con una videotape. Quando la modalità temporale è impostata su "timecode", i comandi **status** "position" e **set** "time format" usano il codice temporale nella videotape. Quando la modalità temporale è impostata su "counter", i comandi **di** stato "position" e **set** "time format" usano i contatori.

Un'applicazione può impostare la modalità temporale su "detect" se non è importante che siano presenti due origini di informazioni sulla posizione. In modalità di rilevamento, il driver VISCA usa le informazioni sul codice temporale per il posizionamento quando si verifica una delle condizioni seguenti:

-   Le informazioni sul codice temporale sono presenti all'apertura del driver.
-   Si modifica un videotape con il **comando** "door open" impostato e le informazioni sul codice temporale sono presenti nella videotape.
-   Il [**comando**](set.md) set "time mode" viene riemittente.

Se non è possibile trovare informazioni sul codice temporale, il driver usa i contatori del nastro.

Per determinare il metodo di posizionamento corrente, eseguire [**il**](status.md) comando di stato "time type", che restituisce "timecode" o "counter". È anche possibile identificare la modalità di posizionamento corrente usando il comando **status** "time mode", che restituisce "timecode", "counter" o "detect".

Il **comando** "counter" di stato recupera il valore corrente del contatore del nastro, indipendentemente dal metodo di posizionamento corrente. Tuttavia, è possibile usare questo contatore solo con il [**comando set**](set.md) "counter".

Il driver VISCA può recuperare il formato del codice temporale nativo registrato in una videoregistrazione usando i comandi **di** stato "timecode type" e **status** "frame rate" insieme. Ad esempio, se il tipo di codice temporale è "smpte" e la frequenza dei fotogrammi è 25, il formato del codice temporale nativo registrato nella videotape è SMPTE 25.

Il driver VISCA può anche recuperare la risoluzione del contatore usando il comando **di** stato "risoluzione del contatore", che restituisce "secondi" o "frame". Il formato del contatore potrebbe essere ancora impostato su SMPTE 30, ma il valore restituito restituisce solo un frame pari a 0. Se il tipo di ora corrente è counter, questa risoluzione si applica anche al valore restituito dallo **stato** "position".

## <a name="capturing-frames"></a>Acquisizione di frame

I comandi di acquisizione di frame forniscono immagini fisse per un *dispositivo di acquisizione di frame.* Un dispositivo di acquisizione fotogrammi è un componente hardware separato in grado di leggere e archiviare l'immagine video. Il driver VISCA supporta il [**comando freeze**](freeze.md) ([**MCI \_ FREEZE**](mci-freeze.md)) per stabilizzare un'immagine fissista per l'acquisizione. Inoltre, il [**comando unfreeze**](unfreeze.md) ([**MCI \_ UNFREEZE**](mci-unfreeze.md)) può essere usato per riavviare il trasporto su nastro dopo un **comando freeze.**

Il **comando freeze** fornisce un'immagine corretta di alta qualità, stabilizzata e basata sul tempo per un dispositivo di acquisizione frame. Questo comando esiste perché un dispositivo potrebbe non recapitare sempre l'immagine di output di massima qualità durante la riproduzione o durante la sospensione. un'immagine video di questo tipo non è adatta per l'acquisizione.

Il **comando unfreeze** sblocca il trasporto del nastro e riprende la modalità di trasporto attiva prima del **comando freeze.**

Quando l'applicazione deve registrare un'immagine video nel videoregistratore, usare il comando **freeze** "input" o il [**comando cue**](cue.md) ( MCI CUE ) per [**\_ registrare**](mci-cue.md)l'immagine.

## <a name="selecting-inputs"></a>Selezione di input

Il driver VISCA supporta tre tipi di input: video, audio e timecode. Gli input video includono due canali standard (linee 1 e 2), un canale SVideo, un canale ausiliario e un canale da un siner interno. Gli input audio includono due canali standard (linee 1 e 2) e un canale da un siner interno. L'input del codice temporale è interno al videoregistratore.

Gli output normali trasportano gli input attualmente selezionati quando il videoregistratore sta registrando o quando il trasporto del nastro viene arrestato e trasportano il contenuto della videocassetta quando il trasporto del nastro è in riproduzione o in pausa. Gli output monitorati hanno le stesse informazioni degli output normali, oltre al codice temporale e alle informazioni sul canale correnti.

Supponendo che gli input esterni appropriati siano connessi al videoregistratore e che si sia deciso cosa registrare, è possibile selezionare gli input da registrare. Ad esempio, per registrare o visualizzare dal video "svideo" e dagli input audio "riga 1", usare i comandi [**setvideo**](setvideo.md) ([**MCI \_ SETVIDEO**](mci-setvideo.md)) e [**setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) per selezionare queste origini di input. È possibile verificare queste selezioni usando il comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)).

Per impostazione predefinita, il monitoraggio mostra esattamente ciò che viene visualizzato come output. A volte, tuttavia, potrebbe essere necessario visualizzare un'origine durante la registrazione da un'altra. Si tratta di una pratica comune che usa il siner. Ad esempio, potrebbe essere necessario guardare il canale 4 mentre si registra il canale 7. In questo caso, sono disponibili due input di siner logici. È possibile configurare il videoregistratore usando i comandi seguenti:

## <a name="to-review-one-source-while-recording-from-another"></a>Per esaminare un'origine durante la registrazione da un'altra

1.  Usare il [**comando settuner**](settuner.md) ([**MCI \_ SETTUNER**](mci-settuner.md)) per selezionare i canali da guardare e registrare.
2.  Usare il **comando setvideo** per selezionare l'origine della registrazione video.
3.  Usare il [**comando setaudio**](setaudio.md) per selezionare l'origine di registrazione audio.
4.  Usare il [**comando setvideo**](setvideo.md) per indirizzare l'input video channel 4 all'output monitorato per visualizzarlo sullo schermo.
5.  Usare il [**comando setaudio**](setaudio.md) per indirizzare l'input audio del canale 4 all'output monitorato per riprodurre l'audio.
6.  Verificare le selezioni usando il [**comando status.**](status.md)

Il driver VISCA supporta anche un tipo di input speciale per audio e video denominato *mute.* Disattiva consente la selezione di "nessun input", utile quando si registra un segnale vuoto.

## <a name="selecting-recording-tracks"></a>Selezione delle tracce di registrazione

In un videotape sono disponibili tre tipi di tracce di registrazione: video, audio e timecode. È disponibile una sola traccia video o timecode, ma è possibile usare più tracce audio. In questo caso, impostare la traccia 1 come traccia audio principale.

Il driver VISCA supporta due modalità operative: assemblare e inserire. In *modalità assemble* vengono selezionate tutte le tracce da registrare. In *modalità inserimento* le tracce possono essere selezionate in modo indipendente per la registrazione. La maggior parte dei videoregistratori è in modalità di assemblaggio per impostazione predefinita. Usare il [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)) per modificare queste modalità.

## <a name="recording-and-editing"></a>Registrazione e modifica

Il [**comando record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) fornisce una registrazione semplice ed è accurato a circa 1 secondo della posizione iniziale. Per registrare in modo più accurato o se si prevede di modificare il contenuto video durante il funzionamento simultaneo di più mazzi, è consigliabile usare il comando [**cue**](cue.md) ([**MCI \_ CUE).**](mci-cue.md)

Il **comando cue** prepara il dispositivo per la registrazione o la riproduzione. Usare il **comando cue** "input" per preparare il dispositivo per la registrazione. Il **comando cue** è obbligatorio perché un'applicazione deve sapere quando il dispositivo è pronto per eseguire il comando (e perché possono essere necessari alcuni minuti per prepararsi [**a**](play.md) una riproduzione ([**MCI \_ PLAY**](mci-play.md)) o al comando **di registrazione.**

Il videoregistratore si prepara per la registrazione o la riproduzione cercando nel punto *,* ovvero la posizione corrente o la posizione specificata tramite il comando **cue** "from". Se il flag di preroll viene specificato con il comando **cue,** tuttavia, il videoregistratore posiziona se stesso la distanza di preroll dal punto. Il flag "preroll" indica anche che il videoregistratore usa qualsiasi modalità di modifica applicabile, quindi è importante usare la "preroll", soprattutto quando si vuole la registrazione più accurata. Usare il [**comando capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) con il flag "can preroll" per verificare se la modalità di preroll è supportata.

> [!Note]  
> Quando si registra usando le posizioni "from" e "to", la posizione "from" viene inclusa nella modifica e la posizione "to" non lo è.

 

Per altre informazioni sulla registrazione, vedere [Registrazione](recording.md).

## <a name="using-the-clock-while-editing"></a>Uso dell'orologio durante la modifica

Durante la modifica, potrebbe essere necessario registrare segmenti da un videoregistratore a un altro. È possibile iniziare a registrare in un'ora e in una posizione specifiche su un videoregistratore mentre un altro inizia a riprodurre contemporaneamente e posizione specificando un'azione (riproduzione o registrazione), una posizione e un'ora per ogni videoregistratore.

Entrambi i videoregistratori devono usare lo stesso orologio per questo tipo di modifica. l'orologio consente di sincronizzare entrambi i dispositivi. È possibile determinare se due videoregistratori condividono lo stesso clock usando il comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) con il flag "clock id" per eseguire query su ogni videoregistratore. Se i numeri di identificazione restituiti dal **comando di** stato sono gli stessi, i dispositivi usano lo stesso orologio. Come risorsa condivisa, l'orologio può essere connesso a più videoregistratori. Il driver VISCA supporta un solo orologio condiviso.

È anche possibile determinare la risoluzione del clock usando il **comando di** stato "clock increment rate". Questo comando restituisce il numero di incrementi supportati dal clock al secondo. Ad esempio, se l'orologio viene aggiornato ogni millisecondo, il comando restituisce 1000 come frequenza di incremento del clock. Il vantaggio dell'uso del tasso di incremento è che la velocità viene espressa come numero intero. In caso contrario, l'incremento sarebbe un valore a virgola mobile (a precisione singola o doppia). Come numero intero, la modifica della frequenza di incremento è un'operazione semplice e non è soggetta a errori di arrotondamento. È possibile reimpostare l'orologio usando il [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)) con il flag "clock 0" (zero).

Quando si esegue [](play.md) una riproduzione [**(MCI \_ PLAY),**](mci-play.md)un [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) o un comando [**seek**](seek.md) ([**MCI \_ SEEK),**](mci-seek.md)è possibile specificare quando eseguire il comando. Le caratteristiche delle videoregistratori usate determinano quando avviare ogni videoregistratore. La tempistica deve prendere in considerazione la quantità di preroll richiesta da ogni dispositivo e la quantità di tempo necessaria per completare i comandi MCI usati per configurare la sessione di modifica. A tale scopo, recuperare l'ora del clock e aggiungere un intervallo di attesa da 5 a 10 secondi. L'intervallo di attesa deve essere sufficientemente lungo per consentire il completamento dell'esecuzione del preroll e degli eventuali comandi MCI in sospeso.

Per assicurarsi che il periodo di attesa sia sufficientemente lungo, inserire l'ultimo **comando di record** nell'applicazione e controllare l'ora immediatamente precedente. Se l'intervallo è troppo breve, riavviare il **comando play.** In alternativa, è possibile controllare l'ora immediatamente dopo l'ultimo comando dello script per verificare che sia disponibile tempo sufficiente per inviare e completare tutti i comandi.

 

 




