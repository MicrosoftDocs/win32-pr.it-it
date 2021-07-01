---
title: Fornire un buon ripristino degli errori
description: Fornire un buon ripristino degli errori
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a20a3d203ab0fcd93a6f4645be4af44b049f3cd
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120796"
---
# <a name="provide-good-error-recovery"></a>Fornire un buon ripristino degli errori

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Come per qualsiasi interfaccia ben progettata, il processo interattivo deve ridurre al minimo le circostanze che possono causare errori. Tuttavia, è raramente possibile eliminare tutti gli errori, quindi il supporto di un buon ripristino degli errori è essenziale per mantenere l'attendibilità e l'interesse dell'utente. In generale, il ripristino degli errori comporta il rilevamento di un errore, la determinazione della causa e la definizione di un modo per risolvere l'errore. Gli utenti rispondono meglio alle interfacce cooperativi che collaborano con l'utente per eseguire un'attività.

Il primo passaggio nel ripristino degli errori vocali consiste nel rilevare la condizione di errore. Il riconoscimento vocale può non riuscire a causa di un'ampia gamma di errori. Le condizioni di errore possono in genere essere rilevate come risultato di input non valido, correzione esplicita dell'utente o annullamento o ripetizione dell'utente.

Un *errore di rifiuto* si verifica quando il motore di riconoscimento non corrisponde a quanto detto dall'utente. Il rumore di fondo o gli avviati anticipati sono anche cause comuni di errori di riconoscimento, quindi chiedere all'utente di ripetere un comando è spesso una buona soluzione iniziale. Tuttavia, se la frase non è in linea con la grammatica attiva corrente, chiedere all'utente di riformorare la richiesta può risolvere il problema. La differenza nella formulazione può comportare una corrispondenza con qualcosa nella grammatica corrente. L'inserzione o il suggerimento di opzioni di input previste appropriate è un'altra alternativa.

Una buona strategia per il ripristino degli errori di rifiuto consiste nel combinare queste tecniche per far tornare in funzione l'utente, offrendo sempre più assistenza se l'errore persiste. Ad esempio, è possibile iniziare rispondendo all'errore iniziale con un interrogativo come "Eh?" o "What?" o un movimento da mano a mano all'udito. Una risposta breve aumenta la probabilità che l'istruzione ripetuta dell'utente non avrà esito negativo perché l'utente ha parlato troppo presto. In caso di errore ripetuto, la richiesta successiva di ridefinire migliora le probabilità di corrispondenza di un elemento all'interno della grammatica specificata. Da qui, fornire richieste esplicite di comandi accettati aumenta ulteriormente le probabilità di corrispondenza. Questa tecnica è illustrata nell'esempio seguente:

**Utente:** mi piace una pizza in stile Chicago con acciughe.

**Carattere**: (Hand to Ear) Eh?

**Utente:** voglio una pizza di Chicago con acciughe.

**Carattere**: (Head shake) Riformizza la richiesta.

**Utente:** ho detto Pizza di Chicago, con acciughe.

**Carattere**: (Shrug) Mi spiace. Indicare lo stile di pizza desiderato.

**Utente:** Chicago, con acciughe.

**Carattere:** ancora nessuna fortuna. Ecco cosa si può dire: "Chicago", "Hawaiano" o "Combo".

Per rendere la gestione degli errori più naturale, assicurarsi di fornire un grado di variazione casuale quando si risponde agli errori. Inoltre, una reazione dell'utente naturale a qualsiasi richiesta di ripetizione di una risposta è esagerare o aumentare il volume quando si ripete l'istruzione. Può essere utile ricordare occasionalmente all'utente di parlare normalmente e chiaramente, poiché l'esagerazione o l'aumento del volume può rendere più difficile al motore vocale riconoscere le parole.

L'assistenza progressiva deve fare di più che portare l'errore all'attenzione dell'utente; dovrebbe guidare l'utente verso la pronuncia nella grammatica corrente fornendo successivamente messaggi più informativi. Le interfacce che sembrano tentare di comprendere incoraggiano un elevato grado di soddisfazione e tolleranza da parte dell'utente.

*Gli errori di sostituzione,* in cui il motore di riconoscimento vocale riconosce l'input ma corrisponde al comando errato, sono più difficili da risolvere perché il motore di riconoscimento vocale rileva un'espressione corrispondente. Una mancata corrispondenza può verificarsi anche quando il motore di riconoscimento vocale interpreta i suoni estranei come input valido (noto anche come errore *di inserimento*). In queste situazioni è necessaria l'assistenza dell'utente per identificare la condizione di errore. A tale scopo, è possibile ripetere ciò che il motore di riconoscimento vocale ha restituito e chiedere all'utente di confermarlo prima di procedere:

**Utente:** mi piace una pizza in stile Chicago.

**Carattere:** si è detto che si desidera una "pizza in stile Chicago"?

**Utente**: Sì.

**Carattere:** quali altri ingredienti si desiderano?

**Utente**: Acciughe.

**Carattere:** hai detto "acciughe"?

**Utente**: Sì.

Tuttavia, l'uso di questa tecnica per ogni espressione diventa inefficiente e noioso. Per gestire questo problema, limitare la conferma a situazioni con conseguenze negative significative o aumentare la complessità dell'attività immediata. Se è facile per l'utente apportare o annullare le modifiche, è possibile evitare di richiedere la conferma delle proprie scelte. Analogamente, se si effettuano scelte visibili, potrebbe non essere necessario fornire una correzione esplicita. Ad esempio, la scelta di un elemento da un elenco potrebbe non richiedere la verifica perché l'utente può visualizzare i risultati e modificarli facilmente. È anche possibile usare l'attendibilità e i punteggi alternativi per fornire una soglia per la conferma. È possibile modificare la soglia mantenendo una cronologia delle azioni dell'utente in una determinata situazione ed eliminando la verifica in base alla conferma dell'utente coerente. Infine, considerare la natura multimodale dell'interfaccia. Anche la conferma dal mouse o dalla tastiera potrebbe essere appropriata.

Scegliere con attenzione la formulazione delle conferme. Ad esempio, "Hai detto...?" o "I think you said..." sono migliori di "Vuoi davvero...?" poiché le frasi precedenti implicano che viene eseguita una query sull'accuratezza dell'ascolto (riconoscimento) del carattere, non che l'utente possa avere un misspoke.

Si consideri anche la grammatica per una risposta. Ad esempio, è probabile che una risposta negativa generi un errore di rifiuto, che richiede un prompt aggiuntivo, come illustrato nell'esempio seguente:

**Utente:** mi piace un po' di pepperoni.

**Carattere:** hai detto "no ham"?

**Utente:** No, ho detto pepperoni.

**Carattere:** Eh?

**Utente:** Pepperoni.

La modifica della grammatica per includere prefissi per gestire le variazioni di risposta naturale aumenta l'efficienza del processo di ripristino, soprattutto quando l'utente non conferma la richiesta di verifica. In questo esempio la conferma avrebbe potuto essere gestita in un unico passaggio modificando la grammatica per i "pepperoni" includendo anche "no I said pepperoni", "I said pepperoni" e "no pepperoni".

È anche possibile gestire gli errori di sostituzione usando le corrispondenze alternative restituite dal motore di riconoscimento vocale come conferma correttiva:

**Utente:** mi piace un po' di pepperoni.

**Carattere**: (Ascolti "no ham" come corrispondenza migliore, "pepperoni" come prima alternativa) Hai detto "no ham"?

**Utente:** No, pepperoni.

**Carattere**: (non viene ancora sentito "nessun ham" come corrispondenza migliore, ma ora offre la prima alternativa) "Pepperoni"?

Analogamente, è possibile mantenere una cronologia degli errori di sostituzione comuni e, se un errore specifico è frequente, offrire l'alternativa la prima volta.

In qualsiasi situazione di errore di riconoscimento, evitare di incolparlo. Se il carattere suggerisce o addirittura implica che l'utente è da biasimare o il carattere sembra indifferente all'errore, l'utente potrebbe essere offeso. Anche in questo caso, scegliere con attenzione la formulazione che accetta esplicitamente la responsabilità, è appropriata alla situazione e usa la varietà per creare una risposta più naturale. Quando si esprime una topologia, evitare parole ambigue come "oops" o "uh-oh" che potrebbero essere interpretate come incolpazione dell'utente. Usare invece frasi come "I'm sorry" o "My mistake". Gli errori ripetuti o più gravi potrebbero usare una topologia più elaborata, ad esempio "Sono davvero dispiaciuto". Si consideri anche la personalità del carattere quando si determina il tipo di risposta. Un'altra opzione è incolpare una situazione esterna. Commenti come "Boy, it's noisy out there", to take the blame away from the user and the character. Anche ricordare all'utente la natura cooperativa dell'interazione può essere utile: prendere in considerazione frasi come "Vediamo cosa possiamo fare per far funzionare questa operazione".

Microsoft Agent supporta anche alcuni commenti e suggerimenti automatici per il riconoscimento. Quando viene rilevata un'espressione, il suggerimento di ascolto visualizza il testo vocale della corrispondenza migliore ascoltata. È possibile impostare il testo personalizzato da visualizzare in base all'impostazione di attendibilità per un comando definito.

A causa del potenziale di errore, è sempre necessario confermare le scelte che hanno gravi conseguenze negative e sono irreversibili. Naturalmente, è necessario richiedere una conferma quando i risultati di un'azione potrebbero essere distruttivi. È tuttavia consigliabile richiedere anche una conferma per situazioni che interrompino un processo o un'operazione di lunga durata.

 

 




