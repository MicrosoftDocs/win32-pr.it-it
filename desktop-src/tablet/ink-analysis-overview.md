---
description: Le API InkAnalysis offrono agli sviluppatori di Tablet PC potenti strumenti per esaminare l'input penna a livello di codice. L'API classifica l'input penna in categorie significative, ad esempio parole, linee, paragrafi e disegni.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Panoramica dell'analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3056a5e5fbff8be82f6df2de2a34fadd9761e50f451ee2d48c112589d1aff397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718927"
---
# <a name="ink-analysis-overview"></a>Panoramica dell'analisi input penna

Le API InkAnalysis offrono agli sviluppatori di Tablet PC potenti strumenti per esaminare l'input penna a livello di codice. L'API classifica l'input penna in categorie significative, ad esempio parole, linee, paragrafi e disegni.

È possibile usare ogni classificazione in diversi modi, incluso il miglioramento dei risultati di riconoscimento per la grafia.

## <a name="ink-analysis-basics"></a>Nozioni di base dell'analisi input penna

Questa sezione presenta la tecnologia di analisi dell'input penna della piattaforma Tablet PC e spiega quando e come usarla.

Le API InkAnalysis combinano in modo efficace due tecnologie distinte ma complementari: il riconoscimento della grafia e la classificazione del layout. La combinazione di queste due tecnologie offre risultati definitivamente maggiori rispetto alle parti prese da sole.

Il riconoscimento della grafia è l'analisi computazionale dell'input penna digitale scritto a mano per restituire l'interpretazione basata su caratteri in una determinata lingua. Ciò significa che il riconoscimento della grafia è il modo in cui il computer "legge" la grafia di una persona.

L'analisi dell'input penna può essere ulteriormente suddivisa in classificazione input penna e analisi del layout. La classificazione input penna è la divisione computazionale dell'input penna in unità semanticamente significative, ad esempio paragrafi, linee, parole e disegni. L'analisi del layout è l'esame computazionale dell'input penna per determinare la posizione dell'input penna sulla superficie di input penna e il modo in cui i tratti sono correlati tra loro dal punto di vista spaziale e anche semantico. Ad esempio, l'analisi del layout può indicare che una particolare parte dell'input penna è un'annotazione o una chiamata.

### <a name="recognition"></a>Riconoscimento

Un esempio di come la combinazione di riconoscimento con l'analisi input penna nell'API InkAnalysis aiuta lo sviluppatore è il miglioramento dei risultati del riconoscimento. I motori di riconoscimento della grafia per Tablet PC sono stati progettati principalmente per riconoscere una singola linea orizzontale dell'input penna. Tuttavia, gli utenti tendono a scrivere più righe quando si prendono appunti e non è garantito che tali righe siano orizzontali in relazione alla pagina. Con l'API InkAnalysis, l'input penna viene pre-elaborato dall'analizzatore input penna prima di essere inviato al sistema di riconoscimento. L'input penna analizzato viene trasformato in orizzontale prima di essere riconosciuto, migliorando i risultati del riconoscimento.

Altri vantaggi del riconoscimento derivano dal fatto che l'analizzatore input penna corregge le informazioni sull'ordine dei tratti non corretto prima di inviare l'input penna al riconoscimento. Inoltre, i risultati del riconoscimento sono ora disponibili in modo selettivo. In altri parole, lo sviluppatore può recuperare rapidamente i risultati del riconoscimento per una singola parola, riga o paragrafo in un'unica chiamata.

### <a name="ink-classification"></a>Classificazione input penna

Esistono naturalmente diversi scenari in cui è possibile mantenere intatti i dati dell'input penna, anziché convertirli immediatamente in testo. Anche l'analisi dell'input penna offre vantaggi in questo caso. In particolare, le API InkAnalysis offrono la possibilità di dividere i tratti input penna in base alla scrittura o ai disegni. I tratti input penna classificati come scritti sono quelli che costituiscono una parola o caratteri. Tutti gli altri tratti sono disegni. Ciò offre un nuovo modo per accedere ai dati input penna, abilitando nuovi scenari utente. Ad esempio, è possibile implementare la selezione in modo che sia diversa in base al tipo di tratto su cui l'utente tocca; Se un utente tocca un tratto di scrittura, l'applicazione seleziona l'intero set di tratti che compongono la parola. Se l'utente tocca uno stoke di disegno, l'applicazione seleziona solo tale tratto.

### <a name="layout-analysis"></a>Analisi del layout

L'analisi del layout utile va ben oltre la suddivisione relativamente semplice dell'input penna in componenti di scrittura e disegno.

L'analisi dell'input penna include anche una suddivisione più completa dei tratti di scrittura e disegno. Come esempio molto semplice, prendere un BLOB di input penna, come illustrato nella figura seguente.

![due semplici righe di scrittura manuale](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Dopo che la piattaforma ha analizzato questi tratti, restituisce una rappresentazione dell'albero di questi tratti, come illustrato nella figura seguente. Per questo semplice caso, l'albero contiene solo informazioni su paragrafi, linee e parole, ma la complessità di questo albero aumenta con l'aumentare della complessità del documento input penna.

![Rappresentazione ad albero di radice, paragrafo, righe e parole](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Poiché queste informazioni sono ora separate in unità gestibili, è ora possibile creare funzionalità più potenti. Ad esempio, l'applicazione può estendere la funzionalità in cui l'utente tocca per selezionare una parola in una funzionalità in cui l'utente tocca una volta per selezionare la parola, tocca due volte per selezionare l'intera riga e tocca tre volte per selezionare l'intero paragrafo. Sfruttando la struttura ad albero restituita dall'operazione di analisi, l'applicazione può correlare l'area toccata a un tratto nell'albero. Dopo che l'applicazione trova un tratto, può raggiungere l'albero per determinare come e quali tratti adiacenti selezionare.

La selezione di un'intera linea è un esempio semplicistico dei vantaggi dell'analisi dell'input penna, ma le possibilità diventano molto grandi se si considerano i diversi tipi di strutture gerarchiche che l'analizzatore dell'input penna è in grado di rilevare:

-   Elenchi ordinati e non ordinati
-   Forme
-   Commenti con annotazioni scritti inline con il testo

I tipi di funzionalità variano da applicazione a applicazione e si basano sui requisiti e sui motori di analisi e riconoscimento input penna disponibili.

### <a name="key-ink-analysis-features"></a>Funzionalità di analisi dell'input penna chiave

Le funzionalità principali dell'API InkAnalysis includono le funzionalità seguenti:

-   Analisi incrementale
-   Persistenza
-   Proxy dati
-   Riconciliazione
-   Estendibilità

### <a name="incremental-analysis"></a>Analisi incrementale

Quando gli utenti finali lavorano con l'input penna, in genere lo trattano come la grafia. L'input penna è continuamente soggetto a operazioni di modifica, ad esempio l'aggiunta di nuovo input penna, l'eliminazione dell'input penna esistente e la modifica delle proprietà dell'input penna, tutte eseguite nello stesso modo in cui la grafia viene modificata continuamente. Queste operazioni di modifica influiscono sui risultati dell'analisi. Quando si verificano modifiche, in genere possono essere isolate in sezioni del documento in determinati punti nel tempo. Si supponga, ad esempio, che un utente scrive cinque righe di input penna. Il modo standard in cui le applicazioni analizzano l'input penna è attendere che l'utente abbia terminato di scrivere tutte e cinque le righe dell'input penna, ad esempio un paragrafo, e quindi analizzare i risultati, in modo sincrono o asincrono.

È possibile ottimizzare il tempo complessivo impiegato per l'analisi di queste cinque righe isolando le aree analizzate durante la scrittura e quindi analizzando nuovamente solo le parti dei risultati che sono state modificate. Dopo l'analisi, la prima riga non verrà più riconosciuta a meno che non venga modificata dall'utente finale. Il riconoscimento della seconda riga viene considerato come un'operazione di riconoscimento indipendente.

Questo approccio incrementale funziona bene a livello di linea per le operazioni di riconoscimento, ma deve funzionare a un livello superiore per l'operazione di analisi dell'input penna. Poiché l'analizzatore input penna è in grado di rilevare classificazioni di livello superiore diverse per queste cinque righe di input penna (ad esempio, potrebbe essere un paragrafo standard o cinque elementi in un elenco), l'approccio incrementale per l'analizzatore input penna è che deve analizzare queste strutture superiori. Ciò significa che, dopo che l'analizzatore dell'input penna classifica la prima riga dell'input penna come linea, verifica che sia ancora una linea quando classifica la seconda riga. Tuttavia, l'analizzatore input penna isola questo controllo doppio al paragrafo e ignora il primo paragrafo durante l'analisi di un secondo paragrafo, trattando il secondo paragrafo come operazione indipendente dell'analizzatore input penna. Questo approccio incrementale all'analisi consente di risparmiare notevolmente il tempo di elaborazione quando sono già presenti grandi quantità di input penna nell'applicazione.

### <a name="persistence"></a>Persistenza

L'analisi incrementale funziona bene all'interno di una determinata sessione o istanza di [**un oggetto InkAnalyzer.**](inkanalyzer.md) Tuttavia, le API della piattaforma Tablet PC di prima generazione non possono eseguire l'analisi incrementale dopo che l'input penna è stato salvato in modo permanente su disco. L'API InkAnalysis consente di salvare l'input penna su disco insieme a una forma persistente dei risultati dell'analisi. I risultati dell'analisi possono essere caricati quando l'input penna viene caricato e possono essere inseriti in una nuova istanza di **inkAnalyzer.** Una nuova istanza dell'oggetto **InkAnalyzer** ha quindi lo stesso stato dei risultati che aveva in precedenza e può ora accettare qualsiasi modifica come modifiche incrementali allo stato esistente, anziché analizzare di nuovo tutti gli elementi.

### <a name="data-proxy"></a>Proxy dati

Molte applicazioni dispongono già di una struttura di documenti esistente nelle applicazioni. ad esempio un grafo o un database. [**InkAnalyzer presenta**](inkanalyzer.md) anche i risultati in un formato strutturato, in un albero di [**oggetti ContextNode.**](icontextnode.md) La **struttura InkAnalyzer** e la struttura esistente dell'applicazione devono interagire in due direzioni: i risultati vengono estratti da **InkAnalyzer** nell'applicazione e lo stato viene inserito dall'applicazione in **InkAnalyzer.**

Se il pull dei risultati da [**InkAnalyzer**](inkanalyzer.md) nella struttura dell'applicazione fosse tutto ciò che era necessario, sarebbe relativamente semplice. Le applicazioni possono scorrere l'albero dei risultati e copiare (integrare) tutti i risultati necessari nella struttura dei dati esistente. Tuttavia, poiché molte applicazioni orizzontali richiedono l'analisi incrementale e la persistenza su disco, il problema diventa bidirezionale. È necessario eseguire il push dello stato (risultati precedenti) dalla struttura dell'applicazione e il push in **InkAnalyzer.**

Per soddisfare questo requisito, [**InkAnalyzer**](inkanalyzer.md) contiene una serie di eventi generati nel momento appropriato durante un'operazione di analisi per consentire alle applicazioni di eseguire il proxy della richiesta di dati alle strutture esistenti. Questi eventi vengono generati solo per gli oggetti [**ContextNode**](icontextnode.md) richiesti dall'operazione incrementale.

### <a name="reconciliation"></a>Riconciliazione

La maggior parte delle applicazioni vuole analizzare l'input penna in background per mantenere al minimo le interruzioni dell'interfaccia utente. L'analisi dell'input penna in background causa tuttavia problemi se l'utente modifica l'input penna (o l'input penna adiacente) che viene analizzato. Ad esempio, se l'utente elimina l'input penna durante l'operazione in background, la struttura risultante rifletterà lo stato del documento all'avvio dell'operazione in background, anziché il momento in cui è stata completata.

Per facilitare le applicazioni, [**InkAnalyzer**](inkanalyzer.md) riconcilia le differenze nello stato del documento tra l'inizio e la fine dell'operazione di analisi. Le modifiche apportate dall'utente o dall'applicazione durante l'esecuzione dell'analisi in background sostituiscono sempre i risultati calcolati in background. Dopo la riconciliazione, vengono segnalate solo le parti della struttura dei risultati che non sono in conflitto con le modifiche del documento e i tratti in conflitto vengono contrassegnati per l'analisi futura. Alla successiva esecuzione dell'operazione di analisi in background, i risultati vengono ricalcolati in base al nuovo stato.

Il diagramma seguente illustra questo processo. Il tempo è espresso in modo lineare dall'alto verso il basso nel diagramma.

![processo per la riconcilezione delle modifiche dello stato del documento durante l'operazione di analisi](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  Al momento 1 (t1), l'applicazione sta raccogliendo input penna dall'utente finale, inclusa qualsiasi modifica dell'input penna, ad esempio aggiunta, rimozione o modifica.
2.  In t2, l'applicazione richiama l'operazione di analisi in background. [**InkAnalyzer**](inkanalyzer.md) determina quale input penna non ha risultati e quale input penna deve essere controllato due volte. Copia i dati dell'input penna necessari per consentire l'esecuzione indipendente del thread in background.
3.  In corrispondenza di t3, [**InkAnalyzer**](inkanalyzer.md) restituisce l'esecuzione del thread dell'interfaccia utente all'applicazione. **InkAnalyzer** crea un secondo thread, il thread di analisi in background e i motori di analisi e riconoscimento dell'input penna analizzano i dati dell'input penna copiati.
4.  Mentre l'operazione di analisi viene eseguita nel secondo thread in background, l'utente finale continua a modificare il documento, aggiungendo e rimuovendo i dati del tratto, in corrispondenza di t4 e t5. Queste modifiche possono essere in conflitto con il lavoro in corso di elaborazione in background.
5.  A t6, il thread in background ha completato l'operazione di analisi e i risultati sono pronti. Prima che [**InkAnalyzer**](inkanalyzer.md) comunichi i risultati all'applicazione, esegue un algoritmo di riconciliazione per determinare se le modifiche apportate dall'utente durante il calcolo dell'operazione di analisi (t4 e t5) sono in conflitto con i risultati. Se vengono rilevate collisioni, i tratti in conflitto vengono contrassegnati per la nuova analisi, che si verifica alla successiva chiamata dell'operazione di analisi in background da parte dell'applicazione.
6.  Infine, a t7, con tutte le collisioni rilevate, [**InkAnalyzer**](inkanalyzer.md) presenta i risultati all'applicazione.

### <a name="extensibility"></a>Estendibilità

Le API InkAnalysis consentono l'uso di nuovi tipi di motori di analisi da parte delle applicazioni, in modo da impedire all'applicazione di dover riscrivere tutti i vantaggi dell'API InkAnalysis, tra cui riconciliazione, proxy di dati, persistenza e analisi incrementale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft.Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 
