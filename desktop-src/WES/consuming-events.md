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
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="d584e-103">Utilizzo di eventi (registro eventi di Windows)</span><span class="sxs-lookup"><span data-stu-id="d584e-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="d584e-104">È possibile utilizzare gli eventi dai canali o dai file di log.</span><span class="sxs-lookup"><span data-stu-id="d584e-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="d584e-105">Per utilizzare gli eventi, è possibile utilizzare tutti gli eventi oppure è possibile specificare un'espressione XPath che identifichi gli eventi che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d584e-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="d584e-106">Per determinare gli elementi e gli attributi di un evento che è possibile utilizzare nell'espressione XPath, vedere [schema di eventi](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d584e-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="d584e-107">Il registro eventi di Windows supporta un subset di XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="d584e-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="d584e-108">Per informazioni dettagliate sulle limitazioni, vedere [limitazioni di XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="d584e-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="d584e-109">Negli esempi seguenti vengono illustrate espressioni XPath semplici.</span><span class="sxs-lookup"><span data-stu-id="d584e-109">The following examples show simple XPath expressions.</span></span>


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



<span data-ttu-id="d584e-110">È possibile utilizzare direttamente le espressioni XPath quando si chiamano le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) oppure è possibile utilizzare una query XML strutturata contenente l'espressione XPath.</span><span class="sxs-lookup"><span data-stu-id="d584e-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="d584e-111">Per query semplici che eseguono query sugli eventi da una singola origine, l'utilizzo di un'espressione XPath è corretto.</span><span class="sxs-lookup"><span data-stu-id="d584e-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="d584e-112">Se l'espressione XPath è un'espressione composta che contiene più di 20 espressioni o si sta eseguendo una query per gli eventi da più origini, è necessario utilizzare una query XML strutturata.</span><span class="sxs-lookup"><span data-stu-id="d584e-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="d584e-113">Per informazioni dettagliate sugli elementi di una query XML strutturata, vedere [schema di query](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d584e-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="d584e-114">Una query strutturata identifica l'origine degli eventi e uno o più selettori o gli eliminati.</span><span class="sxs-lookup"><span data-stu-id="d584e-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="d584e-115">Un selettore contiene espressioni XPath che selezionano gli eventi dall'origine e un eliminatore contiene un'espressione XPath che impedisce la selezione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="d584e-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="d584e-116">È possibile selezionare gli eventi da più di un'origine.</span><span class="sxs-lookup"><span data-stu-id="d584e-116">You can select events from more than one source.</span></span> <span data-ttu-id="d584e-117">Se un selettore e un silenziatore identificano lo stesso evento, l'evento non viene incluso nel risultato.</span><span class="sxs-lookup"><span data-stu-id="d584e-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="d584e-118">Di seguito viene illustrata una query XML strutturata che specifica un set di selettori ed elementi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="d584e-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


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



<span data-ttu-id="d584e-119">Il set di risultati della query non contiene uno snapshot degli eventi al momento della query.</span><span class="sxs-lookup"><span data-stu-id="d584e-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="d584e-120">Il set di risultati include invece gli eventi al momento della query e conterrà anche tutti i nuovi eventi generati che corrispondono ai criteri di query durante l'enumerazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="d584e-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="d584e-121">L'ordine degli eventi viene mantenuto per gli eventi scritti dallo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="d584e-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="d584e-122">Tuttavia, è possibile che gli eventi scritti da thread distinti in processori diversi di un computer con più processori non siano in ordine.</span><span class="sxs-lookup"><span data-stu-id="d584e-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="d584e-123">Per informazioni dettagliate sull'utilizzo degli eventi, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d584e-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="d584e-124">Esecuzione di query per gli eventi</span><span class="sxs-lookup"><span data-stu-id="d584e-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="d584e-125">Sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="d584e-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="d584e-126">Eventi di rendering</span><span class="sxs-lookup"><span data-stu-id="d584e-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="d584e-127">Formattazione dei messaggi di evento</span><span class="sxs-lookup"><span data-stu-id="d584e-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="d584e-128">Eventi di segnalibro</span><span class="sxs-lookup"><span data-stu-id="d584e-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="d584e-129">Gli strumenti per utenti finali standard per l'utilizzo di eventi sono:</span><span class="sxs-lookup"><span data-stu-id="d584e-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="d584e-130">[Visualizzatore eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d584e-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="d584e-131">Cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d584e-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="d584e-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="d584e-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="d584e-133">Limitazioni di XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="d584e-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="d584e-134">Il registro eventi di Windows supporta un subset di XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="d584e-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="d584e-135">La restrizione principale è che solo gli elementi XML che rappresentano gli eventi possono essere selezionati da un selettore di eventi.</span><span class="sxs-lookup"><span data-stu-id="d584e-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="d584e-136">Una query XPath che non seleziona un evento non è valida.</span><span class="sxs-lookup"><span data-stu-id="d584e-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="d584e-137">Tutti i percorsi del selettore validi iniziano con \* o "Event".</span><span class="sxs-lookup"><span data-stu-id="d584e-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="d584e-138">Tutti i percorsi di percorso operano sui nodi evento e sono costituiti da una serie di passaggi.</span><span class="sxs-lookup"><span data-stu-id="d584e-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="d584e-139">Ogni passaggio è una struttura di tre parti: l'asse, il test del nodo e il predicato.</span><span class="sxs-lookup"><span data-stu-id="d584e-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="d584e-140">Per ulteriori informazioni su queste parti e su XPath 1,0, vedere la pagina relativa a [XPath (XML Path Language)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="d584e-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="d584e-141">Il registro eventi di Windows inserisce le restrizioni seguenti nell'espressione:</span><span class="sxs-lookup"><span data-stu-id="d584e-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="d584e-142">Axis: sono supportati solo l'attributo figlio (predefinito) e l'attributo (e l'asse abbreviato "@").</span><span class="sxs-lookup"><span data-stu-id="d584e-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="d584e-143">Test del nodo: sono supportati solo i nomi di nodo e i test NCName.</span><span class="sxs-lookup"><span data-stu-id="d584e-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="d584e-144">Il \* carattere "", che seleziona qualsiasi carattere, è supportato.</span><span class="sxs-lookup"><span data-stu-id="d584e-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="d584e-145">Predicati: qualsiasi espressione XPath valida è accettabile se i percorsi del percorso sono conformi alle restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d584e-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="d584e-146">Sono supportati gli operatori standard **o**, **e**, =,! =, <=, <, >=, > e le parentesi.</span><span class="sxs-lookup"><span data-stu-id="d584e-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="d584e-147">La generazione di un valore stringa per un nome di nodo non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d584e-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="d584e-148">La valutazione in ordine inverso non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d584e-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="d584e-149">I set di nodi non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="d584e-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="d584e-150">L'ambito dello spazio dei nomi non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d584e-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="d584e-151">Gli spazi dei nomi, l'elaborazione e i nodi di commento non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="d584e-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="d584e-152">Dimensioni del contesto non supportate.</span><span class="sxs-lookup"><span data-stu-id="d584e-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="d584e-153">Le associazioni di variabili non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="d584e-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="d584e-154">La funzione position e il relativo riferimento alla matrice abbreviato sono supportati (solo nei nodi foglia).</span><span class="sxs-lookup"><span data-stu-id="d584e-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="d584e-155">La funzione band è supportata.</span><span class="sxs-lookup"><span data-stu-id="d584e-155">The Band function is supported.</span></span> <span data-ttu-id="d584e-156">La funzione esegue un AND bit per bit per due argomenti numerici Integer.</span><span class="sxs-lookup"><span data-stu-id="d584e-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="d584e-157">Se il risultato dell'operatore AND bit per bit è diverso da zero, la funzione restituisce true. in caso contrario, la funzione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="d584e-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="d584e-158">La funzione TimeDiff è supportata.</span><span class="sxs-lookup"><span data-stu-id="d584e-158">The timediff function is supported.</span></span> <span data-ttu-id="d584e-159">La funzione calcola la differenza tra il secondo argomento e il primo argomento.</span><span class="sxs-lookup"><span data-stu-id="d584e-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="d584e-160">Uno degli argomenti deve essere un numero letterale.</span><span class="sxs-lookup"><span data-stu-id="d584e-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="d584e-161">Gli argomenti devono utilizzare la rappresentazione FILETIME.</span><span class="sxs-lookup"><span data-stu-id="d584e-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="d584e-162">Il risultato è il numero di millisecondi tra due volte.</span><span class="sxs-lookup"><span data-stu-id="d584e-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="d584e-163">Il risultato è positivo se il secondo argomento rappresenta un momento successivo. in caso contrario, è negativo.</span><span class="sxs-lookup"><span data-stu-id="d584e-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="d584e-164">Quando il secondo argomento non viene specificato, viene utilizzata l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="d584e-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
