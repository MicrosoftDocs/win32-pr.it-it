---
title: Chiarire e limitare le scelte
description: Chiarire e limitare le scelte
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953001d706089244d6366c8dab0cdb580a2d72ca
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118476"
---
# <a name="clarify-and-limit-choices"></a>Chiarire e limitare le scelte

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il riconoscimento vocale diventa più efficace quando l'utente apprende l'intervallo di grammatica appropriato. Funziona anche meglio quando la gamma di scelte è limitata. Meno aperto è l'input, migliore sarà il motore di riconoscimento vocale in grado di analizzare l'input di informazioni acustiche.

Microsoft Agent include diverse disposizioni incorporate che aumentano il successo dell'input vocale. La prima è la finestra comandi visualizzata quando l'utente dice "Apri finestra comandi" o "Cosa posso dire?" (o quando l'utente sceglie Apri finestra comandi dal menu a comparsa del carattere). La finestra di comando funge da guida visiva alla grammatica attiva del motore di riconoscimento vocale. Riduce inoltre gli errori di riconoscimento attivando solo la grammatica vocale dell'applicazione attiva di input e i comandi globali di Microsoft Agent. Pertanto, la grammatica attiva del motore di riconoscimento vocale si applica al contesto immediato. Per altre informazioni sulla finestra Comandi, vedere Panoramica [dell'interfaccia di programmazione di Microsoft Agent.](microsoft-agent-programming-interface-overview.md)

Quando si creano comandi abilitati per la voce di Microsoft Agent, è possibile creare il testo della didascalia visualizzato nella finestra comandi e il relativo testo vocale (grammatica), ovvero le parole che il motore deve usare per trovare la corrispondenza con questo comando. Provare sempre a rendere i comandi il più distintivi possibile. Maggiore è la differenza tra la formulazione dei comandi, in particolare per il testo vocale, maggiore è la probabilità che il motore di riconoscimento vocale sia in grado di discriminare tra i comandi vocali e fornire una corrispondenza accurata. Evitare anche comandi con una sola parola o molto brevi. In genere, un maggior numero di informazioni acustiche in un'espressione parlata offre al motore una migliore possibilità di ottenere una corrispondenza accurata.

Quando si definisce il testo vocale per un comando, fornire un'ampia gamma di formulazioni. Le richieste che hanno lo stesso significato possono essere formulate in modo molto diverso, come illustrato nell'esempio seguente:

Aggiungere un po' di pepperoni.

I'd like some pepperoni.

È possibile aggiungere un po' di salame?

Pepperoni, please.

Microsoft Agent consente di specificare facilmente alternative o parole facoltative per la grammatica vocale per l'applicazione. È possibile racchiudere parole o frasi alternative tra parentesi, separate da un carattere barra verticale. È possibile definire parole facoltative racchiudendole tra parentesi quadre. È anche possibile annidare alternative o parole facoltative. È anche possibile usare i puntini di sospensione (...) nel testo vocale come segnaposto per qualsiasi parola. Tuttavia, l'uso troppo frequente dei puntini di sospensione può rendere più difficile per il motore distinguere tra comandi vocali diversi. In ogni caso, assicurarsi sempre che il testo vocale includa almeno una parola distintiva per ogni comando non facoltativo. In genere, deve corrispondere a una o più parole nel testo della didascalia definito visualizzato nella finestra Comandi.

Anche se è possibile includere simboli, punteggiatura o abbreviazioni nel testo della didascalia, evitarli nel testo vocale. Molti motori di riconoscimento vocale non possono gestire simboli e abbreviazioni o possono usarli per impostare parametri di input speciali. È anche possibile scrivere i numeri. In questo modo si garantisce anche un supporto di riconoscimento più affidabile.

È anche possibile usare richieste di direttiva per evitare input aperto. Le richieste di direttiva fanno riferimento in modo implicito alle scelte o le dichiarano in modo esplicito, come illustrato negli esempi seguenti:



| Prompt                                           | Valutazione                                                    |
|--------------------------------------------|-----------------------------------------------------|
| Cosa vuoi?                          | Troppo generale, una richiesta aperta                  |
| Scegliere uno stile o un ingrediente per la pizza.        | Buona, se le scelte sono visibili, ma comunque generali     |
| Pronunciare "Chicago", "Chicago" o "The Works". | Meglio, una direttiva esplicita con opzioni specifiche |



 

Questo guida l'utente verso l'esecuzione di un comando valido. Suggerendo le parole o la frase, è più probabile che si ritieni in cambio la formulazione prevista. Per evitare ripetitività innaturale, modificare la formulazione o abbreviare l'originale per la presentazione successiva man appena l'utente diventa più esperto con lo stile di input. I prompt delle direttive possono essere usati anche in situazioni in cui l'utente non riesce a eseguire un comando entro un periodo prestabilito o non riesce a fornire un comando previsto. Le richieste di direttiva possono essere fornite usando l'output vocale, le interfacce dell'applicazione o entrambi. La chiave è aiutare l'utente a conoscere le scelte appropriate.

La formulazione influenza il successo di una richiesta. Ad esempio, il prompt "Would you like to order your pizza?" potrebbe generare una risposta "Sì" o "No", ma potrebbe anche generare una richiesta di ordine. Definire le richieste in modo che siano non ambigue o prepararsi ad accettare una più ampia gamma di possibili risposte. Si noti anche la tendenza delle persone a simulare le parole e i costrutti che udino. Questo può essere spesso usato per aiutare a ottenere una risposta appropriata, come nell'esempio seguente:

**Utente:** Mostrami tutti i messaggi di Paul.

**Carattere:**

È più probabile che il nome completo di una delle parti sia preceduto dal prefisso "Intendevo" o "Intendevo".

Poiché i caratteri di Microsoft Agent operano all'interno dell'interfaccia visiva di Microsoft Windows, è possibile usare gli elementi visivi per fornire richieste di direttiva per l'input vocale. Ad esempio, è possibile fare in modo che il movimento del carattere sia in un elenco di scelte e richiedere all'utente di selezionarne una o di visualizzare le scelte in una finestra di dialogo o di messaggio. Ciò offre due vantaggi: suggerisce in modo esplicito le parole che l'utente deve pronunciare e offre un modo alternativo per rispondere.

È anche possibile usare altre modalità di interazione per suggerire agli utenti la grammatica vocale appropriata, come illustrato nell'esempio seguente:

**Utente:** (fa clic sull'opzione pizza di tipo napoletano con il mouse)

**Carattere:** Pizza in stile napoletano.

**Utente:** (fa clic sull'opzione Extra Cheese con il mouse)

**Carattere:** Aggiungere "Extra Cheese".

Un altro fattore importante per la riuscita dell'input vocale è il segnale dell'utente quando il motore è pronto per l'input, perché molti motori vocali consentono una sola espressione alla volta. Microsoft Agent offre supporto per questa operazione in due modi. In primo luogo, se la scheda audio supporta MIDI, Microsoft Agent genera un breve segnale quando il canale di input vocale è disponibile. In secondo momento, nella finestra Suggerimento per l'ascolto viene visualizzata una richiesta di testo appropriata quando il carattere (motore di riconoscimento vocale) è in ascolto dell'input. Inoltre, questo suggerimento visualizza ciò che il motore ha sentito.

 

 




