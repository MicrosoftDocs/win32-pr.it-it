---
description: In genere, la latenza tra i livelli di un'applicazione distribuita è molto diversa.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe6094cb12cc7875d8a18dea3d28ac55bf8d6ae2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305140"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello di presentazione

In genere, la latenza tra i livelli di un'applicazione distribuita è molto diversa. Le chiamate tra il livello di presentazione e il livello della logica di business sono spesso un ordine di grandezza più lento rispetto alle chiamate tra il livello business e il livello dati. Di conseguenza, lo stato mantenuto è più oneroso quando si chiama il livello della logica di business.

Negli argomenti seguenti vengono illustrati i modi per passare i dati tra i livelli di presentazione e della logica di business:

-   [Passaggio di parametri](#passing-parameters)
-   [Opzioni di passaggio dei dati](#data-passing-options)
-   [Uso di un modello factory per passare i dati](#using-a-factory-pattern-to-pass-data)
-   [Argomenti correlati](#related-topics)

## <a name="passing-parameters"></a>Passaggio di parametri

Per passare un set di informazioni specifico tra il livello di presentazione e il livello della logica di business, è possibile che sia presente una singola riga, più righe o una combinazione di una singola riga (ad esempio un'intestazione) e di più righe di dettaglio di dati. Il modo più efficiente per passare queste informazioni tra i livelli è tramite una singola chiamata al metodo. Questa singola chiamata gestirà l'intero set di informazioni da passare. Questa operazione è necessaria a meno che non si scelga di controllare la transazione dal livello di presentazione (e di rendere identico tutto il trattamento delle transazioni nel livello di presentazione nella funzione). Microsoft non consiglia di eseguire transazioni dal livello di presentazione perché le chiamate tra questo livello e il livello di logica di business sono in genere il più lento tra le chiamate in un'applicazione multilivello.

Un modo per creare un metodo di questo tipo consiste nel passare singole righe di informazioni come parametri e passare più righe come recordset ADO. I recordset rappresentano la base della metodologia di accesso ai dati ADO di Microsoft e l'utilizzo di recordset ADO consente di passare tutte le informazioni relative a una singola transazione in un unico passaggio.

## <a name="data-passing-options"></a>Opzioni di passaggio dei dati

Sono disponibili altre opzioni da considerare quando si passano i dati. Che includono l'utilizzo di un elenco di parametri e di recordset ADO (come illustrato in precedenza), solo recordset ADO, stringhe con codifica XML o matrici di strutture. In questa sezione viene illustrata ciascuna di queste opzioni.

La tabella seguente illustra le aree in cui è necessario prestare particolare attenzione quando si usa una delle quattro diverse possibilità di passaggio di argomenti. Una "X" rappresenta le aree in cui i compromessi devono essere compresi e ponderati in base alle esigenze di ogni progetto. Provare a non prendere decisioni che passano gli argomenti per ogni singolo componente. I vantaggi di un modello di programmazione coerente all'interno di un progetto superano di gran lunga tutti i vantaggi offerti dall'ottimizzazione in base al metodo o al singolo componente in tutte le circostanze, tranne le più estreme. Le colonne sono descritte nell'elenco che segue la tabella.



|                       | Concorrenza  | WAN          | Distribuzione   | Complessità   |
|-----------------------|--------------|--------------|--------------|--------------|
| Voce | Valore |
| Recordset<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Matrici<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Le quattro colonne definiscono le aree da controllare quando si usa tale opzione per passare i parametri.

-   **La colonna concorrenza** rappresenta la necessità di scrivere codice o fornire un meccanismo per gestire le condizioni di blocco sulle operazioni di aggiornamento. Poiché i metodi che eseguono i salvataggi possono rappresentare aggiornamenti, possono verificarsi problemi di concorrenza. Due tipi di blocco sono ottimistici e pessimistici prevalentemente. I blocchi pessimistici impediscono a un utente di recuperare i dati per l'aggiornamento, mentre un altro utente ha la possibilità di eseguire un aggiornamento. Il blocco ottimistico supporta un numero elevato di utenti, negoziando la probabilità che due utenti aggiornino lo stesso documento nello stesso momento. Il blocco ottimistico chiama per verificare che i dati archiviati corrispondano ai dati nel punto in cui è stato eseguito l'accesso a una copia dei dati per la modifica. I recordset ADO forniscono supporto automatico per il blocco ottimistico. Gli scenari di aggiornamento che coinvolgono elenchi di parametri a riga singola non forniscono supporto sufficiente per il controllo della concorrenza. XML soffre di questo stesso problema, in quanto non è presente alcuna consapevolezza di blocco nei dati XML.
-   **La colonna WAN** rappresenta le condizioni in cui è possibile che si verifichi una contesa di trasmissione in un Wide Area Network (WAN). Quando la rete WAN non dispone di capacità sufficiente per la gestione di tutti i dati spostati in una sola volta, gli utenti dell'applicazione ritarderanno i tempi di risposta. Per supportare la concorrenza ottimistica, i recordset ADO disconnessi passano due copie dei dati dal server al client. La seconda copia viene utilizzata dal client per determinare il set di righe di aggiornamento più piccolo da restituire quando viene eseguito il commit di una modifica. Anche se questa operazione riduce il traffico dal livello di presentazione ai dati, il carico aggiuntivo della seconda copia può essere significativo. L'utilizzo di recordset come unico mezzo per passare tutte le informazioni determina pertanto il passaggio del doppio dei dati tra i livelli in base alle esigenze, tranne quando il set di righe di aggiornamento viene passato nuovamente al livello dati da un livello di presentazione.
-   **La colonna di distribuzione rappresenta i** problemi associati al passaggio dei dati quando è necessaria una tecnologia speciale sia sul lato chiamante che sul lato componente della rete. Ad esempio, l'utilizzo di recordset ADO richiede che i componenti ADO siano presenti sia nel client che nel server. I parser XML devono essere presenti anche su entrambi i lati, per evitare di dover codificare i parser nelle applicazioni.
-   **La colonna complessità** è indicata per tutte e quattro le scelte ed è una questione di preferenza o di un modello di programmazione precedente che può essere già stabilito nell'organizzazione di sviluppo. Alcuni utenti trovano il passaggio dei parametri per essere ingombranti e si ritiene che aggiunga una complessità eccessiva al problema di programmazione. Tenere traccia del parametro che si sta gestendo e renderli visibili in un'unica finestra di modifica, può creare una complessità logistica che alcuni sviluppatori trovano non gestibili.

Anche il metodo di passaggio dei parametri può comportare compromessi, come i seguenti:

-   I parametri possono comportare la gestione di più argomenti e tipi di argomento, nonché la necessità di decidere quando è opportuno creare un recordset per un parametro.
-   I recordset ADO possono tagliare le relazioni gerarchiche nei parametri del metodo fino a uno o due argomenti. In questo modo, il modello di programmazione viene semplificato in modo significativo e viene supportata l'aggiunta di colonne in un secondo momento, ma viene nascosta anche la gerarchia delle informazioni. Le informazioni di riempimento in un recordset ADO e in un secondo momento l'estrazione includono i nomi di ogni colonna o l'ordine delle colonne. Questa situazione può aggiungere complessità per altri sviluppatori di componenti o applicazioni nel progetto.
-   XML è un altro spin sulla complicazione della gerarchia nascosta indicata in precedenza. Il programmatore deve comprendere l'uso di un parser XML per ottenere l'accesso alle informazioni e spesso deve conoscere i nomi di ogni elemento nel set di dati prima di poter trovare il set di dati.
-   Le matrici di strutture introducono la necessità di una conoscenza comune delle informazioni passate sulla parte del chiamante e del componente. Questa esigenza di una mappa condivisa tra due elementi di sistema può causare difficoltà quando si gestiscono versioni diverse dei componenti. Sebbene la firma del metodo non venga modificata, le modifiche apportate alle informazioni previste possono rendere incompatibili i programmi chiamante.

Poiché i problemi di complessità associati a tutti e quattro i metodi di passaggio dei parametri sono così simili, è discutibile che è presente un'opportunità di semplificazione significativa associata a una qualsiasi selezione.

## <a name="using-a-factory-pattern-to-pass-data"></a>Uso di un modello factory per passare i dati

Un punto di progettazione importante è la semplicità d'uso. Nel momento in cui si è deciso di utilizzare i recordset ADO per passare un set strutturato di dettagli al livello di presentazione, è stato introdotto un problema di complessità. I programmatori del livello presentazione devono comprendere la struttura di questi Recordset. Un problema di complessità maggiore può verificarsi quando sono necessari più dettagli per un set di dati da passare in un recordset. Per semplificare le cose, è consigliabile creare un metodo factory recordset quando si desidera che i dati vengano passati nei recordset ADO strutturati.

La Factory recordset deve restituire al chiamante un recordset disconnesso, ma scrivibile. Questo recordset deve avere i campi appropriati (nomi e tipi di dati) già configurati in modo che il client chiamante non debba essere in grado di produrre il recordset. Questo approccio viene spesso definito *modello di Factory* ed è un modello di soluzione comune che risolve la necessità di creare un oggetto di una determinata complessità senza che sia necessario conoscerne le sfumature.

Semplici scelte di progettazione, ad esempio la scelta dello stesso nome di parametro per lo stesso tipo di dati in tutti i metodi in cui vengono passate le informazioni, semplificano l'aspetto di un metodo e sanno cosa è previsto. Assicurarsi che l'ordine in cui vengono passati gli argomenti sia coerente in un'intera famiglia di metodi fornisce un punto di comodità che impone un modello coerente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello dati](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




