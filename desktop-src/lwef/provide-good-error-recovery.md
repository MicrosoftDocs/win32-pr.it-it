---
title: Fornire un ripristino corretto degli errori
description: Fornire un ripristino corretto degli errori
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2abc32e1bdf6422e2d8d6422a17e0b881c6ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043965"
---
# <a name="provide-good-error-recovery"></a>Fornire un ripristino corretto degli errori

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Come per qualsiasi interfaccia ben progettata, il processo interattivo dovrebbe ridurre al minimo le circostanze che causano errori. Tuttavia, raramente è possibile eliminare tutti gli errori, pertanto il supporto del ripristino degli errori valido è essenziale per mantenere la confidenza e l'interesse dell'utente. In generale, il ripristino degli errori comporta il rilevamento di un errore, la determinazione della cause e la definizione di un modo per risolvere l'errore. Gli utenti rispondono meglio alle interfacce cooperative, che interagiscono con l'utente per eseguire un'attività.

Il primo passaggio del ripristino degli errori di riconoscimento vocale è il rilevamento della condizione di errore. Il riconoscimento vocale può avere esito negativo a causa di diversi errori. Le condizioni di errore possono in genere essere rilevate come risultato di input non valido, correzione esplicita dell'utente o annullamento o ripetizione dell'utente.

Si verifica un *errore di rifiuto* quando il motore di riconoscimento non corrisponde a quello indicato dall'utente. I rumori di fondo o le fasi iniziali sono anche cause comuni degli errori di riconoscimento, quindi chiedere all'utente di ripetere un comando è spesso una soluzione iniziale efficace. Tuttavia, se la frase è esterna alla grammatica attiva corrente, chiedere all'utente di riformulare la richiesta potrebbe risolvere il problema. La differenza nel wording può comportare una corrispondenza con qualcosa nella grammatica corrente. Elencare o suggerire le opzioni di input previste appropriate è un'altra alternativa.

Una buona strategia per il ripristino degli errori di rifiuto consiste nel combinare queste tecniche per riportare l'utente alla traccia, offrendo sempre più assistenza se l'errore è permanente. Ad esempio, è possibile iniziare rispondendo all'errore iniziale con un interrogatorio come "huh?" o "cosa?" o un gesto da mano a orecchio. Una risposta breve aumenta la probabilità che l'istruzione ripetuta dell'utente non abbia esito negativo perché l'utente ha parlato troppo A breve. In seguito a un errore ripetuto, la richiesta successiva di riformulare migliora la probabilità di corrispondenza di un elemento all'interno della grammatica specificata. Da qui, l'invio di richieste esplicite di comandi accettati aumenta ulteriormente la probabilità di una corrispondenza. Questa tecnica è illustrata nell'esempio seguente:



|            |                                                                            |
|------------|----------------------------------------------------------------------------|
| Utente:      | Vorrei una pizza di tipo Chicago con acciughe.                             |
| Carattere | (Da mano a orecchio) Eh?                                                         |
| Utente:      | Voglio una pizza Chicago con acciughe.                                     |
| Carattere | (Scuotimento Head) Riformulare la richiesta.                                 |
| Utente:      | Ho detto Chicago Pizza, con acciughe.                                      |
| Carattere | Scrollata Mi dispiace. È possibile indicare lo stile della pizza desiderata.                    |
| Utente:      | Chicago, con acciughe.                                                   |
| Carattere | Non ci sono ancora fortuna. Ecco cosa si può dire: "Chicago", "hawaiano" o "combinato". |



 

Per far sì che la gestione degli errori risulti più naturale, assicurarsi di fornire un livello di variazione casuale quando si risponde agli errori. Inoltre, una reazione utente naturale a qualsiasi richiesta di ripetizione di una risposta consiste nell'esagerare o aumentare il volume quando si ripete l'istruzione. Potrebbe essere utile ricordare occasionalmente all'utente di parlare normalmente e chiaramente, poiché l'esagerazione o un volume maggiore può rendere più difficile il riconoscimento delle parole da parte del motore di riconoscimento vocale.

L'assistenza progressiva dovrebbe eseguire più di un errore nell'attenzione dell'utente. per consentire all'utente di parlare con la grammatica corrente, è necessario fornire più messaggi informativi. Le interfacce che sembrano provare a comprendere incoraggiano un livello elevato di soddisfazione e tolleranza da parte dell'utente.

Gli *errori di sostituzione*, in cui il motore di riconoscimento vocale riconosce l'input ma corrisponde al comando errato, sono più difficili da risolvere perché il motore vocale rileva un espressione corrispondente. Una mancata corrispondenza può verificarsi anche quando il motore di riconoscimento vocale interpreta i suoni estranei come input valido (noto anche come *errore di inserimento*). In queste situazioni, l'assistenza dell'utente è necessaria per identificare la condizione di errore. A tale scopo, è possibile ripetere le operazioni restituite dal motore di riconoscimento vocale e richiedere conferma all'utente prima di procedere:



|            |                                                   |
|------------|---------------------------------------------------|
| Utente:      | Preferisco una pizza di tipo Chicago.                   |
| Carattere | Hai detto che vuoi una "pizza in stile Chicago"?   |
| Utente:      | Sì.                                              |
| Carattere | Quali sono gli altri ingredienti desiderati? |
| Utente:      | Acciughe.                                        |
| Carattere | Hai detto "acciughe"?                          |
| Utente:      | Sì.                                              |



 

Tuttavia, l'utilizzo di questa tecnica per ogni espressione diventa inefficiente e noioso. Per gestire questo problema, limitare la conferma a situazioni che presentano conseguenze negative significative o aumentare la complessità dell'attività immediata. Se è facile per l'utente eseguire o annullare le modifiche, è possibile evitare di richiedere la conferma delle scelte. Analogamente, se si rendono visibili le scelte, potrebbe non essere necessario fornire la correzione esplicita. Ad esempio, la scelta di un elemento da un elenco potrebbe non richiedere la verifica perché l'utente può visualizzare i risultati e modificarli facilmente. È anche possibile usare la confidenza e i punteggi alternativi per fornire una soglia per la conferma. È possibile modificare la soglia mantenendo una cronologia delle azioni dell'utente in una determinata situazione ed eliminando la verifica in base alla conferma dell'utente coerente. Infine, si consideri la natura multimodale dell'interfaccia. Potrebbe anche essere opportuno confermare il mouse o la tastiera.

Scegliere con attenzione il testo delle conferme. Ad esempio, "hai detto...?" o "Credo che tu abbia detto..." è preferibile che "si vuole davvero...?" Poiché le frasi precedenti implicano che l'accuratezza dell'ascolto del carattere (riconoscimento) viene sottoposta a query, non è possibile che l'utente abbia parlato.

Prendere in considerazione anche la grammatica per una risposta. Ad esempio, è probabile che una risposta negativa generi un errore di rifiuto, richiedendo un prompt aggiuntivo, come illustrato nell'esempio seguente:



|            |                          |
|------------|--------------------------|
| Utente:      | Vorrei un po' di peperoni. |
| Carattere | Hai detto "No Ham"?    |
| Utente:      | No, ho detto peppery.    |
| Carattere | Questo perché                     |
| Utente:      | Peperoni.               |



 

La modifica della grammatica per includere i prefissi per gestire le variazioni della risposta naturale aumenta l'efficienza del processo di ripristino, soprattutto quando l'utente non conferma la richiesta di verifica. In questo esempio, la conferma potrebbe essere stata gestita in un unico passaggio modificando la grammatica per il "Pepperone", includendo anche "No ho detto Pepperone", "ho detto Pepperino" e "No Pepperone".

È anche possibile gestire gli errori di sostituzione usando le corrispondenze alternative restituite dal motore vocale come conferma correttiva:



|           |                                                                                        |
|-----------|----------------------------------------------------------------------------------------|
| User      | Vorrei un po' di peperoni.                                                               |
| Carattere | ("No Ham" come migliore corrispondenza, "Pepperone" come prima alternativa) Hai detto "No Ham"? |
| User      | No, peppery.                                                                         |
| Carattere | ("Nessun prosciutto" viene comunque trovato come corrispondenza migliore, ma ora offre la prima alternativa) "Peperoni"?    |



 

Analogamente, è possibile gestire una cronologia degli errori di sostituzione comuni e, in caso di frequente errore, offrire l'alternativa la prima volta.

In qualsiasi situazione di errore di riconoscimento, evitare di incolpare l'utente. Se il carattere suggerisce o addirittura implica che l'utente deve incolpare o se il carattere non è diverso dall'errore, l'utente potrebbe essere danneggiato. Inoltre, scegliere con attenzione la formulazione che accetta esplicitamente la responsabilità, è appropriata per la situazione e usa la varietà per creare una risposta più naturale. Quando si esprimono le scuse, evitare parole ambigue, ad esempio "Oops" o "Ehm-Oh", che potrebbero essere interpretate come la colpa dell'utente. Usare invece frasi come "Mi dispiace" o "mio errore". Gli errori ripetuti o più gravi potrebbero usare un'apologia più elaborata, ad esempio "sono molto spiacente". Prendere in considerazione anche la personalità del carattere quando si determina il tipo di risposta. Un'altra opzione è la responsabilità di una situazione esterna. I commenti, ad esempio, "Boy", sono fastidiosi, "si è distolti dall'utente e dal carattere. Potrebbe essere utile tenere presente che l'utente della natura cooperativa dell'interazione può essere utile: considerare frasi come, "vediamo cosa possiamo fare per realizzare questo lavoro".

Microsoft Agent supporta inoltre alcuni commenti e suggerimenti automatici per il riconoscimento. Quando viene rilevato un enunciato, il suggerimento di ascolto Visualizza il testo vocale della migliore corrispondenza. È possibile impostare il testo da visualizzare in base all'impostazione di confidenza per un comando definito.

A causa del potenziale errore, è sempre necessario confermare le scelte con gravi conseguenze negative e sono irreversibili. Naturalmente, è opportuno richiedere una conferma quando i risultati di un'azione potrebbero essere distruttivi. Tuttavia, prendere in considerazione anche la richiesta di conferma per le situazioni che interrompono qualsiasi processo o operazione di lunga durata.

 

 




