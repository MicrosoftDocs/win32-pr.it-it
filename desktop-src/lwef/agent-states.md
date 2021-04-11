---
title: Stati dell'agente
description: Stati dell'agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c371b1a2126129c03f16ce7fc7c2f95cca955a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221086"
---
# <a name="agent-states"></a>Stati dell'agente

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

I servizi di animazione Microsoft Agent riproducono automaticamente determinate animazioni. Ad esempio, quando si utilizzano i comandi [**MoveTo**](moveto-method.md) o [**GestureAt**](gestureat-method.md) , i servizi animazione svolgono un'animazione appropriata. Analogamente, dopo il timeout di inattività, i servizi riproducono automaticamente le animazioni. Per supportare questi Stati, è possibile definire animazioni appropriate e quindi assegnarle agli Stati. È comunque possibile riprodurre qualsiasi animazione definita direttamente usando il metodo [**Play**](play-method.md) , anche se viene assegnata a uno stato.

È possibile assegnare più animazioni allo stesso stato e i servizi di animazione scelgono una delle animazioni in modo casuale. Ciò consente al carattere di presentare una varietà molto più naturale nel suo comportamento.

Sebbene le animazioni assegnate agli Stati possono includere rami di branching, evitare animazioni di ciclo (animazioni che diramano per sempre). In caso contrario, sarà necessario utilizzare il metodo [**Stop**](play-method.md) prima di poter riprodurre un'altra animazione.

È importante definire e assegnare almeno un'animazione per ogni stato che si verifica per il carattere. Se non si specificano queste animazioni e assegnazioni di stato, è possibile che il carattere non comporti un comportamento appropriato per l'utente. Tuttavia, se non si verifica uno stato per un particolare carattere, non è necessario assegnare un'animazione a tale stato. Se, ad esempio, l'applicazione host non chiama mai il metodo [**MoveTo**](moveto-method.md) , è possibile ignorare la creazione e l'assegnazione delle animazioni dello stato di **trasferimento** .



| State              | Esempio di utilizzo                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Quando viene elaborato il metodo di animazione [**GestureAt**](gestureat-method.md) .          |
| **GesturingLeft**  | Quando viene elaborato il metodo di animazione [**GestureAt**](gestureat-method.md) .          |
| **GesturingRight** | Quando viene elaborato il metodo di animazione [**GestureAt**](gestureat-method.md) .          |
| **GesturingUp**    | Quando viene elaborato il metodo di animazione [**GestureAt**](gestureat-method.md) .          |
| **Udito**        | Quando viene rilevato l'inizio dell'input vocale.                                        |
| **Nascondere**         | Quando l'utente o l'applicazione nasconde il carattere.                                  |
| **IdlingLevel1**   | Quando il carattere inizia lo stato **minimo** .                                        |
| **IdlingLevel2**   | Quando il carattere inizia il secondo stato del livello **minimo** .                           |
| **IdlingLevel3**   | Quando il carattere inizia lo stato del livello di inversione **minimo** finale.                            |
| **In ascolto**      | Quando il carattere inizia l'ascolto, l'utente preme prima il tasto di scelta rapida di input vocale. |
| **MovingDown**     | Quando il metodo di animazione [**MoveTo**](moveto-method.md) viene elaborato.                |
| **MovingLeft**     | Quando il metodo di animazione [**MoveTo**](moveto-method.md) viene elaborato.                |
| **MovingRight**    | Quando il metodo di animazione [**MoveTo**](moveto-method.md) viene elaborato.                |
| **MovingUp**       | Quando il metodo di animazione [**MoveTo**](moveto-method.md) viene elaborato.                |
| **Visualizzazione**        | Quando l'utente o l'applicazione Visualizza il carattere.                                  |
| **Parlando**       | Quando il metodo di animazione [**Speak**](speak-method.md) viene elaborato.                  |



 

### <a name="the-hearing-and-listening-states"></a>Stati di udito e ascolto

L'animazione assegnata allo stato di **ascolto** viene riprodotta quando l'utente preme il tasto di scelta rapida per l'input vocale. Creare e assegnare una breve animazione che rende il carattere attento. Analogamente, definire la relativa animazione **restituita** in modo che abbia una durata breve, in modo che il carattere riproduca l'animazione dello stato di **udito** quando l'utente parla. Un'animazione di stato di **audizione** dovrebbe anche essere breve e progettata per informare l'utente che il carattere è in ascolto attivo per quanto afferma l'utente. Le inclinazioni Head o altri piccoli movimenti sono appropriati. Per fornire una variabilità naturale, fornire diverse animazioni dello stato di **udito** .

### <a name="the-gesturing-states"></a>Stati gestuali

È necessario creare e assegnare animazioni di stato **gestuale** solo se si prevede di usare il metodo [**GestureAt**](gestureat-method.md) . Le animazioni dello stato **gestuale** vengono riprodotte quando Microsoft Agent elabora una chiamata al metodo **GestureAt** . Se si definiscono le sovrapposizioni della bocca per le animazioni dello stato **gestuale** , il carattere può parlare come movimenti.

I servizi di animazione determinano la posizione del carattere e la relativa relazione con la posizione delle coordinate specificate nel metodo e svolgono un'animazione appropriata. La direzione della gestualità è sempre rispetto al carattere; ad esempio, **GestureRight** deve essere un movimento al diritto del carattere.

### <a name="the-showing-and-hiding-states"></a>Mostra e Nascondi Stati

Gli stati **Mostra** e **Nascondi** svolgono le animazioni assegnate quando l'utente o l'applicazione host richiede di mostrare o nascondere il carattere. Questi stati inoltre impostano in modo appropriato lo stato **visibile** del frame di caratteri. Quando si definiscono le animazioni per questi Stati, tenere presente che un carattere può essere visualizzato o ripartito in qualsiasi posizione dello schermo. Poiché l'utente può visualizzare o nascondere qualsiasi carattere, supporta sempre almeno un'animazione per questi Stati.

Le animazioni assegnate allo stato di **visualizzazione** in genere terminano con un frame contenente l'immagine della posizione neutra del carattere. Viceversa, le animazioni di stato **nascoste** iniziano in genere con la posizione neutra. **Mostrare** e **nascondere** le animazioni di stato può includere rispettivamente un frame vuoto all'inizio o alla fine per fornire una transizione dallo stato corrente del carattere.

### <a name="the-idling-states"></a>Stati di minimo

Gli Stati di **minimo** sono progressivi. I servizi di animazione iniziano a usare le assegnazioni di livello 1 per il primo periodo di inattività e usano le animazioni di livello 2 per il secondo. Successivamente, il ciclo di inattività passa alle animazioni assegnate di livello 3 e rimane in questo stato fino a quando non viene annullato, ad esempio quando inizia una nuova richiesta di animazione.

Progettare animazioni per gli Stati di **minimo** per comunicare lo stato del carattere, ma non per distrarre l'utente. Le animazioni devono riflettere in modo appropriato la velocità di risposta del carattere in modi sottili ma chiari. Ad esempio, un'occhiata o un lampeggio sono ottime animazioni da assegnare allo stato **IdlingLevel1** . La lettura delle animazioni funziona bene per lo stato **IdlingLevel2** . La sospensione o l'ascolto di musica con le cuffie sono ottimi esempi di animazioni da assegnare allo stato **IdlingLevel3** . Le animazioni che includono molti o movimenti di grandi dimensioni non sono particolarmente adatte per le animazioni inattive perché attirano l'attenzione dell'utente. Poiché le animazioni di stato **minimo** vengono riprodotte spesso, fornire diverse animazioni di stato al **minimo** , specialmente per gli stati **IdlingLevel1** e **IdlingLevel2** .

Si noti che un'applicazione può disattivare l'elaborazione automatica di inattività per un carattere e gestire lo **stato di inattività del carattere** . Gli stati **di** indisponibilità degli agenti sono progettati per evitare situazioni in cui il carattere non ha alcuna animazione da riprodurre. Un'immagine di carattere che non cambia dopo un breve periodo di tempo è simile a un'applicazione che visualizza un puntatore di attesa per un lungo periodo di tempo, il che comporta una riduzione del grado di credibilità e dell'interattività. La gestione dell'illusione non ha molto tempo: a volte solo un lampeggio animato, un respiro visibile o uno spostamento del corpo.

### <a name="the-speaking-state"></a>Stato di pronuncia

I servizi di animazione utilizzano lo stato di **pronuncia** quando non è possibile trovare un'animazione di pronuncia per l'animazione corrente. Consente di assegnare a questo stato una semplice animazione di pronuncia. Ad esempio, è possibile usare un singolo frame costituito dalla posizione neutra del carattere con sovrapposizioni della bocca.

### <a name="the-moving-states"></a>Stati spostati

Gli stati **spostati** vengono riprodotti quando un'applicazione chiama il metodo [**MoveTo**](moveto-method.md) . I servizi di animazione determinano l'animazione da riprodurre in base alla posizione corrente del carattere e alle coordinate specificate. La direzione dello spostamento è basata sulla posizione del carattere. Pertanto, l'animazione assegnata all'animazione **MovingLeft** dovrebbe essere basata sul carattere a sinistra. Se non si usa il metodo **MoveTo** , è possibile ignorare la creazione e l'assegnazione di un'animazione.

Lo stato di animazione dello stato di **trasferimento** deve animare il carattere nella posizione di trasferimento. L'ultimo frame dell'animazione viene visualizzato quando il frame del carattere viene spostato sullo schermo. Non è disponibile alcun supporto per l'animazione del carattere durante lo spostamento del frame.

### <a name="standard-animation-set"></a>Set di animazioni standard

Sebbene sia possibile progettare un carattere personalizzato per avere le animazioni che si vuole usare, Microsoft Agent definisce un set di animazioni standard. I caratteri conformi a questa definizione possono essere selezionati come carattere predefinito.

La tabella seguente elenca le animazioni incluse nel set di animazioni standard. Anche se si crea un carattere personalizzato, è possibile usare l'elenco come guida per la progettazione dei propri caratteri. I caratteri che supportano il set di animazioni standard devono supportare almeno le animazioni seguenti.



| Animazione                        | Esempio di utilizzo                                                                                           | Animazione di esempio                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Riconoscere**                  | Quando il carattere riconosce la richiesta dell'utente.                                                      | Il carattere fa cenno o emette un movimento della mano "OK". Si noti che questa animazione deve restituire il carattere alla relativa posizione neutra.<br/>                                                                                  |
| **Avviso**<sup>1, 2</sup>          | Quando il carattere è in attesa di istruzioni, in genere riprodotto dopo l'accensione della modalità di ascolto da parte dell'utente. | Il carattere viene esposto in primo piano, respirando, lampeggiando occasionalmente, ma in attesa di un'istruzione.                                                                                                                             |
| **Annunciare**<sup>1, 2</sup>       | Quando il carattere ha trovato informazioni per l'utente.                                                   | Movimenti di caratteri mediante la generazione di sopracciglia e la mano o l'apertura di una busta.                                                                                                                                                  |
| **Blink**                        | Quando il carattere termina o inattivo.                                                            | Il carattere lampeggia naturalmente gli occhi.                                                                                                                                                                                       |
| **Confuso**<sup>1, 2</sup>       | Quando il carattere non comprende le operazioni da eseguire.                                                        | Carattere in Scratch.                                                                                                                                                                                              |
| **Congratulazioni**<sup>1, 2</sup>   | Quando il carattere o l'utente completa un'attività (una forma più avanzata dell'animazione di **riconoscimento** ).          | Il carattere esegue un gesto di congratulazioni, trasmette "Sì!"                                                                                                                                                              |
| **Rifiuto**<sup>1, 2</sup>        | Quando il carattere non può eseguire o rifiutare la richiesta dell'utente.                                             | Il carattere scuote la testa, trasmette "no can do".                                                                                                                                                                            |
| **DoMagic1**                     | Il carattere viene preparato per visualizzare un elemento.                                                                 | I caratteri Waves o bacchetta.                                                                                                                                                                                         |
| **DoMagic2**                     | Il carattere completa la visualizzazione di un elemento.                                                                | Il carattere completa il gesto magico.                                                                                                                                                                                     |
| **DontRecognize**<sup>1, 2</sup>  | Quando il carattere non riconosce la richiesta dell'utente.                                                  | Il carattere viene mantenuta a orecchio.                                                                                                                                                                                           |
| **Spiegazione**<sup>1, 2</sup>        | Quando il carattere spiega qualcosa all'utente.                                                       | Movimenti di caratteri come se si spiegasse qualcosa.                                                                                                                                                                         |
| **GestureDown**<sup>1, 2</sup>    | Quando il carattere deve puntare a un elemento al di sotto di esso.                                                 | Il carattere punta verso il basso.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1, 2</sup>    | Quando il carattere deve puntare a un elemento a sinistra.                                              | Punti carattere con sinistra o morph in una freccia rivolta verso sinistra.                                                                                                                                                 |
| **GestureRight**<sup>1, 2</sup>   | Quando il carattere deve puntare a un elemento a destra.                                             | Punti dei caratteri con la destra o i morph in una freccia rivolta verso destra.                                                                                                                                               |
| **GestureUp**<sup>1, 2</sup>      | Quando il carattere deve puntare a un elemento al di sopra di esso.                                                 | Punti di carattere verso l'alto.                                                                                                                                                                                                   |
| **Getattenzione**                 | Quando il carattere deve notificare all'utente un elemento importante.                                   | Le Wave di tipo carattere si spostano verso l'alto e verso il basso.                                                                                                                                                                            |
| **GetAttentionContinued**        | Per evidenziare l'importanza della notifica.                                                         | Continuazione o ripetizione del movimento iniziale.                                                                                                                                                                       |
| **GetAttentionReturn**           | Quando il carattere completa l'animazione **Getattention** o **GetAttentionContinued** .                | Il carattere torna alla relativa posizione neutra.                                                                                                                                                                             |
| **Saluto**<sup>1, 2</sup>          | Quando l'utente avvia il sistema.                                                                      | Smile e Wave.                                                                                                                                                                                            |
| **Hearing1**                     | Quando il carattere ascolta l'inizio di un enunciato vocale (in ascolto attivo).                           | Il carattere è incline a inclinazioni e Cenni, oppure a un'intestazione che mostra la risposta all'input vocale. Nota: questa animazione esegue il ciclo su un frame intermedio che si verifica dopo che il carattere è stato spostato in una posizione appropriata.<br/>   |
| **Hearing2**                     | Quando il carattere ascolta l'inizio di un enunciato vocale (in ascolto attivo).                           | Un'altra variante del tipo di animazione usato in **Hearing1** Nota: questa animazione esegue il ciclo in un frame intermedio che si verifica dopo che il carattere è stato spostato in una posizione appropriata.<br/>                      |
| **Nascondi**                         | Quando l'utente dimentica il carattere.                                                                   | Il carattere rimuove autonomamente dallo schermo.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Quando il carattere non ha attività e l'utente non interagisce con il carattere.                       | Il carattere lampeggia o Cerca, rimanendo o tornando alla posizione neutra.                                                                                                                                   |
| **Idle1 \_ 2**                     | Quando il carattere non ha attività e l'utente non interagisce con il carattere.                       | Un'altra variante del tipo di animazione utilizzato in **Idle1 \_ 1**.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Quando il carattere è rimasto inattivo per un certo periodo di tempo.                                                          | Il carattere sbadiglia o legge la rivista che rimane o ritorna alla posizione neutra.                                                                                                                                   |
| **Idle2 \_ 2**                     | Quando il carattere è rimasto inattivo per un certo periodo di tempo.                                                          | Un'altra variante del tipo di animazione utilizzato in **Idle2 \_ 1**.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Quando il carattere è rimasto inattivo per un lungo periodo di tempo.                                                        | Sbadigli di caratteri.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Quando il carattere è rimasto inattivo per un lungo periodo di tempo.                                                        | Il carattere dorme o inserisce le cuffie per ascoltare la musica. Nota: questa animazione esegue il ciclo su un frame intermedio che si verifica dopo che il carattere è stato spostato in una posizione appropriata.<br/>                          |
| **LookDown**                     | Quando il carattere deve essere sottoposto a ricerca.                                                                   | Il carattere si cerca verso il basso.                                                                                                                                                                                                  |
| **LookLeft**                     | Quando il carattere deve essere lasciato.                                                                   | Il carattere si trova a sinistra.                                                                                                                                                                                           |
| **LookRight**                    | Quando il carattere deve essere a destra.                                                                  | Il carattere si trova a destra.                                                                                                                                                                                          |
| **Ricerca**                       | Quando il carattere deve essere ricercato.                                                                     | Ricerca di caratteri.                                                                                                                                                                                                    |
| **MoveDown**                     | Quando il carattere si prepara per lo spostamento verso il basso.                                                                | Transizioni di caratteri a una posizione a piedi o in basso.                                                                                                                                                               |
| **MoveLeft**                     | Quando il carattere si prepara a spostarsi verso sinistra.                                                                | Transizioni di caratteri a una posizione a sinistra a piedi o in volo.                                                                                                                                                               |
| **MoveRight**                    | Quando il carattere si prepara a spostarsi a destra.                                                               | Transizioni di caratteri a una posizione a destra.                                                                                                                                                              |
| **MoveUp**                       | Quando il carattere si prepara per lo spostamento verso l'alto.                                                                  | Transizioni di caratteri in una posizione a piedi o in alto.                                                                                                                                                                 |
| **Soddisfatto**<sup>1, 2</sup>        | Quando il carattere è soddisfatto della richiesta o della scelta dell'utente.                                         | Caratteri Smile.                                                                                                                                                                                                      |
| **Processo**                      | Quando il carattere esegue un tipo di attività generica.                                                   | Il carattere preme i pulsanti o utilizza un tipo di strumento.                                                                                                                                                                   |
| **Elaborazione in corso**                   | Quando il carattere è occupato a lavorare su un'attività generica.                                                    | Caratteri Scribble sul riempimento di carta o utilizza un tipo di strumento. Nota: questa animazione esegue il ciclo su un frame intermedio che si verifica dopo che il carattere è stato spostato in una posizione appropriata.<br/>                      |
| **Lettura**                         | Quando il carattere legge un elemento all'utente.                                                          | Il carattere Visualizza un libro o un documento, legge e cerca l'utente.                                                                                                                                                       |
| **ReadContinued**                | Quando il carattere viene letto ulteriormente dall'utente.                                                            | Il carattere esegue nuovamente la lettura, quindi cerca l'utente.                                                                                                                                                                        |
| **ReadReturn**                   | Quando il carattere completa l'animazione di **lettura** o di **ReadContinued** .                                | Il carattere torna alla relativa posizione neutra.                                                                                                                                                                             |
| **Lettura**                      | Quando il carattere legge qualcosa ma non accetta input.                                              | Letture di caratteri da un pezzo di carta. Nota: questa animazione esegue il ciclo per alcuni frame intermedi che si verificano dopo che il carattere è stato spostato in una posizione appropriata.<br/>                                           |
| **RestPose**                     | Quando il carattere parla dalla posizione neutra.                                                     | Il carattere è caratterizzato da un atteggiamento rilassato ma attento.                                                                                                                                                                   |
| **Triste**<sup>1, 2</sup>            | Quando il carattere è deluso dalla scelta dell'utente.                                               | Il carattere è imbronciato o sembra deluso.                                                                                                                                                                                |
| **Ricerca**                       | Quando il carattere cerca un elemento.                                                                   | Il carattere viene rimescolato tramite il cassetto dei file o un altro contenitore che cerca un elemento.                                                                                                                                       |
| **Ricerca**                    | Quando il carattere cerca le informazioni specificate dall'utente.                                              | Il carattere viene rimescolato tramite il cassetto dei file o un altro contenitore che cerca un elemento. Nota: questa animazione esegue il ciclo per alcuni frame intermedi che si verificano dopo che il carattere è stato spostato in una posizione appropriata.<br/> |
| **Mostra**                         | Quando il carattere viene avviato o restituito dopo essere stato chiamato.                                            | Il carattere viene visualizzato in un soffio di fumo, travi in o passaggi sullo schermo.                                                                                                                                                    |
| **StartListening**<sup>1, 2</sup> | Quando il carattere è in ascolto.                                                                         | Il carattere mette a disposizione l'orecchio.                                                                                                                                                                                            |
| **StopListening**<sup>1, 2</sup>  | Quando il carattere smette di restare in attesa.                                                                      | Il carattere pone le orecchie.                                                                                                                                                                                        |
| **Suggerisci**<sup>1, 2</sup>        | Quando il carattere presenta una mancia o un suggerimento per l'utente.                                                 | Il bulbo di luce viene visualizzato accanto a carattere.                                                                                                                                                                                  |
| Con **stupore**<sup>1, 2</sup>      | Quando il carattere viene sorpreso dall'azione o dalla scelta dell'utente.                                          | Il carattere allarga gli occhi, apre la bocca.                                                                                                                                                                                    |
| **Pensa**<sup>1, 2</sup>          | Quando il carattere sta pensando a qualcosa.                                                          | Il carattere cerca e controlla la mano.                                                                                                                                                                             |
| **Incerto**<sup>1, 2</sup>      | Quando il carattere richiede all'utente di confermare una richiesta.                                                  | Il carattere è Quizzical, trasmette ("è sicuro?")                                                                                                                                                                   |
| **Wave**<sup>1, 2</sup>           | Quando l'utente sceglie di arrestare il server o il sistema.                                                 | Le Wave di tipo carattere sono ottime, bye o Hello.                                                                                                                                                                                     |
| **Scrittura**                        | Quando il carattere è in ascolto delle istruzioni dell'utente.                                          | Il carattere Visualizza il documento, scrive e cerca l'utente.                                                                                                                                                              |
| **WriteContinued**               | Quando il carattere continua ad ascoltare le istruzioni dell'utente.                                   | Scritture di caratteri in un pezzo di carta e cerca l'utente.                                                                                                                                                           |
| **WriteReturn**                  | Quando il carattere completa l'animazione **Write** o **WriteContinued** .                              | Il carattere torna alla relativa posizione neutra.                                                                                                                                                                             |
| **Scrittura**                      | Quando il carattere scrive informazioni per l'utente.                                                  | Scritture di caratteri sul foglio di carta. Nota: questa animazione esegue il ciclo.<br/>                                                                                                                                             |



 

  L'animazione richiede sovrapposizioni della bocca e un frame di pronuncia definito.

  L'animazione richiede un'animazione return assegnata in base alla relativa diramazione di uscita o a un'animazione return esplicita.

Inoltre, un carattere deve avere le seguenti assegnazioni di stato.



| State          | Animazioni obbligatorie                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Udito        | Hearing1, Hearing2                            |
| Nascondere         | Nascondi                                          |
| IdlingLevel1   | Blink, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| In ascolto      | Avviso                                         |
| MovingDown     | MoveDown                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| MovingUp       | MoveUp                                        |
| Visualizzazione        | Mostra                                          |
| Parlando       | RestPose                                      |



 

 

 





