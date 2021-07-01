---
description: Esaminare l'elenco di controllo per la convalida di PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Elenco di controllo per la convalida di PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6154b7cabb5825a0f0edcc8f90b8294557001f1a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120146"
---
# <a name="printticket-validation-checklist"></a>Elenco di controllo per la convalida di PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintTicket devono convalidare PrintTicket prima di usarlo per qualsiasi scopo. Dopo la convalida, PrintTicket può essere restituito al client oppure può essere eliminato dopo l'uso. Questo elenco di controllo illustra le attività che il provider deve eseguire durante la convalida. Il processo di convalida modificherà spesso il contenuto di PrintTicket, anche se non modificherà un PrintTicket convalidato in precedenza.

La convalida viene sempre eseguita su un dispositivo specifico con un set di istanze Feature, Option e ParameterDef definite in un documento PrintCapabilities. Il codice di convalida deve avere accesso al set di istanze Feature (e alle istanze Option contenute) e ParameterDef per il dispositivo specifico e non deve accedere a PrintCapabilities. Le informazioni delle istanze Feature, Option e ParameterDef sono necessarie in determinate parti del processo di convalida.

1.  Durante i tentativi di individuare gli elementi corrispondenti o corrispondenti, si noti che gli spazi dei nomi degli elementi devono corrispondere prima che qualsiasi nome completo possa essere considerato una corrispondenza. Tutti i nomi degli elementi, i nomi degli attributi e i nomi di istanza sono qualificati per lo spazio dei nomi. Per gli elementi annidati, le relative posizioni devono corrispondere prima che gli elementi siano considerati corrispondenti.

2.  Verificare che tutti i tag di elemento siano nello spazio dei nomi pubblico, siano definiti dallo schema PrintTicket, contengano gli attributi XML e i valori degli attributi appropriati e che la posizione di ogni tipo di elemento sia conforme all'utilizzo definito dallo schema PrintTicket.

3.  Determinare tutti gli spazi dei nomi segnalati dal documento PrintCapabilities. Rimuovere tutti gli elementi (e i relativi discendenti) da PrintTicket i cui nomi di istanza appartengono a spazi dei nomi non segnalati dal documento PrintCapabilities. Si noti la differenza tra questo caso e il caso seguente, che comporta nomi di istanza non riconosciuti all'interno di uno spazio dei nomi noto.

4.  Poiché gli schemi vengono continuamente estesi con l'aggiunta di nuove definizioni di istanza di elemento, il codice di convalida non deve essere scritto presupponendo che ogni nome di istanza in un determinato spazio dei nomi sia noto. Il codice di convalida non può considerare come errori i nomi di istanza non riconosciuti all'interno di uno spazio dei nomi noto né eliminarli da PrintTicket.

5.  Se un'istanza di elemento ha un elemento di pari livello duplicato non consentito dallo schema PrintTicket, mantenere solo la prima occorrenza ed eliminare i duplicati, incluso il contenuto dell'elemento duplicato.

6.  Rimuovere da PrintTicket qualsiasi funzionalità o funzionalità secondaria (e tutti i relativi elementi figlio) senza funzionalità corrispondente nel documento PrintCapabilities.

7.  Controllare la proprietà SelectionType definita nel documento PrintCapabilities per ognuna delle istanze di Feature rimanenti in PrintTicket. Qualsiasi funzionalità la cui proprietà SelectionType è impostata su PickOne deve avere esattamente un'istanza Option presente in PrintTicket, mentre una funzionalità la cui proprietà SelectionType è PickMany può avere più di una. Se per una funzionalità PrintTicket non è presente un'istanza Option, specificare l'istanza predefinita di Option. Poiché si è il provider, si sa quale opzione è l'opzione predefinita per ogni funzionalità.

    Per una funzionalità la cui proprietà SelectionType è PickMany, con più opzioni selezionate in PrintTicket, verificare che nessuna opzione sia designata come IdentityOption. In caso contrario, eliminare ogni altra opzione, lasciando solo quella designata IdentityOption.

8.  Rimuovere qualsiasi istanza ParameterInit in PrintTicket che non dispone di alcuna istanza ParameterDef corrispondente nel documento PrintCapabilities.

    Per qualsiasi altra istanza ParameterInit in PrintTicket, verificare che il valore di ogni sia conforme all'istanza ParameterDef del documento PrintCapabilities. Se manca un valore, specificare il valore predefinito specificato in ParameterDef.

9.  Associare ogni istanza Option in PrintTicket a un'opzione elencata nella funzionalità corrispondente nel documento PrintCapabilities, in base ai risultati del processo di assegnazione dei punteggi. L'assegnazione dei punteggi è il processo di ricerca dell'opzione nel documento PrintCapabilities che meglio corrisponde all'opzione denominata in PrintTicket. Per una descrizione di ciò che viene preso in considerazione durante il processo di assegnazione dei punteggi, vedere [Definizioni delle opzioni](option-definitions.md). Sostituire ogni opzione di riferimento in PrintTicket con l'opzione del documento PrintCapabilities candidato corrispondente. È anche possibile classificare tutti i candidati in base al punteggio e passare queste informazioni alla fase di risoluzione nel caso in cui un conflitto di vincoli impedisca l'uso del candidato corrispondente migliore. In questi casi, il processo di risoluzione può usare il secondo candidato migliore anziché scegliere un altro candidato in modo casuale.

10. Per una funzionalità la cui proprietà SelectionType è impostata su PickMany e con più opzioni selezionate in PrintTicket, verificare che nessuna opzione sia designata come IdentityOption. Se esiste un'opzione di questo tipo, eliminare ogni altra opzione, lasciando solo quella designata IdentityOption. Questo passaggio deve essere eseguito prima e dopo l'applicazione del processo di assegnazione dei punteggi.

    Il motivo per cui questo passaggio deve essere eseguito due volte è che il processo di assegnazione dei punteggi può eseguire il mapping di più istanze option di riferimento alla stessa opzione candidata. In questo caso, eliminare eventuali istanze di Opzione duplicate in modo che le opzioni elencate per una particolare funzionalità PickMany siano univoche.

11. Aggiungere a PrintTicket qualsiasi funzionalità presente nel documento PrintCapabilities che non viene visualizzata in PrintTicket. Per una funzionalità di questo tipo, designare l'opzione predefinita come opzione selezionata.

12. Determinare se sono presenti istanze ParameterDef che soddisfano tutti i criteri seguenti:

    -   L'istanza ParameterDef viene visualizzata nel documento PrintCapabilities, ma non in PrintTicket.

    -   La proprietà Mandatory dell'istanza ParameterDef è impostata su Unconditional o Conditional.

    -   L'istanza ParameterDef fa riferimento a un'istanza ParameterRef in PrintTicket all'interno di un'istanza option.

    Per ogni istanza ParameterDef di questo tipo nel documento PrintCapabilities, aggiungere a PrintTicket un'istanza ParameterInit corrispondente. Impostare il valore delle istanze ParameterInit appena aggiunte sul valore predefinito specificato dalle istanze ParameterDef corrispondenti.

13. Eseguire il rilevamento dei conflitti dei vincoli e modificare la configurazione per eliminare tali conflitti. In questo argomento non viene definito un processo specifico da utilizzare per risolvere i conflitti di vincolo. È necessario decidere quale istanza di Feature o ParameterInit può essere modificata e un'opzione o un valore appropriato, rispettivamente, per selezionare che abbia il minor impatto sulla finalità complessiva della configurazione specificata in PrintTicket. Come accennato in precedenza, è possibile usare il punteggio di mapping di ogni opzione e usare l'opzione con il secondo punteggio più alto. Per determinare la funzionalità o ParameterInit da modificare, è possibile definire una proprietà privata che il client può aggiungere a PrintTicket. Questa proprietà può definire una priorità per le istanze Feature e ParameterInit in modo che il processo di risoluzione sia informato delle istanze Feature o ParameterInit importanti per il client (e devono essere mantenute in PrintTicket) e quali sono meno importanti.

14. Se il processo di risoluzione dei vincoli ha causato modifiche in PrintTicket a tutte le istanze ParameterRef per cui la proprietà obbligatoria è impostata su Condizionale, aggiungere istanze ParameterInit con valori predefiniti per quelle che ora vengono visualizzate e rimuovere qualsiasi istanza ParameterInit per un'istanza ParameterRef che non viene più visualizzata.

15. Rimuovere tutte le istanze property e il relativo contenuto che vengono visualizzati all'interno di istanze Option in PrintTicket. Gli elementi proprietà non hanno alcun ruolo in PrintTicket. Se l'opzione convalidata per una determinata funzionalità corrisponde perfettamente all'opzione prevalidata, trasferire tutte le istanze property in tale opzione da PrintTicket preconvalida a PrintTicket ora convalidato, a condizione che gli spazi dei nomi delle istanze property siano registrati nel documento PrintCapabilities. Si noti che per due istanze option da considerare una corrispondenza perfetta, per ogni ScoredProperty trovato in un'opzione, deve essere presente una proprietà ScoredProperty corrispondente nell'altra opzione e i valori di entrambe le istanze ScoredProperty devono essere gli stessi.

16. Se il provider PrintTicket riconosce e supporta le istanze di proprietà private o pubbliche che sono state ancora eseguite fino a questo punto, eseguirne la convalida. Non eliminare una proprietà a questo punto solo perché non la si riconosce, potrebbe essere destinata a un'altra fase dell'elaborazione dei documenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



