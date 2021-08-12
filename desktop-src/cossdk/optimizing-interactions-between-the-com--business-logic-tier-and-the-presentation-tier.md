---
description: In genere, la latenza tra i livelli di un'applicazione distribuita varia notevolmente.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Ottimizzazione delle interazioni tra il livello della logica di business COM+ e il livello presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca519c6aa7f1585648b0def6530b7f224f12a98961193e4f6f7cc490a747b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306103"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Ottimizzazione delle interazioni tra il livello della logica di business COM+ e il livello presentazione

In genere, la latenza tra i livelli di un'applicazione distribuita varia notevolmente. Le chiamate tra il livello presentazione e il livello di logica di business sono spesso un ordine di grandezza più lento rispetto alle chiamate tra il livello business e il livello dati. Di conseguenza, lo stato mantenuto è più diss costoso quando si effettua una chiamata al livello della logica di business.

Gli argomenti seguenti illustrano come passare i dati tra i livelli di presentazione e logica di business:

-   [Passaggio di parametri](#passing-parameters)
-   [Opzioni di passaggio dei dati](#data-passing-options)
-   [Uso di un modello factory per passare dati](#using-a-factory-pattern-to-pass-data)
-   [Argomenti correlati](#related-topics)

## <a name="passing-parameters"></a>Passaggio di parametri

Per passare un determinato set di informazioni tra il livello di presentazione e il livello della logica di business, è possibile avere una singola riga, più righe o una combinazione di una singola riga (ad esempio un'intestazione) e più righe di dati di dettaglio. Il modo più efficiente per passare queste informazioni tra i livelli è tramite una singola chiamata al metodo. Questa singola chiamata gestirebbe l'intero set di informazioni da passare. Questa operazione è necessaria a meno che non si scentassi di controllare la transazione dal livello di presentazione (e rendere identiche tutte le operazioni di trattamento delle transazioni nel livello di presentazione). Microsoft non consiglia di eseguire transazioni dal livello presentazione perché le chiamate tra questo livello e il livello di logica di business sono in genere le più lente di qualsiasi chiamata in un'applicazione multilivello.

Un modo per creare questo metodo è passare singole righe di informazioni come parametri e passare più righe come recordset ADO. I recordset sono alla base della metodologia di accesso ai dati ADO di Microsoft e l'uso dei recordset ADO consente di passare tutte le informazioni correlate a una singola transazione in un unico passaggio.

## <a name="data-passing-options"></a>Opzioni di passaggio dei dati

Esistono altre opzioni da considerare quando si passano i dati. Questi includono l'uso di un elenco di parametri e recordset ADO (come illustrato in precedenza), solo recordset ADO, stringhe con codifica XML o matrici di strutture. Questa sezione illustra ognuna di queste opzioni.

La tabella seguente illustra le aree in cui è necessario fare particolare attenzione quando si usa una delle quattro diverse possibilità di passaggio di argomenti. Una "X" rappresenta le aree in cui i compromessi devono essere compresi e ponderati in base alle esigenze di ogni progetto. Provare a non prendere decisioni per il passaggio di argomenti in base al componente. I vantaggi di un modello di programmazione coerente in un progetto superano di gran lunga qualsiasi vantaggio offerto dall'ottimizzazione in base al metodo o al componente in tutte le circostanze, ma le più estremi. Le colonne sono descritte nell'elenco che segue la tabella.



|     &nbsp;                  | Concorrenza  | WAN          | Distribuzione   | Complessità   |
|-----------------------|--------------|--------------|--------------|--------------|
| Voce | Valore |
| Recordset<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Matrici<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Le quattro colonne definiscono le aree da controllare quando si usa tale opzione per passare i parametri.

-   **La colonna Concorrenza rappresenta la** necessità di codificare o fornire un meccanismo che gestisce le condizioni di blocco nelle operazioni di aggiornamento. Poiché i metodi che eseguono operazioni di salvataggio possono rappresentare gli aggiornamenti, possono verificarsi problemi di concorrenza. Due tipi di blocco sono ottimistico e pessimistico prevalente. I blocchi pessimistici impediscono a un utente di ottenere dati per l'aggiornamento mentre un altro utente può eseguire un aggiornamento. Il blocco ottimistico supporta molti più utenti scambiando la probabilità che due utenti qualsiasi aggiornino lo stesso documento contemporaneamente. Il blocco ottimistico chiama per verificare che i dati archiviati corrispondano ai dati nel momento in cui è stato eseguito l'accesso a una copia dei dati per la modifica. I recordset ADO forniscono il supporto automatico per il blocco ottimistico. Gli scenari di aggiornamento che coinvolgono elenchi di parametri di riga singola non forniscono supporto sufficiente per il controllo della concorrenza. Il codice XML presenta questo stesso problema, in cui non è presente alcuna sensibilità al blocco nei dati XML.
-   **La colonna WAN rappresenta** le condizioni in cui potrebbe verificarsi una contentione di trasmissione in una rete WAN (Wide Area Network). Quando la rete WAN non ha capacità sufficiente per gestire tutti i dati spostati in qualsiasi momento, gli utenti dell'applicazione si verificano ritardi nei tempi di risposta. Per supportare la concorrenza ottimistica, i recordset ADO disconnessi passano due copie dei dati dal server al client. La seconda copia viene utilizzata dal client per determinare il set di righe di aggiornamento più piccolo da passare quando viene eseguito il commit di una modifica. Anche se questo riduce il traffico dal livello presentazione ai dati, il carico aggiuntivo della seconda copia può essere significativo. L'uso dei recordset come unico mezzo per passare tutte le informazioni comporta quindi il doppio del numero di dati da passare tra i livelli necessari, tranne quando il set di righe di aggiornamento viene passato di nuovo al livello dati da un livello presentazione.
-   **La colonna Distribuzione rappresenta** i problemi associati al passaggio dei dati quando è necessaria una tecnologia speciale sia sul lato chiamante che sul lato componente della rete. Ad esempio, l'uso di recordset ADO richiede che i componenti ADO siano presenti sia nel client che nel server. I parser XML devono essere presenti anche su entrambi i lati, per evitare di dover codificare i parser nelle applicazioni.
-   **La colonna Complessità è indicata** per tutte e quattro le scelte ed è una questione di preferenza o di esperienza del modello di programmazione precedente che potrebbe essere già stata stabilita nell'organizzazione di sviluppo. Alcuni utenti trovano che il passaggio dei parametri sia complesso e si senta troppo complesso nel problema di programmazione. Tenendo traccia del parametro che si sta gestendo e ottenendoli tutti visibili in un'unica finestra di modifica, è possibile creare una complessità logistica che alcuni sviluppatori trovano ingestibile.

Il metodo di passaggio dei parametri può anche avere compromessi, ad esempio:

-   I parametri possono comportare la gestione di più argomenti e tipi di argomento, nonché la necessità di decidere quando è appropriato impostare un recordset come parametro.
-   I recordset ADO possono ridurre le relazioni gerarchiche nei parametri dei metodi a uno o due argomenti. Questo semplifica notevolmente il modello di programmazione e supporta l'aggiunta di colonne in un secondo momento, ma nasconde anche la gerarchia delle informazioni. L'applicazione di informazioni a un recordset ADO e l'estrazione successiva comporta la conoscenza dei nomi di ogni colonna o l'ordine delle colonne. Questa situazione può aggiungere complessità per altri sviluppatori di componenti o applicazioni nel progetto.
-   XML è una rotazione diversa rispetto alla complicazione della gerarchia nascosta citata in precedenza. Il programmatore deve comprendere l'uso di un parser XML per ottenere l'accesso alle informazioni e spesso deve conoscere i nomi di ogni elemento nel set di dati prima di poter trovare il set di dati.
-   Le matrici di strutture introducono la necessità di una conoscenza comune delle informazioni passate sia dal chiamante che dal componente. Questa necessità di una mappa condivisa tra due elementi di sistema può causare difficoltà quando si gestiscono versioni diverse dei componenti. Anche se la firma del metodo potrebbe non cambiare, le modifiche alle informazioni previste possono rendere incompatibili i programmi chiamanti.

Poiché i problemi di complessità associati a tutti e quattro i metodi di passaggio dei parametri sono così simili, è disatteso che esiste un'opportunità di semplificazione significativa associata a una selezione.

## <a name="using-a-factory-pattern-to-pass-data"></a>Uso di un modello factory per passare dati

Un importante punto di progettazione è la facilità d'uso. Nel momento in cui si è deciso di usare i recordset ADO per passare un set strutturato di dettagli al livello presentazione, è stato introdotto un problema di complessità. I programmatori del livello presentazione devono comprendere la struttura di tali recordset. Un problema di maggiore complessità può verificarsi quando sono necessari più dettagli per passare un set di dati in un recordset. Per semplificare le operazioni, è consigliabile creare un metodo factory del recordset ogni volta che si prevede di richiedere il passare dati in recordset ADO strutturati.

La factory del recordset deve restituire al chiamante un recordset disconnesso vuoto ma scrivibile. Questo recordset deve avere i campi appropriati (nomi e tipi di dati) già configurati in modo che il client chiamante non debba sapere come produrre il recordset. Questo approccio viene spesso definito  modello factory ed è un modello di soluzione comune che risolve la necessità di creare un oggetto di una determinata complessità senza dover conoscere le sfumature della creazione.

Semplici scelte di progettazione, ad esempio la scelta dello stesso nome di parametro per lo stesso dato in ogni metodo in cui vengono passate le informazioni, semplificano l'aspetto di un metodo e la possibilità di conoscere il comportamento previsto. Assicurarsi che l'ordine in cui gli argomenti like vengono passati sia coerente in un'intera famiglia di metodi fornisce un punto di comfort che applica un modello coerente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione delle interazioni tra il livello della logica di business COM+ e il livello dati](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




