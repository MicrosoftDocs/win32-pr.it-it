---
description: In questo argomento vengono descritte le considerazioni relative allo stemming per i linguaggi agglutinante e le coppie di surrogati Unicode e per l'utilizzo delle coppie di surrogati per estendere il set di caratteri Unicode per supportare set di caratteri diversi
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Considerazioni linguistiche e Unicode varie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433fb212917f29acbc2347c3324668a77533dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049378"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Considerazioni linguistiche e Unicode varie

In questo argomento vengono descritte le considerazioni relative allo stemming per i linguaggi agglutinante e le coppie di surrogati Unicode e per l'utilizzo delle coppie di surrogati per estendere il set di caratteri Unicode per supportare set di caratteri diversi In questo argomento viene inoltre descritto il modo in cui i Word breaker identificano le frasi nel testo e gestiscono gli spazi unificatori e il modo in cui Word breaker e stemmer gestiscono numeri e date, parole composte, frasi composte, parole e caratteri speciali, acronimi e abbreviazioni e maiuscole.

Questo argomento è organizzato nel modo seguente:

-   [Identificazione di frasi](#phrase-identification)
-   [Lingue agglutinante](#agglutinative-languages)
-   [Numeri, orari e date](#numbers-times-and-dates)
-   [Parole composte](#compound-words)
-   [Frasi composte](#compound-phrases)
-   [Caratteri speciali e parole](#special-characters-and-words)
-   [Acronimi e abbreviazioni](#acronyms-and-abbreviations)
-   [Uso delle maiuscole](#capitalization)
-   [Spazi unificatori](#nonbreaking-spaces)
-   [Coppie di surrogati](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificazione di frasi

Le frasi sono una parola o un gruppo di parole modificate da uno o più utenti. Le frasi sono difficili da identificare in modo coerente perché lo stesso modificatore può essere usato in più di una frase con lo stesso nome. Ad esempio, "nuova casa", "casa del Parlamento", "nuova casa del Parlamento".

Windows Search usa le frasi più spesso in fase di query. Le frasi nel testo della query ricevono un peso maggiore rispetto alle singole parole. Dall'esempio precedente, un documento che contiene "House of Parliament" è classificato a un livello superiore rispetto a quello che contiene "House" e "Parliament" in punti diversi del documento. È consigliabile che i Word breaker generino una frase in fase di query se è probabile che la frase corrisponda almeno a un documento.

## <a name="agglutinative-languages"></a>Lingue agglutinante

Le lingue agglutinante formano parole attraverso la combinazione di nei morfemi più piccoli per esprimere idee composte. Ognuno di questi nei morfemi ha in genere un significato o una funzione e mantiene il formato originale e il significato durante il processo combinato. Per i linguaggi con morfologia agglutinante, ad esempio turco, finlandese, ungherese o coreano, è possibile produrre migliaia di moduli per una parola radice specificata.

Nella tabella seguente viene illustrato un elenco di forme flesse per la parola finlandese "Talo" ("casa").



| Word      | Traduzione   |
|-----------|---------------|
| Talo      | Internamente         |
| Taloni    | La mia casa      |
| Talossa   | In casa  |
| Talossani | In casa   |
| Taloja    | Ospita        |
| Taloissa  | Nelle case |



 

Le lingue flesse, ad esempio l'inglese, il francese e il latino, hanno un numero molto ridotto di possibili forme di Word per una parola radice. Nelle lingue flesse, nei morfemi influisce l'uno sull'altro durante l'associazione. La maggior parte delle modifiche apportate è presente nell'estremità o terminazione di parole. Diversamente dalle lingue agglutinante, le lingue flesse tendono a avere funzioni diverse per un singolo morfema. Ad esempio, un morfema può determinare sia il numero che il caso.

Gli stemmer per le lingue agglutinante devono valutare il compromesso tra prestazioni e accuratezza per generare solo un subset del numero di formati di Word possibili.

## <a name="numbers-times-and-dates"></a>Numeri, orari e date

I Word breaker devono utilizzare un formato comune per la rappresentazione di numeri, orari e date per semplificare l'esecuzione di query coerenti.

Quando si crea un Word breaker, si consiglia di normalizzare i numeri in una rappresentazione canonica usando il modello "NN *DD* D *CC*", dove nn è la sequenza letterale "nn", *DD* è la parte intera del numero, D è il valore letterale "D" e *CC* è la parte frazionaria del numero. I Word breaker non limitano il numero di cifre per il numero intero o la parte frazionaria del numero. È consigliabile che i Word breaker riconoscano modelli numerici delimitati da entrambi i punti (.) e virgole (,). Windows Search, ad esempio, rappresenta sia "1.000,2" che "1.000, 2" come "NN1000D2".

Scegliere un formato sia per Word breaker che per stemmer. I numerali arabi a un byte vengono normalizzati in modo che una query contenente uno di questi moduli corrisponda ai documenti con gli altri form.

Quando si crea un Word breaker, è consigliabile che il Word breaker sia presente in tutte le ore come rappresentazione a 24 ore usando il modello "TT *HHMMSS*", dove TT è il prefisso letterale "TT", *HH* è l'ora, *mm* è il minuti e *SS* è il secondo. Windows Search non corrisponde a unità di tempo aggiuntive, ad esempio millisecondi. Analisi delle AM sia quello patterns è facoltativo.

Quando si crea un Word breaker, è consigliabile che il Word breaker generi date nel formato canonico "DD *AAAAMMGG*", dove gg è il valore letterale "gg", *aaaa* è l'anno, *mm* è il mese e *GG* è il giorno. È inoltre consigliabile che i Word breaker memorizzino gli anni a due cifre nei formati ventesimo e ventunesimo secolo. I Word breaker rappresentano, ad esempio, "2.2.99" come "DD19990202" e "DD20990202". In fase di query, Windows Search deriva la data usando le API (Application Programming Interface) di Windows per determinare la data di crossover per il server per visualizzare il formato corretto, 19 *XX* o 20 *XX*.

## <a name="compound-words"></a>Parole composte

In alcune lingue, ad esempio il tedesco, i sostantivi sono composti da sostantivi più semplici. Questi sostantivi composti sono troppo specifici per il richiamo di una query ragionevole. Ad esempio, senza scomposizione, una query per "Versicherung" ("assicurativa") non corrisponde a "Lebensversicherungsgesellschaft" ("Sales-insurance sales"). In casi come questo, è consigliabile che i Word breaker interrompano queste parole composte in componenti di base durante la creazione dell'indice e il tempo di esecuzione delle query. Il Word breaker tedesco interrompe "Lebensversicherungsgesellschaft" nelle parole del componente "Leben", "Versicherung" e "Gesellschaft". Viene applicata la stessa scomposizione in fase di query, insieme a stemming facoltativo per ognuno dei termini risultanti.

## <a name="compound-phrases"></a>Frasi composte

Alcuni linguaggi, ad esempio il coreano, contengono frasi complesse che possono essere suddivise in diversi modi. Una frase in coreano è costituita da *parole di contenuto*, ad esempio sostantivi, pronomi, verbi ed aggettivi, seguiti da *parole funzionali*. Le parole funzionali si trovano in postposizioni e terminazioni. Le postposizioni indicano il ruolo funzionale del sostantivo o del pronome in una frase; le terminazioni indicano il ruolo funzionale del verbo o dell'aggettivo.

Una frase può avere diverse analisi e ogni analisi può essere costituita da più parole di contenuto. Il Word breaker deve usare euristiche specifiche della lingua per determinare, dal contesto, quanto peso assegnare a diverse analisi. Il Word breaker può determinare la scomposizione da utilizzare in base al numero di parole dei componenti risultanti. Alcuni Word breaker possono favorire brevi sequenze di termini più lunghi, mentre altri Word breaker possono favorire sequenze lunghe di parole più piccole.

Un'altra considerazione è che in coreano, i sostantivi e i sostantivi possono essere archiviati nell'indice senza le parole funzionali corrispondenti. Il coreano è un linguaggio agglutinante e combina numerose terminazioni di parola con verbi ed aggettivi per formare innumerevoli forme flesse. I verbi e gli aggettivi identificati nelle frasi vengono salvati con le relative terminazioni nell'indice, ma il Word breaker non genera nuovi moduli.

## <a name="special-characters-and-words"></a>Caratteri speciali e parole

I caratteri speciali sono caratteri quali "," "©" e "™". Questi caratteri vengono usati raramente nelle query. I Word breaker devono rimuovere i caratteri speciali durante la creazione dell'indice e in fase di query.

È consigliabile che i Word breaker riconoscano parole speciali, ad esempio "C++", "C", ".NET", \# voti e notazione musicale. I Word breaker possono utilizzare un'euristica del linguaggio per identificare un modello per parole speciali. I Word breaker possono inoltre utilizzare un dizionario personalizzato che contiene parole speciali riconosciute.

## <a name="acronyms-and-abbreviations"></a>Acronimi e abbreviazioni

Quando si implementa un Word breaker, è necessario considerare gli acronimi e le abbreviazioni. In molti linguaggi le singole lettere degli acronimi sono separate da punti. Occasionalmente, le parole che non sono acronimi o abbreviazioni riconosciute sono abbreviate. Ad esempio, "Stati Uniti of America" può essere abbreviato come "USA" o "U.S.A.". I Word breaker inclusi nella ricerca di Windows in genere identificano le parole a lettera singola come parole non significative e considerano tali parole come segnaposto durante la fase di query. Durante la fase di query, un Word breaker che non è in grado di riconoscere gli acronimi comuni o che non riconosce le abbreviazioni, converte l'abbreviazione "U.S.A." in "U", "S" e "A". Questa scomposizione non fornisce informazioni sufficienti per trovare la corrispondenza con le parole nell'indice full-text perché tutti i termini di query sono parole non significative. Quando si crea un Word breaker, è consigliabile che il Word breaker rimuova i punti che separano le lettere degli acronimi. Nell'esempio "U.S.A." viene archiviato come "USA" e un termine di query che contiene "U.S.A." effettivamente esegue una query per "USA". Se un Word breaker elabora un'abbreviazione, il periodo di tale abbreviazione non viene considerato come un'esplosione EOS. Per questo motivo, un Word breaker potrebbe non identificare correttamente un'esplosione EOS se l'abbreviazione si trova alla fine della frase.

## <a name="capitalization"></a>Uso delle maiuscole

Windows Search non mantiene attualmente le maiuscole quando salva le parole nell'indice full-text. I Word breaker e gli stemmer non devono modificare il case per le parole.

## <a name="nonbreaking-spaces"></a>Spazi unificatori

Quando si crea un Word breaker, è consigliabile assicurarsi che il Word breaker consideri gli spazi unificatori come separatori di parole. È inoltre consigliabile che il Word breaker generi forme alternative della parola, con e senza spazi unificatori. Alcuni caratteri, come i caratteri di sottolineatura, sono caratteri speciali che vengono trattati come caratteri non Breaker a causa delle origini del testo in cui vengono trovati. Ad esempio, il codice sorgente o i nomi di file possono includere caratteri di sottolineatura come caratteri non di interruzioni.

## <a name="surrogate-pairs"></a>Coppie di surrogati

Le coppie di surrogati sono rappresentazioni di caratteri nel codice sorgente che rappresentano un singolo carattere costituito da una sequenza di due valori Unicode. In una coppia codificata, il primo valore è un surrogato alto e il secondo è un surrogato basso. Un surrogato alto è un carattere compreso nell'intervallo tra U + D800 e U + DBFF. Un surrogato basso è un carattere compreso nell'intervallo tra U + DC00 e U + DFFF. Le coppie di surrogati estendono il set di caratteri oltre il carattere Unicode. Per la gestione delle coppie di surrogati, è consigliabile che un Word breaker usi le regole seguenti:

-   Un surrogato alto deve precedere un surrogato basso.
-   Un surrogato basso deve seguire un surrogato alto.
-   Un surrogato alto o basso senza un valore corrispondente per l'altra metà non ha alcun significato.

I Word breaker devono prendere in considerazione qualsiasi coppia e generare le coppie come tali nell'indice. Per ulteriori informazioni, vedere [surrogati e caratteri supplementari](/windows/desktop/Intl/surrogates-and-supplementary-characters).

 

 
