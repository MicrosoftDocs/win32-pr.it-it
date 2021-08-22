---
title: Utilizzo di eventi (Windows eventi)
description: È possibile utilizzare gli eventi dai canali o dai file di log.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131f0f3b02485c3c838e9180ea1daaebb4121b8846e5a124f36cfdb6bf377f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620381"
---
# <a name="consuming-events-windows-event-log"></a>Utilizzo di eventi (Windows eventi)

È possibile utilizzare gli eventi dai canali o dai file di log. Per utilizzare gli eventi, è possibile utilizzare tutti gli eventi oppure specificare un'espressione XPath che identifica gli eventi che si desidera utilizzare. Per determinare gli elementi e gli attributi di un evento che è possibile usare nell'espressione XPath, vedere [Schema di eventi.](eventschema-schema.md)

Windows Il registro eventi supporta un subset di XPath 1.0. Per informazioni dettagliate sulle limitazioni, vedere [Limitazioni di XPath 1.0.](#xpath-10-limitations)

Negli esempi seguenti vengono mostrate espressioni XPath semplici.


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



È possibile utilizzare le espressioni XPath direttamente quando si chiamano le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) oppure è possibile usare una query XML strutturata che contiene l'espressione XPath. Per query semplici in cui vengono eseguite query sugli eventi da una singola origine, l'uso di un'espressione XPath è un'operazione valida. Se l'espressione XPath è un'espressione composta che contiene più di 20 espressioni o si sta cercando eventi da più origini, è necessario utilizzare una query XML strutturata. Per informazioni dettagliate sugli elementi di una query XML strutturata, vedere [Schema di query.](queryschema-schema.md)

Una query strutturata identifica l'origine degli eventi e uno o più selettori o soppressori. Un selettore contiene un'espressione XPath che seleziona gli eventi dall'origine e un suppressor contiene un'espressione XPath che impedisce la selezione degli eventi. È possibile selezionare eventi da più di un'origine. Se un selettore e un soppressore identificano lo stesso evento, l'evento non viene incluso nel risultato.

Di seguito viene illustrata una query XML strutturata che specifica un set di selettori ed eliminatori.


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



Il set di risultati della query non contiene uno snapshot degli eventi al momento della query. Al contrario, il set di risultati include gli eventi al momento della query e conterrà anche tutti i nuovi eventi generati che corrispondono ai criteri di query durante l'enumerazione dei risultati.

> [!Note]  
> L'ordine degli eventi viene mantenuto per gli eventi scritti dallo stesso thread. Tuttavia, è possibile che gli eventi scritti da thread separati in processori diversi di un computer con più processori non vengano visualizzati in ordine.

 

Per informazioni dettagliate sull'utilizzo degli eventi, vedere gli argomenti seguenti:

-   [Esecuzione di query per gli eventi](querying-for-events.md)
-   [Sottoscrizione di eventi](subscribing-to-events.md)
-   [Eventi di rendering](rendering-events.md)
-   [Formattazione dei messaggi di evento](formatting-event-messages.md)
-   [Aggiunta di segnalibri agli eventi](bookmarking-events.md)

Gli strumenti standard dell'utente finale per l'utilizzo di eventi sono:

-   [Visualizzatore eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   Il cmdlet [Windows PowerShell Get-WinEvent](/previous-versions//dd367894(v=technet.10))
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitazioni di XPath 1.0

Windows Il registro eventi supporta un subset di XPath 1.0. La restrizione principale è che solo gli elementi XML che rappresentano gli eventi possono essere selezionati da un selettore di eventi. Una query XPath che non seleziona un evento non è valida. Tutti i percorsi del selettore validi \* iniziano con o "Event". Tutti i percorsi operano sui nodi evento e sono costituiti da una serie di passaggi. Ogni passaggio è una struttura di tre parti: asse, test del nodo e predicato. Per altre informazioni su queste parti e su XPath 1.0, vedere [XML Path Language (XPath)](https://www.w3.org/TR/xpath). Windows Nel registro eventi vengono applicate le restrizioni seguenti all'espressione:

-   Asse: sono supportati solo gli assi Figlio (impostazione predefinita) e Attributo (e la sintassi abbreviata "@").
-   Test del nodo: sono supportati solo i nomi dei nodi e i test NCName. Il carattere \* " ", che seleziona qualsiasi carattere, è supportato.
-   Predicati: qualsiasi espressione XPath valida è accettabile se i percorsi sono conformi alle restrizioni seguenti:
    -   Sono supportati gli operatori standard **OR**, **AND**, =, !=, <=, <, >=, > e parentesi.
    -   La generazione di un valore stringa per un nome di nodo non è supportata.
    -   La valutazione in ordine inverso non è supportata.
    -   I set di nodi non sono supportati.
    -   L'ambito dello spazio dei nomi non è supportato.
    -   I nodi spazio dei nomi, elaborazione e commento non sono supportati.
    -   Le dimensioni del contesto non sono supportate.
    -   Le associazioni di variabili non sono supportate.
    -   La funzione position e il relativo riferimento alla matrice abbreviata sono supportati (solo nei nodi foglia).
    -   La funzione Band è supportata. La funzione esegue un'operazione AND bit per bit per due argomenti di numeri interi. Se il risultato dell'operatore AND bit per bit è diverso da zero, la funzione restituisce true; In caso contrario, la funzione restituisce false.
    -   La funzione timediff è supportata. La funzione calcola la differenza tra il secondo argomento e il primo argomento. Uno degli argomenti deve essere un numero letterale. Gli argomenti devono usare la rappresentazione FILETIME. Il risultato è il numero di millisecondi tra due volte. Il risultato è positivo se il secondo argomento rappresenta un'ora successiva. in caso contrario, è negativo. Quando il secondo argomento non viene specificato, viene utilizzata l'ora di sistema corrente.

 

 
