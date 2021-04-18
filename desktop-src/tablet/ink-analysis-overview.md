---
description: Le API di InkAnalysis forniscono agli sviluppatori di Tablet PC strumenti avanzati per esaminare a livello di codice l'input penna. L'API classifica l'input penna in categorie significative quali parole, linee, paragrafi e disegni.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Panoramica dell'analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e383d16c01cd9475d4c54587b4b5fb4c09791a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525309"
---
# <a name="ink-analysis-overview"></a>Panoramica dell'analisi dell'input penna

Le API di InkAnalysis forniscono agli sviluppatori di Tablet PC strumenti avanzati per esaminare a livello di codice l'input penna. L'API classifica l'input penna in categorie significative quali parole, linee, paragrafi e disegni.

È possibile utilizzare ogni classificazione in diversi modi, tra cui migliorare i risultati del riconoscimento per la grafia.

## <a name="ink-analysis-basics"></a>Nozioni fondamentali sull'analisi dell'input penna

In questa sezione viene presentata la tecnologia di analisi dell'input penna della piattaforma Tablet PC e viene illustrato quando e come utilizzarlo.

Le API InkAnalysis combinano efficacemente due tecnologie distinte ma gratuite: il riconoscimento della grafia e la classificazione del layout. La combinazione di queste due tecnologie offre risultati più estesi rispetto alle parti prese da soli.

Il riconoscimento della grafia è l'analisi computazionale dell'input penna digitale manoscritto per restituire l'interpretazione basata sui caratteri in una determinata lingua. Ovvero il riconoscimento della grafia è il modo in cui il computer "legge" la grafia di una persona.

L'analisi dell'input penna può essere suddivisa ulteriormente nella classificazione dell'input penna e nell'analisi del layout. La classificazione Ink è la suddivisione computazionale dell'input penna in unità semanticamente significative, ad esempio paragrafi, righe, parole e disegni. L'analisi del layout è l'esame computazionale dell'input penna per determinare la posizione dell'input penna sulla superficie di Inking e il modo in cui i tratti sono correlati tra loro a livello spaziale e anche semanticamente. Ad esempio, l'analisi del layout può indicare che un particolare componente di input penna è un'annotazione o una chiamata.

### <a name="recognition"></a>Riconoscimento

Un esempio di come la combinazione di riconoscimento con l'analisi dell'input penna nell'API InkAnalysis consente allo sviluppatore di migliorare i risultati dei riconoscimenti. I motori di riconoscimento della grafia di Tablet PC sono stati progettati principalmente per riconoscere un'unica linea orizzontale di input penna. Tuttavia, le persone tendono a scrivere più righe quando si accettano note e tali righe non sono necessariamente orizzontali rispetto alla pagina. Con l'API InkAnalysis, l'input penna viene pre-elaborato da Ink Analyzer prima di essere inviato al riconoscimento. L'input penna analizzato viene trasformato in orizzontale prima di essere riconosciuto, migliorando i risultati del riconoscimento.

Altri vantaggi del riconoscimento derivano dal fatto che l'analizzatore di input penna corregge le informazioni errate dell'ordine di ictus prima di inviare l'input penna al riconoscimento. I risultati del riconoscimento sono ora disponibili in modo selettivo. In altre parole, lo sviluppatore può recuperare rapidamente i risultati del riconoscimento per una singola parola, riga o paragrafo in un'unica chiamata.

### <a name="ink-classification"></a>Classificazione input penna

Esistono, naturalmente, diversi scenari in cui è possibile mantenere intatti i dati dell'input penna, anziché convertirli immediatamente in testo. Anche l'analisi dell'input penna offre vantaggi. In particolare, le API InkAnalysis offrono la possibilità di suddividere i tratti di input penna a seconda che si tratti di scritture o disegni. I tratti di input penna classificati come scritti sono quelli che costituiscono una parola o caratteri. Tutti gli altri tratti sono disegni. Si tratta di un nuovo modo per accedere ai dati Ink, abilitando nuovi scenari utente. Ad esempio, è possibile implementare la selezione in modo che sia diversa in base al tipo di tratto su cui l'utente tocca; Se un utente tocca un tratto di scrittura, l'applicazione seleziona l'intero set di tratti che compongono la parola, se l'utente tocca un disegno Stoke, l'applicazione seleziona solo tale tratto.

### <a name="layout-analysis"></a>Analisi del layout

Un'analisi del layout utile è in realtà ben oltre la suddivisione relativamente semplice dell'input penna nella scrittura e nel disegno di componenti.

L'analisi dell'input penna include anche una suddivisione più dettagliata dei tratti di scrittura e di disegno. Come esempio molto semplice, prendere un BLOB di input penna, come illustrato nella figura seguente.

![due semplici righe di grafia](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Dopo che la piattaforma ha analizzato questi tratti, restituisce una rappresentazione ad albero di questi tratti, come illustrato nella figura seguente. Per questo semplice caso, l'albero contiene solo le informazioni relative a paragrafo, riga e parola, ma la ricchezza di questo albero aumenta man mano che aumenta la complessità del documento Ink.

![rappresentazione ad albero di radice, paragrafo, righe e parole](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Poiché queste informazioni sono ora separate da unità gestibili, è ora possibile creare funzionalità più potenti. Ad esempio, l'applicazione può estendere la funzionalità in cui l'utente tocca per selezionare una parola in una funzionalità in cui l'utente tocca una sola volta per selezionare la parola, tocca due volte per selezionare l'intera riga e tocca tre volte per selezionare l'intero paragrafo. Sfruttando la struttura ad albero restituita dall'operazione di analisi, l'applicazione può correlare l'area toccata a un tratto nell'albero. Dopo che l'applicazione ha individuato un tratto, può esaminare l'albero per determinare come e quali tratti adiacenti selezionare.

La selezione di un'intera riga è un esempio semplicistico dei vantaggi dell'analisi dell'input penna, ma le possibilità diventano ottimali quando si considerano i diversi tipi di strutture gerarchiche che possono essere rilevati dall'analizzatore di input penna:

-   Elenchi ordinati e non ordinati
-   Forme
-   Commenti annotativi scritti inline con il testo

I tipi di funzionalità variano da applicazione ad applicazione e si basano sui requisiti e sui motori di analisi e di riconoscimento disponibili.

### <a name="key-ink-analysis-features"></a>Funzionalità di analisi dell'input penna chiave

Le funzionalità principali dell'API InkAnalysis includono le funzionalità seguenti:

-   Analisi incrementale
-   Persistenza
-   Proxy di dati
-   Riconciliazione
-   Estendibilità

### <a name="incremental-analysis"></a>Analisi incrementale

Quando gli utenti finali lavorano con l'input penna, in genere lo considerano come grafia. L'input penna è costantemente soggetto a operazioni di modifica, ad esempio l'aggiunta di nuovi input penna, l'eliminazione di input penna e la modifica delle proprietà dell'input penna, tutte eseguite nello stesso modo in cui la grafia viene continuamente modificata. Queste operazioni di modifica influiscono sui risultati dell'analisi. Quando si verificano modifiche, in genere possono essere isolate in sezioni del documento in momenti specifici. Si supponga, ad esempio, che un utente scriva cinque righe di input penna. Il modo standard in cui le applicazioni analizzano l'input penna è attendere fino a quando l'utente non ha completato la scrittura di tutte le cinque righe di input penna, ad esempio un paragrafo, e quindi analizza i risultati in modo sincrono o asincrono.

È possibile ottimizzare il tempo complessivo impiegato per l'analisi di queste cinque righe isolando le aree analizzate durante la scrittura e quindi rianalizzando solo le parti dei risultati modificati. Dopo l'analisi, la prima riga non verrà mai riconosciuta a meno che non venga modificata dall'utente finale. Il riconoscimento della seconda riga viene considerato come un'operazione di riconoscimento indipendente.

Questo approccio incrementale funziona bene a livello di riga per le operazioni di riconoscimento, ma deve funzionare a un livello superiore per l'operazione di analisi dell'input penna. Poiché l'analizzatore di input penna è in grado di rilevare diverse classificazioni di livello superiore per queste cinque righe di input penna (ad esempio, potrebbe trattarsi di un paragrafo standard o di cinque elementi in un elenco), l'approccio incrementale per l'analizzatore di input penna è che deve analizzare queste strutture più elevate. Ciò significa che, dopo che l'analizzatore di input penna ha classificato la prima riga di input penna come riga, verifica che sia ancora una linea quando classifica la seconda riga. Tuttavia, l'analizzatore di input penna isola questo doppio controllo sul paragrafo e ignora il primo paragrafo quando si analizza un secondo paragrafo, considerando il secondo paragrafo come operazione di analizzatore di input penna indipendente. Questo approccio incrementale all'analisi consente di risparmiare notevolmente tempo di elaborazione quando nell'applicazione sono già presenti grandi quantità di input penna.

### <a name="persistence"></a>Persistenza

L'analisi incrementale funziona correttamente in una determinata sessione o istanza di un oggetto [**InkAnalyzer**](inkanalyzer.md) . Tuttavia, le API della piattaforma Tablet PC di prima generazione non possono eseguire l'analisi incrementale dopo che l'input penna è stato salvato su disco. L'API InkAnalysis consente di salvare l'input penna su disco insieme a una forma permanente dei risultati dell'analisi. I risultati dell'analisi possono essere caricati quando l'input penna viene caricato e possono essere inseriti in una nuova istanza di un **oggetto InkAnalyzer**. Una nuova istanza dell'oggetto **InkAnalyzer** ha quindi lo stesso stato dei risultati ottenuta in precedenza ed è ora in grado di accettare modifiche incrementali apportate allo stato esistente, anziché analizzare di nuovo tutti gli elementi.

### <a name="data-proxy"></a>Proxy di dati

Molte applicazioni dispongono già di una struttura di documenti esistente nelle proprie applicazioni. ad esempio, un grafo o un database. L' [**oggetto InkAnalyzer**](inkanalyzer.md) presenta anche i risultati in un formato strutturato, in una struttura ad albero di oggetti [**ContextNode**](icontextnode.md) . La struttura **InkAnalyzer** e la struttura esistente dell'applicazione devono interagire in due direzioni: i risultati vengono estratti dall' **oggetto InkAnalyzer** nell'applicazione e lo stato viene inserito dall'applicazione in **InkAnalyzer**.

Se il pull dei risultati dall' [**oggetto InkAnalyzer**](inkanalyzer.md) nella struttura dell'applicazione era sufficiente, sarebbe stato relativamente semplice. Le applicazioni eseguono l'iterazione nell'albero dei risultati e copiano (integrano) tutti i risultati necessari nella struttura dei dati esistente. Tuttavia, poiché molte applicazioni orizzontali richiedono l'analisi incrementale e la persistenza su disco, il problema diventa bidirezionale. Lo stato (risultati precedenti) deve essere estratto dalla struttura dell'applicazione e inserito nell' **oggetto InkAnalyzer**.

Per soddisfare questo requisito, l' [**oggetto InkAnalyzer**](inkanalyzer.md) contiene una serie di eventi che genera al momento appropriato durante un'operazione di analisi per consentire alle applicazioni di eseguire il proxy della richiesta di dati alle strutture esistenti. Questi eventi vengono generati solo per gli oggetti [**ContextNode**](icontextnode.md) richiesti dall'operazione incrementale.

### <a name="reconciliation"></a>Riconciliazione

Per la maggior parte delle applicazioni si desidera analizzare l'input penna in background per ridurre al minimo le interruzioni dell'interfaccia utente. L'analisi dell'input penna in background causa problemi, tuttavia, se l'utente modifica l'input penna (o l'input penna adiacente) analizzato. Se ad esempio l'utente elimina l'input penna durante l'operazione in background, la struttura risultante rifletterà lo stato del documento all'avvio dell'operazione in background, anziché quando è stata completata.

Per supportare le applicazioni, [**InkAnalyzer**](inkanalyzer.md) riconcilia le differenze nello stato del documento tra l'inizio e la fine dell'operazione di analisi. Le modifiche apportate dall'utente o dall'applicazione durante l'esecuzione dell'analisi in background eseguono sempre l'override dei risultati calcolati in background. Dopo la riconciliazione, vengono segnalati solo le parti della struttura dei risultati che non sono in conflitto con le modifiche del documento e i tratti in conflitto vengono contrassegnati per l'analisi futura. La volta successiva che viene eseguita l'operazione di analisi in background, i risultati vengono ricalcolati in base al nuovo stato.

Il diagramma seguente illustra questo processo. Il tempo è espresso in modo lineare dall'alto verso il basso nel diagramma.

![processo per la riconciliazione delle modifiche dello stato del documento durante l'operazione di analisi](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  All'ora 1 (T1), l'applicazione raccoglie l'input penna dall'utente finale, incluso qualsiasi tipo di modifica dell'input penna, ad esempio l'aggiunta, la rimozione o la modifica.
2.  In T2, l'applicazione richiama l'operazione di analisi in background. [**InkAnalyzer**](inkanalyzer.md) determina quale input penna non contiene risultati e quale input penna deve essere sottoposto a doppio controllo. Vengono copiati i dati dell'input penna necessari per consentire l'esecuzione del thread in background in modo indipendente.
3.  In T3, l' [**oggetto InkAnalyzer**](inkanalyzer.md) restituisce l'esecuzione del thread dell'interfaccia utente all'applicazione. **InkAnalyzer** crea un secondo thread, il thread di analisi in background e i motori di analisi e riconoscimento dell'input penna analizzano i dati dell'input penna copiato.
4.  Mentre l'operazione di analisi è in corso sul secondo thread in background, l'utente finale continua a modificare il documento, aggiungendo e rimuovendo i dati del tratto, a T4 e T5. Queste modifiche possono entrare in conflitto con il lavoro in corso di elaborazione in background.
5.  A T6, il thread in background ha completato l'operazione di analisi e i risultati sono pronti. Prima che l' [**oggetto InkAnalyzer**](inkanalyzer.md) comunichi i risultati all'applicazione, viene eseguito un algoritmo di riconciliazione per determinare se le modifiche apportate dall'utente durante il calcolo dell'operazione di analisi (T4 e T5) sono in conflitto con i risultati. Se vengono rilevati conflitti, i tratti in conflitto vengono contrassegnati per la ripetizione dell'analisi, operazione che viene eseguita la volta successiva che l'applicazione richiama l'operazione di analisi in background.
6.  Infine, in T7, con tutti i conflitti rilevati, l' [**oggetto InkAnalyzer**](inkanalyzer.md) presenta i risultati all'applicazione.

### <a name="extensibility"></a>Estendibilità

Le API InkAnalysis consentono l'uso da parte delle applicazioni di nuovi tipi di motori di analisi, in modo da evitare che l'applicazione debba riscrivere tutti i vantaggi dell'API InkAnalysis, tra cui la riconciliazione, il proxy di dati, la persistenza e l'analisi incrementale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 
