---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Elenco di controllo convalida PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a0e9f3eb71b1e9a3b670456e04e2efa3c8b15
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320954"
---
# <a name="printticket-validation-checklist"></a>Elenco di controllo convalida PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintTicket devono convalidare l'oggetto PrintTicket prima di utilizzarlo per qualsiasi scopo. Una volta convalidata, l'oggetto PrintTicket può essere restituito al client o può essere rimosso dopo l'utilizzo. In questo elenco di controllo vengono illustrate le attività che il provider deve eseguire durante la convalida. Il processo di convalida modificherà spesso il contenuto dell'oggetto PrintTicket, sebbene non alteri un oggetto PrintTicket precedentemente convalidato.

La convalida viene sempre eseguita su un dispositivo specifico che include un set di istanze di funzionalità, opzioni e ParameterDef definite in un documento PrintCapabilities. Il codice di convalida deve avere accesso al set di istanze della funzionalità (e alle istanze di opzioni contenute) e alle istanze di ParameterDef per il dispositivo specifico e non deve necessariamente accedere a PrintCapabilities. Le informazioni dalle istanze feature, Option e ParameterDef sono necessarie in determinate parti del processo di convalida.

1.  Durante i tentativi di individuare gli elementi corrispondenti o corrispondenti, si noti che gli spazi dei nomi degli elementi devono corrispondere prima che qualsiasi nome completo possa essere considerato una corrispondenza. Tutti i nomi degli elementi, i nomi degli attributi e i nomi delle istanze sono qualificati con lo spazio dei nomi. Per gli elementi annidati, le rispettive posizioni devono corrispondere prima che gli elementi vengano considerati corrispondenti.

2.  Verificare che tutti i tag degli elementi si trovino nello spazio dei nomi Public, che siano definiti dallo schema PrintTicket, che contengano gli attributi XML appropriati e i valori di attributo e che la posizione di ogni tipo di elemento sia conforme all'utilizzo definito dallo schema PrintTicket.

3.  Determinare tutti gli spazi dei nomi restituiti dal documento PrintCapabilities. Rimuovere tutti gli elementi (e i relativi discendenti) da PrintTicket i cui nomi di istanza appartengono agli spazi dei nomi non segnalati dal documento PrintCapabilities. Si noti la differenza tra questo caso e il caso seguente, che prevede nomi di istanza non riconosciuti all'interno di uno spazio dei nomi noto.

4.  Poiché gli schemi vengono continuamente estesi con l'aggiunta di nuove definizioni di istanza dell'elemento, il codice di convalida non deve essere scritto nel presupposto che ogni nome di istanza in uno spazio dei nomi specificato sia noto. Il codice di convalida non può considerare i nomi di istanza non riconosciuti all'interno di uno spazio dei nomi noto come errori, né eliminarli dall'oggetto PrintTicket.

5.  Se un'istanza dell'elemento ha un elemento di pari livello duplicato non consentito dallo schema PrintTicket, conserva solo la prima occorrenza ed Elimina i duplicati, incluso il contenuto dell'elemento duplicato.

6.  Rimuovere da PrintTicket qualsiasi funzionalità o sottofunzionalità (e tutti i relativi elementi figlio) che non dispone di funzionalità corrispondenti nel documento PrintCapabilities.

7.  Controllare la proprietà SelectionType definita nel documento PrintCapabilities per ognuna delle istanze della funzionalità rimanenti nel PrintTicket. Tutte le funzionalità la cui proprietà SelectionType è impostata su PickOne devono avere una sola istanza di opzioni presente nell'oggetto PrintTicket, mentre una funzionalità la cui proprietà SelectionType è PickMany può avere più di una. Se una funzionalità PrintTicket non dispone di un'istanza di opzione, fornire l'istanza dell'opzione predefinita. Poiché si è il provider, si sa quale opzione è l'opzione predefinita per ogni funzionalità.

    Per una funzionalità la cui proprietà SelectionType è PickMany, con più di un'opzione selezionata in PrintTicket, verificare che nessuna opzione sia designata come IdentityOption. Se è presente, eliminare tutte le altre opzioni lasciando solo quello designato come IdentityOption.

8.  Rimuovere qualsiasi istanza di ParameterInit nell'oggetto PrintTicket che non dispone di un'istanza ParameterDef corrispondente nel documento PrintCapabilities.

    Per tutte le altre istanze di ParameterInit nell'oggetto PrintTicket, verificare che il valore per ogni istanza sia conforme all'istanza ParameterDef del documento PrintCapabilities. Se non è presente un valore, specificare il valore predefinito fornito in ParameterDef.

9.  Associare ogni istanza di opzione nel PrintTicket con un'opzione elencata nella funzionalità corrispondente del documento PrintCapabilities, in base ai risultati del processo di assegnazione dei punteggi. Il Punteggio è il processo di ricerca dell'opzione nel documento PrintCapabilities che corrisponde maggiormente all'opzione denominata nell'oggetto PrintTicket. Per una descrizione degli elementi presi in considerazione durante il processo di assegnazione dei punteggi, vedere [definizioni delle opzioni](option-definitions.md). Sostituire ogni opzione di riferimento nell'oggetto PrintTicket con l'opzione corrispondente al documento PrintCapabilities corrispondente. È anche possibile classificare tutti i candidati per punteggio e passare queste informazioni alla fase di risoluzione nel caso in cui un conflitto di vincoli impedisca l'uso del candidato corrispondente. In questi casi, il processo di risoluzione può utilizzare il secondo candidato migliore anziché scegliere un altro candidato in modo casuale.

10. Per una funzionalità la cui proprietà SelectionType è impostata su PickMany e con più di un'opzione selezionata nel PrintTicket, verificare che nessuna opzione sia designata come IdentityOption. Se esiste un'opzione di questo tipo, eliminare tutte le altre opzioni lasciando solo quella designata IdentityOption. Questo passaggio deve essere eseguito prima e dopo l'applicazione del processo di assegnazione dei punteggi.

    Il motivo per cui questo passaggio deve essere eseguito due volte è che il processo di assegnazione dei punteggi può eseguire il mapping di più istanze di opzioni di riferimento alla stessa opzione candidata. In tal caso, eliminare eventuali istanze di opzioni duplicate in modo che le opzioni elencate per una particolare funzionalità PickMany siano univoche.

11. Aggiungere all'oggetto PrintTicket le funzionalità presenti nel documento PrintCapabilities che non vengono visualizzate nell'oggetto PrintTicket. Per questa funzionalità, impostare l'opzione predefinita come opzione selezionata.

12. Determinare se sono presenti istanze di ParameterDef che soddisfano tutti i criteri seguenti:

    -   L'istanza ParameterDef viene visualizzata nel documento PrintCapabilities, ma non nel PrintTicket.

    -   La proprietà obbligatoria dell'istanza ParameterDef è impostata su non condizionale o condizionale.

    -   Un'istanza di ParameterDef fa riferimento all'istanza di ParameterRef in un oggetto PrintTicket all'interno di un'istanza di Option.

    Per ogni istanza di ParameterDef nel documento PrintCapabilities, aggiungere all'oggetto PrintTicket un'istanza di ParameterInit corrispondente. Impostare il valore delle istanze di ParameterInit appena aggiunte sul valore predefinito specificato dalle istanze ParameterDef corrispondenti.

13. Eseguire il rilevamento dei conflitti di vincolo e modificare la configurazione per eliminare questi conflitti. Questo argomento non definisce un processo specifico da usare per risolvere i conflitti di vincolo. È necessario decidere la funzionalità o l'istanza di ParameterInit che è possibile modificare e un'opzione o un valore appropriato, rispettivamente, per selezionare che ha un effetto minimo sulla finalità complessiva della configurazione specificata nel PrintTicket. Come indicato in precedenza, si potrebbe voler usare il Punteggio di mapping di ogni opzione e usare l'opzione con il secondo punteggio più alto. Per determinare la funzionalità o il ParameterInit da modificare, è possibile definire una proprietà privata che il client può aggiungere al PrintTicket. Questa proprietà può definire una priorità per le istanze feature e ParameterInit, in modo che il processo del resolver venga informato delle istanze feature o ParameterInit importanti per il client (e deve essere mantenuto nell'oggetto PrintTicket) e quali sono meno importanti.

14. Se il processo di risoluzione dei vincoli ha causato modifiche in PrintTicket a qualsiasi istanza di ParameterRef per la quale la proprietà obbligatoria è impostata su Conditional, aggiungere istanze di ParameterInit con i valori predefiniti per quelle che ora appaiono e rimuovere qualsiasi istanza di ParameterInit per un'istanza di ParameterRef che non viene più visualizzata.

15. Rimuovere tutte le istanze di proprietà e il relativo contenuto presenti all'interno delle istanze di opzioni nell'oggetto PrintTicket. Gli elementi Property non hanno alcun ruolo nell'oggetto PrintTicket. Se l'opzione convalidata per una particolare funzionalità corrisponde perfettamente all'opzione prevalidata, trasferire tutte le istanze di proprietà in tale opzione dall'oggetto PrintTicket di preconvalida al PrintTicket ora convalidato, in base alla condizione in cui gli spazi dei nomi delle istanze di proprietà vengono registrati nel documento PrintCapabilities. Si noti che per due istanze di opzioni da considerare come una corrispondenza perfetta, per ogni ScoredProperty trovato in un'opzione, deve essere presente un ScoredProperty corrispondente nell'altra opzione e i valori di entrambe le istanze di ScoredProperty devono essere uguali.

16. Se il provider PrintTicket riconosce e supporta le istanze di proprietà private o pubbliche che sono sopravvissute a questo punto, eseguire la convalida su di essi. Non eliminare una proprietà in questa fase solo perché non è riconosciuta, potrebbe essere destinata a un'altra fase dell'elaborazione dei documenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



