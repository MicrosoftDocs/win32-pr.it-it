---
title: Stati dell'agente
description: Stati dell'agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbfb927cbe9ad703e733caa827df7c5a63bac67b93d49edbb8f59884c89b6ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976801"
---
# <a name="agent-states"></a>Stati dell'agente

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

I servizi di animazione di Microsoft Agent riprodurno automaticamente determinate animazioni. Ad esempio, quando si usano i [**comandi MoveTo**](moveto-method.md) [**o GestureAt,**](gestureat-method.md) i servizi di animazione riproducino un'animazione appropriata. Analogamente, dopo il timeout di inattività, i servizi riprodureranno automaticamente le animazioni. Per supportare questi stati, è possibile definire animazioni appropriate e quindi assegnarle agli stati. È comunque possibile riprodurre qualsiasi animazione definita direttamente usando il [**metodo Play,**](play-method.md) anche se la si assegna a uno stato.

È possibile assegnare più animazioni allo stesso stato e i servizi di animazione sceglieranno in modo casuale una delle animazioni. In questo modo il tuo carattere può presentare una varietà molto più naturale nel suo comportamento.

Anche se le animazioni assegnate agli stati possono includere fotogrammi di diramazione, evitare di creare cicli di animazioni (animazioni che si dirameranno per sempre). In caso contrario, sarà necessario usare il metodo [**Stop prima**](play-method.md) di poter riprodurre un'altra animazione.

È importante definire e assegnare almeno un'animazione per ogni stato che si verifica per il carattere. Se non si specificano queste animazioni e assegnazioni di stato, è possibile che il carattere non si comporti in modo appropriato per l'utente. Tuttavia, se non si verifica uno stato per un particolare carattere, non è necessario assegnare un'animazione a tale stato. Ad esempio, se l'applicazione host non chiama mai il [**metodo MoveTo,**](moveto-method.md) è possibile ignorare la creazione e l'assegnazione di animazioni **di** stato Moving.



| State              | Esempio d'uso                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Quando viene elaborato il metodo di animazione [**GestureAt.**](gestureat-method.md)          |
| **GesturingLeft**  | Quando viene elaborato il metodo di animazione [**GestureAt.**](gestureat-method.md)          |
| **GesturingRight** | Quando viene elaborato il metodo di animazione [**GestureAt.**](gestureat-method.md)          |
| **GesturingUp**    | Quando viene elaborato il metodo di animazione [**GestureAt.**](gestureat-method.md)          |
| **Udito**        | Quando viene rilevato l'inizio dell'input parlato.                                        |
| **Nascondere**         | Quando l'utente o l'applicazione nasconde il carattere.                                  |
| **IdlingLevel1**   | Quando il carattere inizia lo **stato idling.**                                        |
| **IdlingLevel2**   | Quando il carattere inizia il secondo **stato del livello** di identificazione.                           |
| **IdlingLevel3**   | Quando il carattere inizia lo stato **finale del livello** di identificazione.                            |
| **Ascolto**      | Quando il carattere inizia ad ascoltare (l'utente preme per la prima volta il tasto di scelta rapida per l'input vocale). |
| **MovingDown**     | Quando viene elaborato il metodo di animazione [**MoveTo.**](moveto-method.md)                |
| **MovingLeft**     | Quando viene elaborato il metodo di animazione [**MoveTo.**](moveto-method.md)                |
| **MovingRight**    | Quando viene elaborato il metodo di animazione [**MoveTo.**](moveto-method.md)                |
| **MovingUp**       | Quando viene elaborato il metodo di animazione [**MoveTo.**](moveto-method.md)                |
| **Visualizzazione**        | Quando l'utente o l'applicazione visualizza il carattere .                                  |
| **Parlando**       | Quando viene [**elaborato il metodo**](speak-method.md) di animazione Speak.                  |



 

### <a name="the-hearing-and-listening-states"></a>Stati di ascolto e di ascolto

L'animazione assegnata allo stato **Listening** viene riprodotta quando l'utente preme il tasto di scelta rapida push-to-talk per l'input vocale. Creare e assegnare una breve animazione che rende il carattere più attento. Analogamente, definire **l'animazione Return** in modo che abbia una durata breve, in modo che il carattere riproduci l'animazione dello stato **di** ascolto quando l'utente parla. Anche **un'animazione** dello stato dell'udito deve essere breve e progettata per invoire l'utente a sapere che il carattere è attivamente in ascolto di ciò che dice l'utente. È appropriato inclinare la testa o altri piccoli movimenti. Per fornire la variabilità naturale, fornire diverse animazioni **dello stato dell'udito.**

### <a name="the-gesturing-states"></a>Stati di inserimento

È necessario creare e assegnare animazioni di stato di **gesturing** solo se si prevede di usare il [**metodo GestureAt.**](gestureat-method.md) **Le animazioni di stato** di inserimento vengono riprodotte quando Microsoft Agent elabora una chiamata al **metodo GestureAt.** Se si definiscono sovrimpressione per le animazioni di stato di **Gesturing,** il carattere può parlare durante i movimenti.

I servizi di animazione determinano la posizione del carattere e la relativa relazione con la posizione delle coordinate specificate nel metodo e riproduceno un'animazione appropriata. La direzione di inserimento è sempre rispetto al carattere; Ad esempio, **GestureRight** deve essere un movimento a destra del carattere.

### <a name="the-showing-and-hiding-states"></a>Stati di visualizzazione e di nascondere

Gli **stati Showing** **(Visualizzazione) e Hiding (Nascondi)** riproducino le animazioni assegnate quando l'utente o l'applicazione host richiede di mostrare o nascondere il carattere. Questi stati impostano anche in modo appropriato lo stato Visible del **frame di** caratteri. Quando si definiscono animazioni per questi stati, tenere presente che un carattere può apparire o rimanere invaso in qualsiasi posizione dello schermo. Poiché l'utente può mostrare o nascondere qualsiasi carattere, supporta sempre almeno un'animazione per questi stati.

Le animazioni assegnate allo stato **Showing** terminano in genere con un fotogramma contenente l'immagine della posizione neutra del carattere. Al contrario, nascondere **le animazioni** di stato inizia in genere con la posizione neutra. **Le** animazioni di stato Showing e **Hiding** possono includere rispettivamente un frame vuoto all'inizio o alla fine per fornire una transizione dallo stato corrente del carattere.

### <a name="the-idling-states"></a>Stati di idling

Gli **stati idling** sono progressivi. I servizi di animazione iniziano a usare le assegnazioni di livello 1 per il primo periodo di inattività e usano le animazioni di livello 2 per il secondo. Successivamente, il ciclo di inattività avanza fino alle animazioni assegnate di livello 3 e rimane in questo stato fino all'annullamento, ad esempio quando inizia una nuova richiesta di animazione.

Progettare animazioni per gli stati **idling** per comunicare lo stato del carattere, ma non per distrarre l'utente. Le animazioni devono riflettere in modo appropriato la velocità di risposta del carattere in modi discreti ma chiari. Ad esempio, il lampeggiamento o il lampeggiamento sono animazioni buone da assegnare allo **stato IdlingLevel1.** La lettura delle animazioni funziona bene per lo **stato IdlingLevel2.** La sospensione o l'ascolto di musica con le cuffi sono esempi di animazioni da assegnare allo **stato IdlingLevel3.** Le animazioni che includono molti o movimenti di grandi dimensioni non sono particolarmente adatte per le animazioni inattive perché disegnano l'attenzione dell'utente. Poiché le animazioni con stato **Idling** vengono riprodotte di frequente, fornire diverse animazioni di stato **idling,** in particolare per gli stati **IdlingLevel1** e **IdlingLevel2.**

Si noti che un'applicazione può disattivare l'elaborazione inattiva automatica per un carattere e gestire lo stato di inattività **del** carattere stesso. Gli stati **di Agent Idling** sono progettati per evitare qualsiasi situazione in cui il carattere non ha animazioni da riprodurre. Un'immagine di carattere che non cambia dopo un breve periodo di tempo è simile a un'applicazione che visualizza un puntatore di attesa per un lungo periodo di tempo, il che sminera il senso di affidabilità e interattività. La gestione dell'intessuto non richiede molto: a volte è sufficiente un lampeggiamento animato, un'affondo visibile o uno spostamento del corpo.

### <a name="the-speaking-state"></a>Stato di pronuncia

I servizi di animazione usano lo **stato Speaking** quando non è possibile trovare un'animazione di pronuncia per l'animazione corrente. Assegnare un'animazione di pronuncia semplice a questo stato. Ad esempio, è possibile usare un singolo fotogramma costituito dalla posizione neutra del carattere con sovrimpressione della cornice.

### <a name="the-moving-states"></a>Stati di spostamento

Gli **stati Spostamento** vengono riprodotti quando un'applicazione chiama il metodo [**MoveTo.**](moveto-method.md) I servizi di animazione determinano quale animazione riprodurre in base alla posizione corrente del carattere e alle coordinate specificate. La direzione di spostamento è basata sulla posizione del carattere. Pertanto, l'animazione assegnata **all'animazione MovingLeft** deve essere basata sulla sinistra del carattere. Se non si usa il metodo **MoveTo,** è possibile ignorare la creazione e l'assegnazione di un'animazione.

**Le animazioni** di stato di spostamento devono animare il carattere nella posizione in movimento. L'ultimo fotogramma di questa animazione viene visualizzato quando il fotogramma del carattere viene spostato sullo schermo. Non è disponibile alcun supporto per l'animazione del carattere durante lo spostamento del frame.

### <a name="standard-animation-set"></a>Set di animazioni standard

Sebbene sia possibile progettare un carattere personalizzato in modo che abbia le animazioni da usare, Microsoft Agent definisce un set di animazioni standard. I caratteri conformi a questa definizione possono essere selezionati come carattere predefinito.

Nella tabella seguente sono elencate le animazioni incluse nel set di animazioni standard. Anche se si crea un carattere personalizzato, è possibile usare l'elenco come guida per la progettazione di caratteri personalizzati. I caratteri che supportano il set di animazioni standard devono supportare almeno le animazioni seguenti.



| Animazione                        | Esempio di utilizzo                                                                                           | Animazione di esempio                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Riconoscere**                  | Quando il carattere conferma la richiesta dell'utente.                                                      | Il carattere lampeggia o fa lampeggiare il movimento della mano "OK". Si noti che questa animazione deve restituire il carattere alla posizione neutra.<br/>                                                                                  |
| **Avviso**<sup>1,2</sup>          | Quando il carattere è in attesa di istruzioni, in genere riprodotto dopo che l'utente ha attivata la modalità di ascolto. | I visi di tipo carattere sono frontale, intermittenti, lampeggianti occasionalmente, ma attendono chiaramente l'istruzione.                                                                                                                             |
| **Annuncio**<sup>1,2</sup>       | Quando il carattere ha trovato informazioni per l'utente.                                                   | I movimenti dei caratteri alzando le ciglia e la mano o apre una busta.                                                                                                                                                  |
| **Blink**                        | Al termine della pronuncia o dell'inattività del carattere.                                                            | Il carattere lampeggia naturalmente gli occhi.                                                                                                                                                                                       |
| **Confuso**<sup>1,2</sup>       | Quando il carattere non comprende cosa fare.                                                        | Il carattere si gratta la testa.                                                                                                                                                                                              |
| **Congratulazioni**<sup>1,2</sup>   | Quando il carattere o l'utente completa un'attività (una forma più avanzata dell'animazione **Acknowledge).**          | Il carattere esegue un gesto di congratulazioni, indicando "Sì!"                                                                                                                                                              |
| **Rifiutare**<sup>1,2</sup>        | Quando il carattere non può eseguire o rifiutare la richiesta dell'utente.                                             | Il carattere scuote la testa, comunica che "non può fare".                                                                                                                                                                            |
| **DoMagic1**                     | Il carattere si prepara a visualizzare qualcosa.                                                                 | Onde di caratteri mani o wand.                                                                                                                                                                                         |
| **DoMagic2**                     | Il carattere completa la visualizzazione di qualcosa.                                                                | Il carattere completa il movimento magico.                                                                                                                                                                                     |
| **DontRecognize**<sup>1,2</sup>  | Quando il carattere non riconosce la richiesta dell'utente.                                                  | Il carattere tiene la mano all'udito.                                                                                                                                                                                           |
| **Spiegare**<sup>1,2</sup>        | Quando il carattere spiega qualcosa all'utente.                                                       | I movimenti dei caratteri sono come se spiegasse qualcosa.                                                                                                                                                                         |
| **GestureDown**<sup>1,2</sup>    | Quando il carattere deve puntare a qualcosa sotto di esso.                                                 | Il carattere punta verso il basso.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1,2</sup>    | Quando il carattere deve puntare a un elemento a sinistra.                                              | Punti carattere con mano sinistra o morphing in una freccia che punta a sinistra.                                                                                                                                                 |
| **GestureRight**<sup>1,2</sup>   | Quando il carattere deve puntare a un elemento a destra.                                             | I punti carattere con la mano destra o si trasformano in una freccia che punta a destra.                                                                                                                                               |
| **GestureUp**<sup>1,2</sup>      | Quando il carattere deve puntare a qualcosa sopra di esso.                                                 | Il carattere punta verso l'alto.                                                                                                                                                                                                   |
| **GetAttention**                 | Quando il carattere deve notificare all'utente qualcosa di importante.                                   | Il carattere onde mani o salti verso l'alto e verso il basso.                                                                                                                                                                            |
| **GetAttentionContinued**        | Per evidenziare l'importanza della notifica.                                                         | Continuazione o ripetizione del movimento iniziale.                                                                                                                                                                       |
| **GetAttentionReturn**           | Quando il carattere completa **l'animazione GetAttention** o **GetAttentionContinued.**                | Il carattere torna alla posizione neutra.                                                                                                                                                                             |
| **Greet**<sup>1,2</sup>          | Quando l'utente avvia il sistema.                                                                      | Sorrisi e onde dei caratteri.                                                                                                                                                                                            |
| **Udito1**                     | Quando il carattere ascolta l'inizio di un'espressione parlata (attivamente in ascolto).                           | Il carattere si inclina in avanti e fa chinare o ruota la testa che mostra la risposta all'input vocale. Nota: questa animazione passa a un fotogramma intermedio che si verifica dopo lo spostamento del carattere in una posizione appropriata.<br/>   |
| **Udito2**                     | Quando il carattere ascolta l'inizio di un'espressione parlata (attivamente in ascolto).                           | Un'altra variazione del tipo di animazione usata in **Hearing1** Nota: questa animazione scorre in un fotogramma intermedio che si verifica dopo che il carattere si sposta in una posizione appropriata.<br/>                      |
| **Nascondi**                         | Quando l'utente chiude il carattere.                                                                   | Il carattere rimuove self dallo schermo.                                                                                                                                                                                    |
| **Inattivo 1 \_ 1**                     | Quando il carattere non ha alcuna attività e l'utente non interagisce con il carattere.                       | Il carattere lampeggia o si guarda intorno, rimanendo o tornando alla posizione neutra.                                                                                                                                   |
| **Inattivo 1 \_ 2**                     | Quando il carattere non ha alcuna attività e l'utente non interagisce con il carattere.                       | Un'altra variante del tipo di animazione usata in **Idle1 \_ 1**.                                                                                                                                                       |
| **Inattivo 2 \_ 1**                     | Quando il carattere è rimasto inattivo per un certo periodo di tempo.                                                          | Il carattere sbadiglia o legge la rivista rimanendo o tornando alla posizione neutra.                                                                                                                                   |
| **Inattivo \_ 2 2**                     | Quando il carattere è rimasto inattivo per un certo periodo di tempo.                                                          | Un'altra variante del tipo di animazione usata in **Idle2 \_ 1.**                                                                                                                                                       |
| **Inattivo3 \_ 1**                     | Quando il carattere è rimasto inattivo per molto tempo.                                                        | Sbadigli di caratteri.                                                                                                                                                                                                       |
| **Inattivo3 \_ 2**                     | Quando il carattere è rimasto inattivo per molto tempo.                                                        | Il carattere sosmette o mette le cuffia per ascoltare la musica. Nota: questa animazione passa a un fotogramma intermedio che si verifica dopo lo spostamento del carattere in una posizione appropriata.<br/>                          |
| **LookDown**                     | Quando il carattere deve guardare in basso.                                                                   | Il carattere è in basso.                                                                                                                                                                                                  |
| **LookLeft**                     | Quando il carattere deve essere visualizzato a sinistra.                                                                   | Il carattere è a sinistra.                                                                                                                                                                                           |
| **LookRight**                    | Quando il carattere deve essere visualizzato a destra.                                                                  | Il carattere è a destra.                                                                                                                                                                                          |
| **Ricerca**                       | Quando il carattere deve essere ricercato.                                                                     | Il carattere cerca.                                                                                                                                                                                                    |
| **MoveDown**                     | Quando il carattere si prepara per lo spostamento verso il basso.                                                                | Il carattere passa a una posizione di discesa a piedi o in discesa.                                                                                                                                                               |
| **MoveLeft**                     | Quando il carattere si prepara per lo spostamento a sinistra.                                                                | Il carattere passa a una posizione a sinistra a piedi o in posizione sinistra.                                                                                                                                                               |
| **MoveRight**                    | Quando il carattere si prepara per lo spostamento a destra.                                                               | Il carattere passa a una posizione a piedi/a destra.                                                                                                                                                              |
| **MoveUp**                       | Quando il carattere si prepara per lo spostamento verso l'alto.                                                                  | Il carattere passa a una posizione di passaggio verso l'alto.                                                                                                                                                                 |
| **Ora**<sup>1,2</sup>        | Quando il carattere è soddisfatto della richiesta o della scelta dell'utente.                                         | Smile di caratteri.                                                                                                                                                                                                      |
| **Processo**                      | Quando il carattere esegue un tipo di attività generica.                                                   | Il carattere preme i pulsanti o usa un tipo di strumento.                                                                                                                                                                   |
| **Elaborazione in corso**                   | Quando il carattere è occupato a lavorare su un'attività generica.                                                    | Il carattere si scarabocchi su un foglio di carta o usa un tipo di strumento. Nota: questa animazione esegue il ciclo fino a un fotogramma intermedio che si verifica dopo che il carattere si sposta in una posizione appropriata.<br/>                      |
| **Lettura**                         | Quando il carattere legge qualcosa per l'utente.                                                          | Il carattere visualizza libro o carta, legge e esamina l'utente.                                                                                                                                                       |
| **ReadContinued**                | Quando il carattere legge ulteriormente l'utente.                                                            | Il carattere legge di nuovo e quindi esamina l'utente.                                                                                                                                                                        |
| **ReadReturn**                   | Quando il carattere completa **l'animazione Read** **o ReadContinued.**                                | Il carattere torna alla posizione neutra.                                                                                                                                                                             |
| **Lettura**                      | Quando il carattere legge un elemento ma non può accettare l'input.                                              | Il carattere legge da un foglio di carta. Nota: questa animazione passa a uno o più fotogrammi intermedi che si verificano dopo che il carattere si sposta in una posizione appropriata.<br/>                                           |
| **RestPose**                     | Quando il carattere parla dalla posizione neutra.                                                     | Il carattere è l'acronimo di relaxed but relaxed posture.                                                                                                                                                                   |
| **Sad**<sup>1,2</sup>            | Quando il carattere è dispiaciuto con la scelta dell'utente.                                               | Il carattere si accrende o sembra insoddis dispiaciuto.                                                                                                                                                                                |
| **Ricerca**                       | Quando il carattere cerca qualcosa.                                                                   | Il carattere passa attraverso il pannello dei file o un altro contenitore alla ricerca di qualcosa.                                                                                                                                       |
| **Ricerca**                    | Quando il carattere cerca informazioni specificate dall'utente.                                              | Il carattere passa attraverso il pannello dei file o un altro contenitore alla ricerca di qualcosa. Nota: questa animazione passa a uno o più fotogrammi intermedi che si verificano dopo che il carattere si sposta in una posizione appropriata.<br/> |
| **Mostra**                         | Quando il carattere viene avviato o viene restituito dopo essere stato ripartito.                                            | Il carattere si apre in una nuvola di fumi, trave o entra sullo schermo.                                                                                                                                                    |
| **StartListening**<sup>1,2</sup> | Quando il carattere è in ascolto.                                                                         | Il carattere mette la mano all'ascolto.                                                                                                                                                                                            |
| **StopListening**<sup>1,2</sup>  | Quando il carattere smette di essere in ascolto.                                                                      | Il carattere mette le mani sopra le mani.                                                                                                                                                                                        |
| **Suggerisci**<sup>1,2</sup>        | Quando il carattere contiene una mancia o un suggerimento per l'utente.                                                 | Accanto al carattere viene visualizzata la lampadina.                                                                                                                                                                                  |
| **Sorprendo**<sup>1,2</sup>      | Quando il carattere è sorpreso dall'azione o dalla scelta dell'utente.                                          | Il carattere ampi gli occhi, apre la sguardo.                                                                                                                                                                                    |
| **Si pensi**<sup>a 1,2</sup>          | Quando il carattere sta pensando a qualcosa.                                                          | Il carattere cerca e tiene la mano sulla testa.                                                                                                                                                                             |
| **Incerto**<sup>1,2</sup>      | Quando il carattere richiede all'utente di confermare una richiesta.                                                  | Character looks quizzical, conveys ("Are you sure?")                                                                                                                                                                   |
| **Wave**<sup>1,2</sup>           | Quando l'utente sceglie di arrestare il server o il sistema.                                                 | Onde di caratteri good-bye o hello.                                                                                                                                                                                     |
| **Scrittura**                        | Quando il carattere è in ascolto delle istruzioni dell'utente.                                          | Il carattere visualizza la carta, scrive e esamina l'utente.                                                                                                                                                              |
| **WriteContinued**               | Quando il carattere continua ad ascoltare le istruzioni dell'utente.                                   | Il carattere scrive su un foglio di carta e esamina l'utente.                                                                                                                                                           |
| **WriteReturn**                  | Quando il carattere completa **l'animazione** **Write o WriteContinued.**                              | Il carattere torna alla posizione neutra.                                                                                                                                                                             |
| **Scrittura**                      | Quando il carattere scrive informazioni per l'utente.                                                  | Scrittura di caratteri su un foglio di carta. Nota: questa animazione esegue cicli.<br/>                                                                                                                                             |



 

  L'animazione richiede sovrimpressione a sovrimpressione e un frame di pronuncia definito.

  L'animazione richiede un'animazione Return assegnata in base alla diramazione di uscita o a un'animazione Return esplicita.

Inoltre, un carattere deve avere le assegnazioni di stato seguenti.



| State          | Animazioni necessarie                           |
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
| Ascolto      | Avviso                                         |
| MovingDown     | MoveDown                                      |
| Spostamentoleft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| Spostamento in avanti       | MoveUp                                        |
| Visualizzazione        | Mostra                                          |
| Parlando       | RestPose                                      |



 

 

 





