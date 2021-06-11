---
description: Informazioni sulle procedure consigliate per la creazione di gestori di filtri in Windows Search. La ricerca usa i filtri per estrarre gli elementi da includere in un indice full-text.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedure consigliate per i gestori di filtri in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a864cb2651d6236a212f3bf356eed3380869284
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989306"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="5274d-104">Procedure consigliate per la creazione di gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5274d-104">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="5274d-105">Microsoft Windows Search i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.</span><span class="sxs-lookup"><span data-stu-id="5274d-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="5274d-106">È possibile estendere Windows Search per indicizzare i tipi di file nuovi o proprietari scrivendo gestori di filtri per estrarre il contenuto e gestori di proprietà per estrarre le proprietà dei file.</span><span class="sxs-lookup"><span data-stu-id="5274d-106">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="5274d-107">I filtri sono associati ai tipi di file, come denotato da estensioni di file, tipi MIME o identificatori di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="5274d-107">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="5274d-108">Mentre un filtro può gestire più tipi di file, ogni tipo funziona con un solo filtro.</span><span class="sxs-lookup"><span data-stu-id="5274d-108">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="5274d-109">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5274d-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5274d-110">Codice nativo</span><span class="sxs-lookup"><span data-stu-id="5274d-110">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="5274d-111">Procedure di sicurezza del codice per Windows Search</span><span class="sxs-lookup"><span data-stu-id="5274d-111">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="5274d-112">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="5274d-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5274d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5274d-113">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="5274d-114">Codice nativo</span><span class="sxs-lookup"><span data-stu-id="5274d-114">Native Code</span></span>

<span data-ttu-id="5274d-115">In Windows 7 e versioni successive i filtri scritti in codice gestito vengono bloccati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="5274d-115">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="5274d-116">I filtri DEVONO essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo in cui vengono eseguiti più componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5274d-116">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="5274d-117">Procedure di sicurezza del codice per Windows Search</span><span class="sxs-lookup"><span data-stu-id="5274d-117">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="5274d-118">Di seguito sono riportate le procedure per la scrittura di applicazioni sicure da usare con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="5274d-118">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="5274d-119">**Per le applicazioni di query:**</span><span class="sxs-lookup"><span data-stu-id="5274d-119">**For query applications:**</span></span>

-   <span data-ttu-id="5274d-120">Quando si scrivono client di ricerca, è consigliabile scegliere l'API che viene eseguita in un contesto di sicurezza che consenta all'utente il privilegio minimo.</span><span class="sxs-lookup"><span data-stu-id="5274d-120">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="5274d-121">Ad esempio, le pagine ASP possono usare l'oggetto query IXSSO, che viene eseguito come processo utente.</span><span class="sxs-lookup"><span data-stu-id="5274d-121">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="5274d-122">**Per IFilter e risorse della lingua:**</span><span class="sxs-lookup"><span data-stu-id="5274d-122">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="5274d-123">Se viene installato un nuovo gestore di filtri per un tipo di file in sostituzione di una registrazione di filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtri viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="5274d-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="5274d-124">Non esiste alcun meccanismo per concatenare i filtri.</span><span class="sxs-lookup"><span data-stu-id="5274d-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="5274d-125">Di conseguenza, il nuovo gestore di filtri è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="5274d-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="5274d-126">I filtri IFilter, word breaker e stemmer per Windows Search vengono eseguiti nel contesto di sicurezza locale.</span><span class="sxs-lookup"><span data-stu-id="5274d-126">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="5274d-127">Devono essere scritti per gestire i buffer e lo stack correttamente.</span><span class="sxs-lookup"><span data-stu-id="5274d-127">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="5274d-128">Tutte le copie di stringhe devono avere controlli espliciti per proteggersi dai sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="5274d-128">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="5274d-129">È consigliabile verificare sempre le dimensioni allocate del buffer e testare le dimensioni dei dati rispetto alle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="5274d-129">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="5274d-130">I sovraccarichi del buffer sono una tecnica comune per sfruttare il codice che non applica restrizioni relative alle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="5274d-130">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="5274d-131">[**I componenti IFilter,**](/windows/win32/api/filter/nn-filter-ifilter)word breaker e stemmer non devono mai chiamare la funzione [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o un'API simile che termina un processo e tutti i relativi thread.</span><span class="sxs-lookup"><span data-stu-id="5274d-131">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="5274d-132">Non allocare o liberare risorse nel punto di ingresso DllMain.</span><span class="sxs-lookup"><span data-stu-id="5274d-132">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="5274d-133">Ciò può causare errori durante i test di stress con risorse basse.</span><span class="sxs-lookup"><span data-stu-id="5274d-133">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="5274d-134">Codificare tutti gli oggetti in modo che siano thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5274d-134">Code all objects to be thread-safe.</span></span> <span data-ttu-id="5274d-135">Windows Search chiama qualsiasi istanza di un word breaker o stemmer in un thread alla volta, ma può chiamare più istanze contemporaneamente tra più thread.</span><span class="sxs-lookup"><span data-stu-id="5274d-135">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="5274d-136">Evitare di creare file temporanei o scrivere nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5274d-136">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="5274d-137">Se si usa il compilatore Microsoft Visual C++, assicurarsi di compilare l'applicazione usando **l'opzione /GS.**</span><span class="sxs-lookup"><span data-stu-id="5274d-137">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="5274d-138">**L'opzione /GS** viene usata per rilevare i sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="5274d-138">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="5274d-139">L'opzione /GS inserisce i controlli di sicurezza nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="5274d-139">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="5274d-140">Per altre informazioni, vedere [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / GS (Buffer Security Check)**(Funzione DllGetClassObject GS** (controllo di sicurezza del buffer) nella sezione Visual C++ Compiler Options (Opzioni del compilatore) di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5274d-140">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5274d-141">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="5274d-141">Additional Resources</span></span>

-   <span data-ttu-id="5274d-142">[L'esempio IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="5274d-142">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="5274d-143">Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5274d-143">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="5274d-144">Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="5274d-144">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="5274d-145">Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5274d-145">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5274d-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5274d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5274d-147">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="5274d-147">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="5274d-148">Informazioni sui gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5274d-148">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="5274d-149">Restituzione di proprietà da un gestore di filtri</span><span class="sxs-lookup"><span data-stu-id="5274d-149">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="5274d-150">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="5274d-150">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="5274d-151">Implementazione di gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5274d-151">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="5274d-152">Registrazione di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="5274d-152">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="5274d-153">Test dei gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="5274d-153">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
