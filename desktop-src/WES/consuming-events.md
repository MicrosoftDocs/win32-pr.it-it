---
title: Utilizzo di eventi (registro eventi di Windows)
description: È possibile utilizzare gli eventi dai canali o dai file di log.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300862"
---
# <a name="consuming-events-windows-event-log"></a>Utilizzo di eventi (registro eventi di Windows)

È possibile utilizzare gli eventi dai canali o dai file di log. Per utilizzare gli eventi, è possibile utilizzare tutti gli eventi oppure è possibile specificare un'espressione XPath che identifichi gli eventi che si desidera utilizzare. Per determinare gli elementi e gli attributi di un evento che è possibile utilizzare nell'espressione XPath, vedere [schema di eventi](eventschema-schema.md).

Il registro eventi di Windows supporta un subset di XPath 1,0. Per informazioni dettagliate sulle limitazioni, vedere [limitazioni di XPath 1,0](#xpath-10-limitations).

Negli esempi seguenti vengono illustrate espressioni XPath semplici.


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



È possibile utilizzare direttamente le espressioni XPath quando si chiamano le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) oppure è possibile utilizzare una query XML strutturata contenente l'espressione XPath. Per query semplici che eseguono query sugli eventi da una singola origine, l'utilizzo di un'espressione XPath è corretto. Se l'espressione XPath è un'espressione composta che contiene più di 20 espressioni o si sta eseguendo una query per gli eventi da più origini, è necessario utilizzare una query XML strutturata. Per informazioni dettagliate sugli elementi di una query XML strutturata, vedere [schema di query](queryschema-schema.md).

Una query strutturata identifica l'origine degli eventi e uno o più selettori o gli eliminati. Un selettore contiene espressioni XPath che selezionano gli eventi dall'origine e un eliminatore contiene un'espressione XPath che impedisce la selezione degli eventi. È possibile selezionare gli eventi da più di un'origine. Se un selettore e un silenziatore identificano lo stesso evento, l'evento non viene incluso nel risultato.

Di seguito viene illustrata una query XML strutturata che specifica un set di selettori ed elementi di esclusione.


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



Il set di risultati della query non contiene uno snapshot degli eventi al momento della query. Il set di risultati include invece gli eventi al momento della query e conterrà anche tutti i nuovi eventi generati che corrispondono ai criteri di query durante l'enumerazione dei risultati.

> [!Note]  
> L'ordine degli eventi viene mantenuto per gli eventi scritti dallo stesso thread. Tuttavia, è possibile che gli eventi scritti da thread distinti in processori diversi di un computer con più processori non siano in ordine.

 

Per informazioni dettagliate sull'utilizzo degli eventi, vedere gli argomenti seguenti:

-   [Esecuzione di query per gli eventi](querying-for-events.md)
-   [Sottoscrizione di eventi](subscribing-to-events.md)
-   [Eventi di rendering](rendering-events.md)
-   [Formattazione dei messaggi di evento](formatting-event-messages.md)
-   [Eventi di segnalibro](bookmarking-events.md)

Gli strumenti per utenti finali standard per l'utilizzo di eventi sono:

-   [Visualizzatore eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   Cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) di Windows PowerShell
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitazioni di XPath 1,0

Il registro eventi di Windows supporta un subset di XPath 1,0. La restrizione principale è che solo gli elementi XML che rappresentano gli eventi possono essere selezionati da un selettore di eventi. Una query XPath che non seleziona un evento non è valida. Tutti i percorsi del selettore validi iniziano con \* o "Event". Tutti i percorsi di percorso operano sui nodi evento e sono costituiti da una serie di passaggi. Ogni passaggio è una struttura di tre parti: l'asse, il test del nodo e il predicato. Per ulteriori informazioni su queste parti e su XPath 1,0, vedere la pagina relativa a [XPath (XML Path Language)](https://www.w3.org/TR/xpath). Il registro eventi di Windows inserisce le restrizioni seguenti nell'espressione:

-   Axis: sono supportati solo l'attributo figlio (predefinito) e l'attributo (e l'asse abbreviato "@").
-   Test del nodo: sono supportati solo i nomi di nodo e i test NCName. Il \* carattere "", che seleziona qualsiasi carattere, è supportato.
-   Predicati: qualsiasi espressione XPath valida è accettabile se i percorsi del percorso sono conformi alle restrizioni seguenti:
    -   Sono supportati gli operatori standard **o**, **e**, =,! =, <=, <, >=, > e le parentesi.
    -   La generazione di un valore stringa per un nome di nodo non è supportata.
    -   La valutazione in ordine inverso non è supportata.
    -   I set di nodi non sono supportati.
    -   L'ambito dello spazio dei nomi non è supportato.
    -   Gli spazi dei nomi, l'elaborazione e i nodi di commento non sono supportati.
    -   Dimensioni del contesto non supportate.
    -   Le associazioni di variabili non sono supportate.
    -   La funzione position e il relativo riferimento alla matrice abbreviato sono supportati (solo nei nodi foglia).
    -   La funzione band è supportata. La funzione esegue un AND bit per bit per due argomenti numerici Integer. Se il risultato dell'operatore AND bit per bit è diverso da zero, la funzione restituisce true. in caso contrario, la funzione restituisce false.
    -   La funzione TimeDiff è supportata. La funzione calcola la differenza tra il secondo argomento e il primo argomento. Uno degli argomenti deve essere un numero letterale. Gli argomenti devono utilizzare la rappresentazione FILETIME. Il risultato è il numero di millisecondi tra due volte. Il risultato è positivo se il secondo argomento rappresenta un momento successivo. in caso contrario, è negativo. Quando il secondo argomento non viene specificato, viene utilizzata l'ora di sistema corrente.

 

 
