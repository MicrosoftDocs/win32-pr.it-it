---
title: Chiarire e limitare le scelte
description: Chiarire e limitare le scelte
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ed5f95c2e516f304ffa28bcca1d9fd67a9169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298673"
---
# <a name="clarify-and-limit-choices"></a>Chiarire e limitare le scelte

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il riconoscimento vocale diventa più efficace quando l'utente apprende l'intervallo di grammatica appropriato. Funziona inoltre meglio quando l'intervallo di scelte è limitato. Minore è il numero di input aperto, più il motore vocale può analizzare l'input di informazioni acustiche.

Microsoft Agent include diverse clausole predefinite che aumentano la riuscita dell'input vocale. Il primo è la finestra dei comandi visualizzata quando l'utente dice "Apri finestra comandi" o "cosa posso dire?" (o quando l'utente sceglie la finestra Apri comandi dal menu popup del carattere). La finestra di comando funge da guida visiva alla grammatica attiva del motore di riconoscimento vocale. Consente inoltre di ridurre gli errori di riconoscimento attivando solo la grammatica vocale dei comandi globali dell'applicazione input-Active e di Microsoft Agent. Pertanto, la grammatica attiva del motore di riconoscimento vocale si applica al contesto immediato. Per ulteriori informazioni sulla finestra comandi, vedere [Cenni preliminari sull'interfaccia di programmazione Microsoft Agent](microsoft-agent-programming-interface-overview.md).

Quando si creano comandi abilitati per la voce di Microsoft Agent, è possibile creare il testo della didascalia visualizzato nella finestra comandi e il testo vocale (grammatica), ovvero le parole che il motore deve usare per la corrispondenza di questo comando. Provare sempre a rendere i comandi più distinti possibile. Maggiore è la differenza tra la formulazione dei comandi, in particolare per il testo vocale, più probabilmente il motore vocale sarà in grado di distinguere tra i comandi vocali e fornire una corrispondenza accurata. È anche possibile evitare comandi a parola singola o molto breve. In generale, le informazioni acustiche in un'espressione pronunciata forniscono al motore una migliore probabilità di ottenere una corrispondenza precisa.

Quando si definisce il testo vocale per un comando, fornire un'ampia gamma di parole. Le richieste che significano la stessa cosa possono essere formulate in modo molto diverso, come illustrato nell'esempio seguente:

Aggiungere alcuni peperoni.

Vorrei un po' di peperoni.

È possibile aggiungere alcuni peperoni?

Pepperone,

Microsoft Agent consente di specificare facilmente alternative o parole facoltative per la grammatica vocale per l'applicazione. Racchiudere le parole o le frasi alternative tra parentesi separate da un carattere di barra verticale. È possibile definire parole facoltative racchiudendo i caratteri tra parentesi quadre. È anche possibile annidare alternative o parole facoltative. Inoltre, è possibile utilizzare i puntini di sospensione (...) nel testo vocale come segnaposto per qualsiasi parola. Tuttavia, l'uso troppo frequente dei puntini di sospensione potrebbe rendere più difficile la distinzione tra i diversi comandi vocali del motore. In ogni caso, assicurarsi sempre che il testo vocale includa almeno una parola distinta per ogni comando che non è facoltativo. In genere, questo deve corrispondere a una parola o a parole nel testo della didascalia definito che viene visualizzato nella finestra dei comandi.

Sebbene sia possibile includere simboli, punteggiatura o abbreviazioni nel testo della didascalia, evitarli nel testo vocale. Molti motori di riconoscimento vocale non possono gestire simboli e abbreviazioni oppure possono usarli per impostare parametri di input speciali. Inoltre, vengono digitati i numeri. Questo garantisce anche un supporto per il riconoscimento più affidabile.

È anche possibile usare i prompt della direttiva per evitare input aperti. I prompt della direttiva fanno riferimento in modo implicito alle scelte o lo dichiarano in modo esplicito, come illustrato negli esempi seguenti:



|                                            |                                                     |
|--------------------------------------------|-----------------------------------------------------|
| Cosa vuoi?                          | Troppo generale, una richiesta aperta                  |
| Scegliere uno stile o un ingrediente per la pizza.        | Bene, se le scelte sono visibili, ma ancora generali     |
| Pronunciare "Hawaiian", "Chicago" o "The Works". | Migliore, una direttiva esplicita con opzioni specifiche |



 

In questo modo l'utente viene indirizzato per l'invio di un comando valido. Suggerendo parole o frasi, è più probabile che si tratti di una formulazione prevista in return. Per evitare la ripetibilità non naturale, modificare il testo o abbreviare l'originale per la presentazione successiva quando l'utente diventa più esperto con lo stile di input. I prompt della direttiva possono essere usati anche nelle situazioni in cui l'utente non riesce a emettere un comando entro un periodo di tempo previsto o non fornisce un comando previsto. I prompt della direttiva possono essere forniti usando l'output vocale, le interfacce dell'applicazione o entrambi. La chiave sta aiutando l'utente a comprendere le scelte appropriate.

Il wording influisce sull'esito positivo di una richiesta. Ad esempio, la richiesta "si vuole ordinare la pizza?" potrebbe generare una risposta "Yes" o "No", ma potrebbe anche generare una richiesta di ordine. Definire richieste non ambigue o essere pronte ad accettare una maggiore varietà di risposte possibili. Si noti inoltre la tendenza per le persone a simulare parole e costrutti che ascoltano. Questo può essere usato spesso per aiutare a evocare una risposta appropriata come nell'esempio seguente:



|            |                                 |
|------------|---------------------------------|
| Utente:      | Mostra tutti i messaggi di Paul. |
| Carattere |                                 |



 

È più probabile che il nome completo di una delle parti venga determinato con il prefisso "I mean" o "I means".

Poiché i caratteri di Microsoft Agent operano all'interno dell'interfaccia visiva di Microsoft Windows, è possibile usare gli elementi visivi per fornire i prompt della direttiva per l'input vocale. Ad esempio, è possibile impostare il carattere su un elenco di scelte e richiedere che l'utente ne selezioni uno oppure visualizzare le scelte in una finestra di dialogo o in una finestra di messaggio. Questo offre due vantaggi: suggerisce esplicitamente le parole che si desidera che l'utente parli e fornisce un modo alternativo per rispondere all'utente.

È anche possibile usare altre modalità di interazione per suggerire leggermente agli utenti la grammatica vocale appropriata, come illustrato nell'esempio seguente:



|            |                                                     |
|------------|-----------------------------------------------------|
| Utente:      | (Fare clic sull'opzione della pizza in stile hawaiano con il mouse) |
| Carattere | Pizza in stile hawaiano.                               |
| Utente:      | (Fare clic sull'opzione di formaggio aggiuntivo con il mouse)         |
| Carattere | Aggiungere "Cheese aggiuntivo".                                 |



 

Un altro fattore importante nella riuscita dell'input vocale è la messa a punto dell'utente quando il motore è pronto per l'input, perché molti motori di riconoscimento vocale consentono una sola espressione alla volta. Microsoft Agent fornisce supporto per questa operazione in due modi. Prima di tutto, se la scheda audio supporta MIDI, Microsoft Agent genera un breve segnale acustico quando il canale di input vocale è disponibile. In secondo luogo, la finestra del suggerimento di ascolto Visualizza una richiesta di testo appropriata quando il carattere (motore vocale) è in ascolto dell'input. Inoltre, questo suggerimento Visualizza il contenuto del motore.

 

 




