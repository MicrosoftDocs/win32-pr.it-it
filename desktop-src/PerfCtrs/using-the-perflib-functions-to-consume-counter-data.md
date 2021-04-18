---
title: Uso delle funzioni PerfLib per utilizzare i dati dei contatore
description: Le funzioni API PerfLib possono essere usate per utilizzare i dati del contatore delle prestazioni V2 direttamente quando non è possibile usare PDH.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2020
ms.locfileid: "106300558"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a><span data-ttu-id="97d95-103">Uso delle funzioni PerfLib per utilizzare i dati dei contatore</span><span class="sxs-lookup"><span data-stu-id="97d95-103">Using the PerfLib Functions to Consume Counter Data</span></span>

<span data-ttu-id="97d95-104">Utilizzare le funzioni consumer PerfLib per utilizzare i dati sulle prestazioni dei provider di dati prestazioni V2 quando non è possibile utilizzare le [funzioni PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="97d95-104">Use the PerfLib Consumer functions to consume performance data from V2 performance data providers when you cannot use the [Performance Data Helper (PDH) functions](using-the-pdh-functions-to-consume-counter-data.md).</span></span> <span data-ttu-id="97d95-105">Queste funzioni possono essere usate durante la scrittura di applicazioni OneCore per la raccolta di V2 CounterSet o quando è necessario raccogliere V2 CounterSet con dipendenze minime e overhead.</span><span class="sxs-lookup"><span data-stu-id="97d95-105">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="97d95-106">Le funzioni consumer PerfLib V2 sono più difficili da usare rispetto alle funzioni PDH (Performance Data Helper) e supportano solo la raccolta dei dati dai provider v2.</span><span class="sxs-lookup"><span data-stu-id="97d95-106">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="97d95-107">Le funzioni PDH dovrebbero essere preferite per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="97d95-107">The PDH functions should be preferred for most applications.</span></span>

<span data-ttu-id="97d95-108">Le funzioni consumer PerfLib V2 sono l'API di basso livello per la raccolta dei dati dai **provider v2**.</span><span class="sxs-lookup"><span data-stu-id="97d95-108">The PerfLib V2 Consumer functions are the low-level API for collecting data from **V2 providers**.</span></span> <span data-ttu-id="97d95-109">Le funzioni consumer PerfLib V2 non supportano la raccolta di dati dai **provider v1**.</span><span class="sxs-lookup"><span data-stu-id="97d95-109">The PerfLib V2 Consumer functions do not support collecting data from **V1 providers**.</span></span>

> [!WARNING]
> <span data-ttu-id="97d95-110">Le funzioni consumer PerfLib V2 possono raccogliere dati da origini non attendibili, ad esempio da servizi locali con privilegi limitati o da computer remoti.</span><span class="sxs-lookup"><span data-stu-id="97d95-110">The PerfLib V2 consumer functions can potentially collect data from untrusted sources, e.g. from limited-privilege local services or from remote machines.</span></span> <span data-ttu-id="97d95-111">Le funzioni consumer PerfLib V2 non convalidano i dati per l'integrità o la coerenza.</span><span class="sxs-lookup"><span data-stu-id="97d95-111">The PerfLib V2 consumer functions do not validate the data for integrity or consistency.</span></span> <span data-ttu-id="97d95-112">Spetta all'applicazione consumer verificare che i dati restituiti siano coerenti, ad esempio che i valori delle dimensioni nel blocco di dati restituito non superino le dimensioni effettive del blocco di dati restituito.</span><span class="sxs-lookup"><span data-stu-id="97d95-112">It is up to your consumer application to verify that the returned data is consistent, e.g. that the Size values in the returned data block do not exceed the actual size of the returned data block.</span></span> <span data-ttu-id="97d95-113">Ciò è particolarmente importante quando l'applicazione consumer viene eseguita con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="97d95-113">This is especially important when the consumer application runs at elevated privilege.</span></span>

## <a name="perflib-usage"></a><span data-ttu-id="97d95-114">Utilizzo di PerfLib</span><span class="sxs-lookup"><span data-stu-id="97d95-114">PerfLib Usage</span></span>

<span data-ttu-id="97d95-115">L' `perflib.h` intestazione include le dichiarazioni utilizzate dai provider in modalità utente V2 (ovvero l'API del provider Perflib) e i consumer V2 (ovvero l'API del consumer di Perflib).</span><span class="sxs-lookup"><span data-stu-id="97d95-115">The `perflib.h` header includes the declarations used by V2 user-mode providers (i.e. the PerfLib Provider API) and V2 consumers (i.e. the PerfLib Consumer API).</span></span> <span data-ttu-id="97d95-116">Dichiara le funzioni seguenti per l'utilizzo dei dati sulle prestazioni V2:</span><span class="sxs-lookup"><span data-stu-id="97d95-116">It declares the following functions for consuming V2 performance data:</span></span>

- <span data-ttu-id="97d95-117">Usare [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) per ottenere i GUID di CounterSet registrati dai provider v2 nel sistema.</span><span class="sxs-lookup"><span data-stu-id="97d95-117">Use [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) to get the GUIDs of the countersets that are registered by the V2 providers on the system.</span></span>
- <span data-ttu-id="97d95-118">Usare [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) per ottenere informazioni su un determinato contatore, ad esempio il nome, la descrizione, il tipo (a istanza singola o a istanza singola), i tipi di contatore, i nomi dei contatori e le descrizioni dei contatori.</span><span class="sxs-lookup"><span data-stu-id="97d95-118">Use [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) to get information about a particular counterset such as the counterset's name, description, type (single-instance or multi-instance), counter types, counter names, and counter descriptions.</span></span>
- <span data-ttu-id="97d95-119">Usare [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) per ottenere i nomi delle istanze attualmente attive di un contatore a più istanze.</span><span class="sxs-lookup"><span data-stu-id="97d95-119">Use [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) to get the names of the currently-active instances of a multi-instance counterset.</span></span>
- <span data-ttu-id="97d95-120">Usare [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) per creare un nuovo handle di query da usare per la raccolta di dati da uno o più CounterSet.</span><span class="sxs-lookup"><span data-stu-id="97d95-120">Use [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) to create a new query handle to use for collecting data from one or more countersets.</span></span>
- <span data-ttu-id="97d95-121">Usare [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) per chiudere un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-121">Use [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) to close a query handle.</span></span>
- <span data-ttu-id="97d95-122">Usare [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) per aggiungere una query a un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-122">Use [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) to add a query to a query handle.</span></span>
- <span data-ttu-id="97d95-123">Usare [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) per rimuovere una query da un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-123">Use [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) to remove a query from a query handle.</span></span>
- <span data-ttu-id="97d95-124">Usare [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) per ottenere informazioni sulle query correnti su un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-124">Use [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) to get information about the current queries on a query handle.</span></span>
- <span data-ttu-id="97d95-125">Usare [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) per raccogliere i dati sulle prestazioni da un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-125">Use [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) to collect the performance data from a query handle.</span></span>

<span data-ttu-id="97d95-126">Se il consumer utilizzerà i dati solo da un provider specifico in cui gli indici GUID e contatore sono stabili e si ha accesso al file di simboli generato da [CTRPP](ctrpp.md)(dal `-ch` parametro CTRPP), è possibile impostare come hardcoded il GUID del contatore e i valori degli indici dei contatori nel consumer.</span><span class="sxs-lookup"><span data-stu-id="97d95-126">If your consumer will be consuming data only from a specific provider where the GUID and counter indexes are stable and you have access to the [CTRPP](ctrpp.md)-generated symbol file (from the CTRPP `-ch` parameter), you can hard-code the counterset GUID and counter index values into your consumer.</span></span>

<span data-ttu-id="97d95-127">In caso contrario, sarà necessario caricare i metadati del contatore per determinare i GUID del contatore e gli indici dei contatori da usare nella query come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="97d95-127">Otherwise, you will need to load counterset metadata to determine the counterset GUID(s) and counter indexes to use in your query as follows:</span></span>

- <span data-ttu-id="97d95-128">Usare **PerfEnumerateCounterSet** per ottenere un elenco di GUID del contatore di contatori supportati.</span><span class="sxs-lookup"><span data-stu-id="97d95-128">Use **PerfEnumerateCounterSet** to get a list of supported counterset GUIDs.</span></span>
- <span data-ttu-id="97d95-129">Per ogni GUID, usare **PerfQueryCounterSetRegistrationInfo** per caricare il nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="97d95-129">For each GUID, use **PerfQueryCounterSetRegistrationInfo** to load the counterset name.</span></span> <span data-ttu-id="97d95-130">Arrestare quando si trova il nome che si sta cercando.</span><span class="sxs-lookup"><span data-stu-id="97d95-130">Stop when you find the name you are looking for.</span></span>
- <span data-ttu-id="97d95-131">Usare **PerfQueryCounterSetRegistrationInfo** per caricare i metadati rimanenti (configurazione di contatori, nomi dei contatori, indici dei contatori, tipi di contatori) per quel contatore.</span><span class="sxs-lookup"><span data-stu-id="97d95-131">Use **PerfQueryCounterSetRegistrationInfo** to load the remaining metadata (counterset configuration, counter names, counter indexes, counter types) for that counterset.</span></span>

<span data-ttu-id="97d95-132">Se è sufficiente ottenere informazioni sui nomi delle istanze attualmente attive di un contatore, ad esempio se non sono necessari i valori effettivi dei dati sulle prestazioni, è possibile usare **PerfEnumerateCounterSetInstances**.</span><span class="sxs-lookup"><span data-stu-id="97d95-132">If you just need to know the names of the currently-active instances of a counterset (i.e. if you do not need the actual performance data values), you can use **PerfEnumerateCounterSetInstances**.</span></span> <span data-ttu-id="97d95-133">Questo accetta un GUID del contatore come input e restituisce un `PERF_INSTANCE_HEADER` blocco con i nomi e gli ID delle istanze attualmente attive del contatore specificato.</span><span class="sxs-lookup"><span data-stu-id="97d95-133">This takes a counterset GUID as input and returns a `PERF_INSTANCE_HEADER` block with the names and IDs of the currently-active instances of the given counterset.</span></span>

### <a name="queries"></a><span data-ttu-id="97d95-134">Query</span><span class="sxs-lookup"><span data-stu-id="97d95-134">Queries</span></span>

<span data-ttu-id="97d95-135">Per raccogliere i dati sulle prestazioni, è necessario creare un handle di query, aggiungervi query e raccogliere i dati dalle query.</span><span class="sxs-lookup"><span data-stu-id="97d95-135">To collect performance data, you need to create a query handle, add queries to it, and collect the data from the queries.</span></span>

<span data-ttu-id="97d95-136">A un handle di query possono essere associate diverse query.</span><span class="sxs-lookup"><span data-stu-id="97d95-136">A query handle can have many queries associated with it.</span></span> <span data-ttu-id="97d95-137">Quando si chiama **PerfQueryCounterData** per un handle di query, Perflib eseguirà tutte le query dell'handle e raccoglierà tutti i risultati.</span><span class="sxs-lookup"><span data-stu-id="97d95-137">When you call **PerfQueryCounterData** for a query handle, PerfLib will execute all of the handle's queries and collect all of the results.</span></span>

<span data-ttu-id="97d95-138">Ogni query specifica un GUID del contatore dei contatori, un filtro del nome di istanza, un filtro di ID istanza facoltativo e un filtro ID contatore facoltativo.</span><span class="sxs-lookup"><span data-stu-id="97d95-138">Each query specifies a counterset GUID, an instance name filter, an optional instance ID filter, and an optional counter ID filter.</span></span>

- <span data-ttu-id="97d95-139">Il GUID del contatore è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="97d95-139">The counterset GUID is required.</span></span> <span data-ttu-id="97d95-140">Indica il GUID del contatore dal quale la query raccoglierà i dati.</span><span class="sxs-lookup"><span data-stu-id="97d95-140">It indicates the GUID of the counterset from which the query will collect data.</span></span> <span data-ttu-id="97d95-141">Questa operazione è simile alla `FROM` clausola di una query SQL.</span><span class="sxs-lookup"><span data-stu-id="97d95-141">This is similar to the `FROM` clause of a SQL query.</span></span>
- <span data-ttu-id="97d95-142">Il filtro del nome dell'istanza è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="97d95-142">The instance name filter is required.</span></span> <span data-ttu-id="97d95-143">Indica un modello di carattere jolly che deve corrispondere al nome dell'istanza per l'istanza da includere nella query, con l' `*` indicazione di "any characters" e l' `?` indicazione di "One character".</span><span class="sxs-lookup"><span data-stu-id="97d95-143">It indicates a wildcard pattern that the instance name must match for the instance to be included in the query, with `*` indicating "any characters" and `?` indicating "one character".</span></span> <span data-ttu-id="97d95-144">Per CounterSet a istanza singola questa impostazione **deve** essere impostata su una stringa di lunghezza zero `""` .</span><span class="sxs-lookup"><span data-stu-id="97d95-144">For single-instance countersets this **MUST** be set to a zero-length string `""`.</span></span> <span data-ttu-id="97d95-145">Per CounterSet a più istanze, questo valore **deve** essere impostato su una stringa non vuota (usare `"*"` per accettare tutti i nomi di istanza).</span><span class="sxs-lookup"><span data-stu-id="97d95-145">For multi-instance countersets this **MUST** be set to a non-empty string (use `"*"` to accept all instance names).</span></span> <span data-ttu-id="97d95-146">Questa operazione è simile a una `WHERE InstanceName LIKE NameFilter` clausola di una query SQL.</span><span class="sxs-lookup"><span data-stu-id="97d95-146">This is similar to a `WHERE InstanceName LIKE NameFilter` clause of a SQL query.</span></span>
- <span data-ttu-id="97d95-147">Il filtro ID istanza è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="97d95-147">The instance ID filter is optional.</span></span> <span data-ttu-id="97d95-148">Se presente (ovvero se è impostato su un valore diverso da `0xFFFFFFFF` ), indica che la query deve raccogliere solo le istanze in cui l'ID istanza corrisponde all'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="97d95-148">If present (i.e. if set to a value other than `0xFFFFFFFF`), it indicates that the query should only collect instances where the instance ID matches the specified ID.</span></span> <span data-ttu-id="97d95-149">Se assente, ovvero se è impostato su `0xFFFFFFFF` , indica che la query deve accettare tutti gli ID istanza.</span><span class="sxs-lookup"><span data-stu-id="97d95-149">If absent (i.e. if set to `0xFFFFFFFF`), it indicates that the query should accept all instance IDs.</span></span> <span data-ttu-id="97d95-150">Questa operazione è simile a una `WHERE InstanceId == IdFilter` clausola di una query SQL.</span><span class="sxs-lookup"><span data-stu-id="97d95-150">This is similar to a `WHERE InstanceId == IdFilter` clause of a SQL query.</span></span>
- <span data-ttu-id="97d95-151">Il filtro ID contatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="97d95-151">The counter ID filter is optional.</span></span> <span data-ttu-id="97d95-152">Se presente (ad esempio, se è impostato su un valore diverso da `PERF_WILDCARD_COUNTER` ), indica che la query deve raccogliere un singolo contatore, simile a una `SELECT CounterName` clausola di una query SQL.</span><span class="sxs-lookup"><span data-stu-id="97d95-152">If present (i.e. if set to a value other than `PERF_WILDCARD_COUNTER`), it indicates that the query should collect a single counter, similar to a `SELECT CounterName` clause of a SQL query.</span></span> <span data-ttu-id="97d95-153">Se assente, ovvero se impostato su `PERF_WILDCARD_COUNTER` , indica che la query deve raccogliere tutti i contatori disponibili, in modo analogo a una `SELECT *` clausola di una query SQL.</span><span class="sxs-lookup"><span data-stu-id="97d95-153">If absent (i.e. if set to `PERF_WILDCARD_COUNTER`), it indicates that the query should collect all available counters, similar to a `SELECT *` clause of a SQL query.</span></span>

<span data-ttu-id="97d95-154">Usare **PerfAddCounters** per aggiungere query a un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-154">Use **PerfAddCounters** to add queries to a query handle.</span></span> <span data-ttu-id="97d95-155">Usare **PerfDeleteCounters** per rimuovere query da un handle di query.</span><span class="sxs-lookup"><span data-stu-id="97d95-155">Use **PerfDeleteCounters** to remove queries from a query handle.</span></span>

<span data-ttu-id="97d95-156">Dopo aver modificato le query in un handle di query, utilizzare **PerfQueryCounterInfo** per ottenere gli indici della query.</span><span class="sxs-lookup"><span data-stu-id="97d95-156">After changing the queries in a query handle, use **PerfQueryCounterInfo** to obtain the query indexes.</span></span> <span data-ttu-id="97d95-157">Gli indici indicano l'ordine in cui i risultati della query verranno restituiti da **PerfQueryCounterData** (i risultati non corrisponderanno sempre all'ordine in cui sono state aggiunte le query).</span><span class="sxs-lookup"><span data-stu-id="97d95-157">The indexes indicate the order in which the query results will be returned by **PerfQueryCounterData** (the results will not always match the order in which the queries were added).</span></span>

<span data-ttu-id="97d95-158">Quando l'handle di query è pronto, usare **PerfQueryCounterData** per raccogliere i dati.</span><span class="sxs-lookup"><span data-stu-id="97d95-158">Once the query handle is ready, use **PerfQueryCounterData** to collect the data.</span></span> <span data-ttu-id="97d95-159">In genere i dati vengono raccolti periodicamente, una volta al secondo o una volta al minuto, quindi elaborati i dati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="97d95-159">You will normally collect the data periodically (once a second or once a minute) then process the data as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="97d95-160">I contatori delle prestazioni non sono progettati per essere raccolti più di una volta al secondo.</span><span class="sxs-lookup"><span data-stu-id="97d95-160">Performance counters are not designed to be collected more than once per second.</span></span>

<span data-ttu-id="97d95-161">**PerfQueryCounterData** restituirà un `PERF_DATA_HEADER` blocco costituito da un'intestazione di dati con timestamp seguito da una sequenza di `PERF_COUNTER_HEADER` blocchi, ognuno dei quali contiene i risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="97d95-161">**PerfQueryCounterData** will return a `PERF_DATA_HEADER` block, which consists of a data header with timestamps followed by a sequence of `PERF_COUNTER_HEADER` blocks, each containing the results of one query.</span></span>

<span data-ttu-id="97d95-162">`PERF_COUNTER_HEADER`Può contenere diversi tipi di dati, come indicato dal valore del `dwType` campo:</span><span class="sxs-lookup"><span data-stu-id="97d95-162">The `PERF_COUNTER_HEADER` may contain various different kinds of data, as indicated by the value of the `dwType` field:</span></span>

- <span data-ttu-id="97d95-163">`PERF_ERROR_RETURN` -PerfLib non è in grado di recuperare i dati del contatore validi dal provider.</span><span class="sxs-lookup"><span data-stu-id="97d95-163">`PERF_ERROR_RETURN` - PerfLib cannot get valid counter data back from provider.</span></span>
- <span data-ttu-id="97d95-164">`PERF_SINGLE_COUNTER` -La query è stata eseguita per un singolo contatore da un contatore a istanza singola.</span><span class="sxs-lookup"><span data-stu-id="97d95-164">`PERF_SINGLE_COUNTER` - The query was for a single counter from a single-instance counterset.</span></span> <span data-ttu-id="97d95-165">I risultati contengono solo il valore del contatore richiesto.</span><span class="sxs-lookup"><span data-stu-id="97d95-165">The results contain only the requested counter value.</span></span>
- <span data-ttu-id="97d95-166">`PERF_MULTIPLE_COUNTERS` -La query era per più contatori da un contatore a istanza singola.</span><span class="sxs-lookup"><span data-stu-id="97d95-166">`PERF_MULTIPLE_COUNTERS` - The query was for multiple counters from a single-instance counterset.</span></span> <span data-ttu-id="97d95-167">Il risultato contiene i valori dei contatori insieme alle informazioni per la corrispondenza di ogni valore con il contatore corrispondente, ovvero le intestazioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="97d95-167">The result contains the counter values along with information for matching each value up with the corresponding counter (i.e. column headings).</span></span>
- <span data-ttu-id="97d95-168">`PERF_MULTIPLE_INSTANCES` -La query è stata eseguita per un singolo contatore da un contatore a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="97d95-168">`PERF_MULTIPLE_INSTANCES` - The query was for a single counter from a multi-instance counterset.</span></span> <span data-ttu-id="97d95-169">I risultati contengono le informazioni sull'istanza, ad esempio le intestazioni di riga, e un valore del contatore per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="97d95-169">The results contain the instance information (i.e. row headings) and one counter value per instance.</span></span>
- <span data-ttu-id="97d95-170">`PERF_COUNTERSET` -La query era per più contatori da un contatore di più istanze.</span><span class="sxs-lookup"><span data-stu-id="97d95-170">`PERF_COUNTERSET` - The query was for multiple counters from a multi-instance counterset.</span></span> <span data-ttu-id="97d95-171">I risultati contengono le informazioni sull'istanza, ad esempio le intestazioni di riga, i valori dei contatori per ogni istanza e le informazioni per la corrispondenza di ogni valore con il contatore corrispondente, ovvero le intestazioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="97d95-171">The results contain the instance information (i.e. row headings), the counter values for each instance, and information for matching each value up with the corresponding counter (i.e. column headings).</span></span>

<span data-ttu-id="97d95-172">I valori restituiti da **PerfQueryCounterData** sono `UINT32` `UINT64` valori non elaborati.</span><span class="sxs-lookup"><span data-stu-id="97d95-172">The values returned by **PerfQueryCounterData** are `UINT32` or `UINT64` raw values.</span></span> <span data-ttu-id="97d95-173">Che in genere richiedono una certa elaborazione per produrre i valori formattati previsti.</span><span class="sxs-lookup"><span data-stu-id="97d95-173">These usually require some processing to produce the expected formatted values.</span></span> <span data-ttu-id="97d95-174">L'elaborazione richiesta dipende dal tipo del contatore.</span><span class="sxs-lookup"><span data-stu-id="97d95-174">The required processing depends on the counter's type.</span></span> <span data-ttu-id="97d95-175">Molti tipi di contatori richiedono informazioni aggiuntive per l'elaborazione completa, ad esempio un timestamp o un valore da un contatore "base" nello stesso campione.</span><span class="sxs-lookup"><span data-stu-id="97d95-175">Many counter types require additional information for complete processing, such as a timestamp or a value from a "base" counter in the same sample.</span></span>

<span data-ttu-id="97d95-176">Alcuni tipi di contatori sono contatori "Delta" significativi solo se confrontati con i dati di un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="97d95-176">Some counter types are "delta" counters that are only meaningful when compared with the data from a previous sample.</span></span> <span data-ttu-id="97d95-177">Un contatore di tipo, ad esempio, `PERF_SAMPLE_COUNTER` ha un valore formattato che dovrebbe mostrare una frequenza (il numero di volte in cui si è verificato un determinato evento al secondo nell'intervallo di campionamento), ma il valore non elaborato effettivo è semplicemente un conteggio (il numero di volte in cui si è verificato un evento specifico in totale).</span><span class="sxs-lookup"><span data-stu-id="97d95-177">For example, a counter of type `PERF_SAMPLE_COUNTER` has a formatted value that is expected to show a rate (the number of times a particular thing happened per second over the sample interval), but the actual raw value is just a count (the number of times a particular thing has happened in total).</span></span> <span data-ttu-id="97d95-178">Per produrre il valore formattato "frequenza", è necessario applicare la formula corrispondente al tipo di contatore.</span><span class="sxs-lookup"><span data-stu-id="97d95-178">To produce the formatted "rate" value, you must apply the formula corresponding to the counter type.</span></span> <span data-ttu-id="97d95-179">La formula per `PERF_SAMPLE_COUNTER` è `(N1 - N0) / ((T1 - T0) / F)` : sottrae il valore dell'esempio corrente dal valore del campione precedente (indicando il numero di volte in cui si è verificato l'evento durante l'intervallo di campionamento), quindi divide il risultato per il numero di secondi nell'intervallo di campionamento (ottenuto sottraendo il timestamp del campione corrente dal timestamp dell'esempio precedente e dividendo per frequenza per convertire l'intervallo di tempo in</span><span class="sxs-lookup"><span data-stu-id="97d95-179">The formula for `PERF_SAMPLE_COUNTER` is `(N1 - N0) / ((T1 - T0) / F)`: subtract the current sample's value from the previous sample's value (giving the number of times the event occurred during the sample interval) then divide the result by the number of seconds in the sample interval (obtained by subtracting the current sample's timestamp from the previous sample's timestamp and dividing by frequency to convert the timespan into seconds).</span></span>

<span data-ttu-id="97d95-180">Vedere [calcolo dei valori dei contatori](calculating-counter-values.md) per ulteriori informazioni sul calcolo dei valori formattati da valori non elaborati.</span><span class="sxs-lookup"><span data-stu-id="97d95-180">Refer to [Calculating Counter Values](calculating-counter-values.md) for more information on computing formatted values from raw values.</span></span>

## <a name="sample"></a><span data-ttu-id="97d95-181">Esempio</span><span class="sxs-lookup"><span data-stu-id="97d95-181">Sample</span></span>

<span data-ttu-id="97d95-182">Il codice seguente implementa un consumer che usa le funzioni consumer PerfLib V2 per leggere le informazioni sulle prestazioni della CPU dal contatore "Information Processor".</span><span class="sxs-lookup"><span data-stu-id="97d95-182">The following code implements a consumer that uses the PerfLib V2 Consumer functions to read CPU performance information from the "Processor Information" counterset.</span></span>

<span data-ttu-id="97d95-183">Il consumer è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="97d95-183">The consumer is organized as follows:</span></span>

- <span data-ttu-id="97d95-184">La `CpuPerfCounters` classe implementa la logica per l'utilizzo dei dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="97d95-184">The `CpuPerfCounters` class implements the logic for consuming performance data.</span></span> <span data-ttu-id="97d95-185">Incapsula un handle di query e un buffer dei dati in cui vengono registrati i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="97d95-185">It encapsulates a query handle and a data buffer into which query results are recorded.</span></span>
- <span data-ttu-id="97d95-186">La `CpuPerfTimestamp` struttura archivia le informazioni sul timestamp per un esempio.</span><span class="sxs-lookup"><span data-stu-id="97d95-186">The `CpuPerfTimestamp` struct stores the timestamp information for a sample.</span></span> <span data-ttu-id="97d95-187">Ogni volta che vengono raccolti i dati, il chiamante riceve un singolo `CpuPerfTimestamp` .</span><span class="sxs-lookup"><span data-stu-id="97d95-187">Each time data is collected the caller receives a single `CpuPerfTimestamp`.</span></span>
- <span data-ttu-id="97d95-188">La `CpuPerfData` struttura archivia le informazioni sulle prestazioni (nome istanza e valori di prestazioni non elaborate) per una CPU.</span><span class="sxs-lookup"><span data-stu-id="97d95-188">The `CpuPerfData` struct stores the performance information (instance name and raw performance values) for one CPU.</span></span> <span data-ttu-id="97d95-189">Ogni volta che vengono raccolti i dati, il chiamante riceve una matrice di `CpuPerfData` (uno per CPU).</span><span class="sxs-lookup"><span data-stu-id="97d95-189">Each time data is collected the caller receives an array of `CpuPerfData` (one per CPU).</span></span>

<span data-ttu-id="97d95-190">Questo esempio usa i valori GUID del contatore e ID contatore hardcoded perché è ottimizzato per un determinato contatore (informazioni sul processore) che non modifica i valori GUID o ID.</span><span class="sxs-lookup"><span data-stu-id="97d95-190">This sample uses hard-coded counterset GUID and counter ID values because it is optimized for a specific counterset (Processor Information) that will not change GUID or ID values.</span></span> <span data-ttu-id="97d95-191">Una classe più generica che legge i dati sulle prestazioni da CounterSet arbitrario deve usare **PerfQueryCounterSetRegistrationInfo** per cercare il mapping tra gli ID contatore e i valori dei contatori in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="97d95-191">A more-generic class that reads performance data from arbitrary countersets would need to use **PerfQueryCounterSetRegistrationInfo** to look up the mapping between counter IDs and counter values at runtime.</span></span>

<span data-ttu-id="97d95-192">Un semplice `CpuPerfCountersConsumer.cpp` programma Mostra come usare i valori della `CpuPerfCounters` classe.</span><span class="sxs-lookup"><span data-stu-id="97d95-192">A simple `CpuPerfCountersConsumer.cpp` program shows how to use the values from the `CpuPerfCounters` class.</span></span>

### <a name="cpuperfcountersh"></a><span data-ttu-id="97d95-193">CpuPerfCounters. h</span><span class="sxs-lookup"><span data-stu-id="97d95-193">CpuPerfCounters.h</span></span>

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a><span data-ttu-id="97d95-194">CpuPerfCounters. cpp</span><span class="sxs-lookup"><span data-stu-id="97d95-194">CpuPerfCounters.cpp</span></span>

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a><span data-ttu-id="97d95-195">CpuPerfCountersConsumer. cpp</span><span class="sxs-lookup"><span data-stu-id="97d95-195">CpuPerfCountersConsumer.cpp</span></span>

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
