---
description: Questo argomento descrive le considerazioni di stemming per i linguaggi agglutinativi e le coppie di surrogati Unicode e per l'uso di coppie di surrogati per estendere il set di caratteri Unicode per supportare set di caratteri diversi.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Considerazioni varie su linguistico e Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24372194fb17498e1e0ce19be1bbbac3f1dccb27a63d840cedf95de38f735026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594481"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Considerazioni varie su linguistico e Unicode

Questo argomento descrive le considerazioni di stemming per i linguaggi agglutinativi e le coppie di surrogati Unicode e per l'uso di coppie di surrogati per estendere il set di caratteri Unicode per supportare set di caratteri diversi. Questo argomento descrive anche come i word breaker identificano le frasi nel testo e gestiscono gli spazi unificatori e come i word breaker e gli stemmer gestiscono numeri e date, parole composte, frasi composte, parole e caratteri speciali, acronimi e abbreviazioni e lettere maiuscole.

Questo argomento è organizzato come segue:

-   [Identificazione di frasi](#phrase-identification)
-   [Lingue agglutinative](#agglutinative-languages)
-   [Numeri, ore e date](#numbers-times-and-dates)
-   [Parole composte](#compound-words)
-   [Frasi composte](#compound-phrases)
-   [Caratteri speciali e parole](#special-characters-and-words)
-   [Acronimi e abbreviazioni](#acronyms-and-abbreviations)
-   [Uso delle maiuscole](#capitalization)
-   [Spazi unificatori](#nonbreaking-spaces)
-   [Coppie di surrogati](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificazione di frasi

Le frasi sono una parola o un gruppo di parole modificate da una o più altre parole. Le frasi sono difficili da identificare in modo coerente perché lo stesso modificatore può essere usato in più frasi con lo stesso sostantivo. Ad esempio, "nuova casa", "Camera del parlamentino", "nuova camera del parlamentino".

Windows La ricerca usa le frasi più spesso in fase di query. Le frasi nel testo della query ricevono un peso maggiore rispetto alle singole parole. Nell'esempio precedente, un documento contenente "House of Parliament" è classificato più in alto di uno contenente "House" e "Parlamenti" in punti diversi del documento. È consigliabile che i word breaker generino una frase in fase di query se è probabile che corrisponda ad almeno un documento.

## <a name="agglutinative-languages"></a>Lingue agglutinative

I linguaggi agglutinativi formano le parole tramite la combinazione di morfimi più piccoli per esprimere idee composte. Ognuno di questi morphemi ha in genere un significato o una funzione e mantiene la forma e il significato originali durante il processo di combinazione. Per le lingue con morfologia agglutinativa, ad esempio turco, finlandese, ungherese o coreano, è possibile produrre migliaia di forme per una determinata parola radice.

La tabella seguente mostra un elenco di moduli gonfiati per la parola finlandese "talo" ("house").



| Word      | Traduzione   |
|-----------|---------------|
| Talo      | Casa         |
| Taloni    | La mia casa      |
| Talossa   | In casa  |
| Talossani | In casa mia   |
| Taloja    | Case        |
| Taloissa  | Nelle case |



 

Le lingue gonfiate, ad esempio inglese, francese e latino, hanno un numero molto ridotto di possibili forme di parola per una parola radice. Nei linguaggi gonfiati, i morfimi si influenzano l'un l'altro durante l'associazione. La maggior parte delle modifiche nell'inflezione è presente nel gambo o nella fine della parola. A differenza dei linguaggi agglutinativi, i linguaggi gonfiati tendono ad avere funzioni diverse per un singolo morpheme. Ad esempio, un morpheme può determinare sia il numero che la distinzione tra maiuscole e minuscole.

Gli stemmer per le lingue agglutinative devono valutare il compromesso tra prestazioni e accuratezza per generare solo un subset del numero di possibili forme di parola.

## <a name="numbers-times-and-dates"></a>Numeri, ore e date

I word breaker devono usare un formato comune per rappresentare numeri, ore e date per facilitare l'esecuzione di query coerenti.

Quando si crea un word breaker, è consigliabile che il word breaker normalizzi i numeri in una rappresentazione canonica usando il modello "NN *dd* D *cc",* dove NN è la sequenza letterale "NN", *dd* è la parte intera del numero, D è il valore letterale "D" e *cc* è la parte frazionaria del numero. I word breaker non limitano il numero di cifre per l'intero o la parte frazionaria del numero. È consigliabile che i word breaker riconoscano modelli numerici delimitati da punti (.) e virgole (,). Ad esempio, Windows ricerca rappresenta sia "1.000.2" che "1.000,2" come "NN1000D2".

Scegliere un formato sia per word breaker che per stemmer. I numeri arabi a byte singolo vengono normalizzati in modo che una query contenente uno di questi moduli corrisponda ai documenti con gli altri formati.

Quando si crea un word breaker, è consigliabile che il word breaker sia presente tutte le volte come rappresentazione di 24 ore usando il modello "TT *hhmmss",* dove TT è il prefisso letterale *"TT", hh* è il numero di ore, *mm* è il minuto e *ss* è il secondo. Windows La ricerca non corrisponde ad altre unità di tempo, ad esempio millisecondi. Analisi di A.M. sia quello i modelli sono facoltativi.

Quando si crea un word breaker, è consigliabile che il word breaker generi date nel formato canonico "GG *aaaaammgg",* dove GG è il valore letterale "DD", *a* è gli anni, *mm* è il mese e *gg* è il giorno. È anche consigliabile che i word breaker archivino gli anni a due cifre nei formati ventesimo e ventunesimo secolo. Ad esempio, i word breaker rappresentano "2.2.99" come "DD19990202" e "DD20990202". In fase di query, Windows Search deriva la data usando le API (Application Programming Interface) di Windows per determinare la data crossover per il server per visualizzare il formato corretto, 19 *XX* o 20 *XX.*

## <a name="compound-words"></a>Parole composte

In alcune lingue, ad esempio il tedesco, i sostantivi sono composti da sostantivi più semplici. Questi sostantivi composti sono troppo specifici per un richiamo ragionevole delle query. Ad esempio, senza scomposizione, una query per "Versicherung" ("assicurazioni") non corrisponde a "Lebensversicherungsgesellschaft" ("venditore di assicurazioni sulla vita"). In casi come questo, è consigliabile suddividere queste parole composte in componenti di base durante la creazione dell'indice e durante la query. Il word breaker tedesco suddivide "Lebensversicherungsgesellschaft" nelle parole componenti "Leben", "Versicherung" e "Gesellschaft". Applica la stessa scomposizione in fase di query, insieme allo stemming facoltativo per ognuno dei termini risultanti.

## <a name="compound-phrases"></a>Frasi composte

Alcune lingue, ad esempio il coreano, contengono frasi complesse che possono essere interrotte in diversi modi. Una frase coreana è costituita da parole di *contenuto,* ad esempio sostantivi, pronomi, verbi e aggettivi, seguite da *parole funzionali.* Le parole funzionali si trovano nelle post-posizioni e nelle terminazioni. Le post-posizioni indicano il ruolo funzionale del sostantivo o del pronome in una frase; le terminazioni indicano il ruolo funzionale del verbo o dell'aggettivo.

Una frase può avere diverse analisi e ogni analisi può essere costituita da diverse parole di contenuto. Il word breaker deve usare euristica specifica del linguaggio per determinare, dal contesto, la quantità di peso da assegnare alle diverse analisi. Il word breaker può determinare quale scomposizione usare in base al numero di parole componente risultanti. Alcuni word breaker possono favorire brevi sequenze di termini più lunghi, mentre altri word breaker possono favorire sequenze lunghe di parole più piccole.

Un'altra considerazione è che in coreano, i sostantivi e i pronomi possono essere archiviati nell'indice senza le parole funzionali corrispondenti. Il coreano è un linguaggio agglutinativo e combina numerose terminazioni di parole con verbi e aggettivi per formare innumerevoli forme gonfiate. I verbi e gli aggettivi identificati nelle frasi vengono salvati con le relative terminazioni nell'indice, ma il word breaker non genera nuove forme.

## <a name="special-characters-and-words"></a>Caratteri speciali e parole

I caratteri speciali sono caratteri come "," "©" e "™". Questi caratteri vengono usati raramente nelle query. I word breaker devono rimuovere i caratteri speciali durante la creazione dell'indice e in fase di query.

È consigliabile che i word breaker riconoscano parole speciali, ad esempio "C++", \# "C", ".NET" e la notazione musicale. I word breaker possono usare un'euristica linguistica per identificare un modello per parole speciali. I word breaker possono anche usare un dizionario personalizzato che contiene parole speciali riconosciute.

## <a name="acronyms-and-abbreviations"></a>Acronimi e abbreviazioni

Quando si implementa un word breaker, è necessario considerare gli acronimi e le abbreviazioni. In molte lingue le singole lettere degli acronimi sono separate da punti. In alcuni casi, le parole che non sono acronimi o abbreviazioni non riconosciute vengono abbreviate. Ad esempio, "Stati Uniti america" può essere abbreviato come "USA" o "U.S.A." I word breaker inclusi in Windows ricerca identificano in genere le parole di una sola lettera come parole non erre e trattano tali parole come segnaposto durante la query. Durante il tempo di query, un word breaker che non è a conoscenza di acronimi comuni o che non riconosce le abbreviazioni, converte l'abbreviazione "U.S.A." in "U", "S" e "A". Questa scomposizione non fornisce informazioni sufficienti per trovare la corrispondenza con le parole nell'indice full-text perché tutti i termini di query sono parole non erre. Quando si crea un word breaker, è consigliabile rimuovere i punti che separano le lettere degli acronimi. Nell'esempio, "U.S.A." viene archiviato come "USA" e un termine di query che contiene "U.S.A." esegue effettivamente una query per "USA". Se un word breaker elabora un'abbreviazione, il punto in tale abbreviazione non viene considerato un'interruzione EOS. Per questo scopo, un word breaker potrebbe non identificare correttamente un'interruzione EOS se l'abbreviazione si trova alla fine della frase.

## <a name="capitalization"></a>Uso delle maiuscole

Windows La ricerca non mantiene attualmente l'uso di maiuscole e minuscole quando salva le parole nell'indice full-text. I word breaker e gli stemmer non devono modificare la distinzione tra maiuscole e minuscole per le parole.

## <a name="nonbreaking-spaces"></a>Spazi unificatori

Quando si crea un word breaker, è consigliabile assicurarsi che il word breaker tratti gli spazi unificatori come separatori di parole. È anche consigliabile che il word breaker generi forme alternative della parola, con e senza spazi unificatori. Alcuni caratteri, ad esempio caratteri di sottolineatura, sono caratteri speciali trattati come caratteri unificatori a causa delle origini del testo in cui vengono trovati. Ad esempio, il codice sorgente o i nomi di file possono includere caratteri di sottolineatura come caratteri unificatori.

## <a name="surrogate-pairs"></a>Coppie di surrogati

Le coppie di surrogati sono rappresentazioni di caratteri nel codice sorgente che rappresentano un singolo carattere costituito da una sequenza di due valori Unicode. In una coppia codificata, il primo valore è un surrogato alto e il secondo è un surrogato basso. Un surrogato alto è un carattere compreso nell'intervallo da U+D800 a U+DBFF. Un surrogato basso è un carattere compreso nell'intervallo da U+DC00 a U+DFFF. Le coppie di surrogati estendono il set di caratteri oltre il carattere Unicode. È consigliabile che un word breaker usi le regole seguenti per la gestione delle coppie di surrogati:

-   Un surrogato alto deve precedere un surrogato basso.
-   Un surrogato basso deve seguire un surrogato alto.
-   Un surrogato alto o basso senza un valore corrispondente per l'altra metà non ha alcun significato.

I word breaker devono prendere in considerazione qualsiasi coppia e generare le coppie come tali nell'indice. Per altre informazioni, vedere [Surrogati e caratteri supplementari.](/windows/desktop/Intl/surrogates-and-supplementary-characters)

 

 
