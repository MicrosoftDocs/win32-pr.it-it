---
description: Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedure consigliate per i gestori di filtro in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525537"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="a6397-103">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6397-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="a6397-104">Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.</span><span class="sxs-lookup"><span data-stu-id="a6397-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="a6397-105">È possibile estendere la ricerca di Windows per indicizzare i tipi di file nuovi o proprietari scrivendo i gestori di filtro per estrarre il contenuto e i gestori delle proprietà per estrarre le proprietà dei file.</span><span class="sxs-lookup"><span data-stu-id="a6397-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="a6397-106">I filtri sono associati ai tipi di file, come indicato dalle estensioni dei nomi di file, dai tipi MIME o dagli identificatori di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="a6397-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="a6397-107">Mentre un filtro può gestire più tipi di file, ogni tipo funziona con un solo filtro.</span><span class="sxs-lookup"><span data-stu-id="a6397-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="a6397-108">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6397-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a6397-109">Codice nativo</span><span class="sxs-lookup"><span data-stu-id="a6397-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="a6397-110">Procedure di sicurezza del codice per Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6397-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="a6397-111">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a6397-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a6397-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6397-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="a6397-113">Codice nativo</span><span class="sxs-lookup"><span data-stu-id="a6397-113">Native Code</span></span>

<span data-ttu-id="a6397-114">In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="a6397-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="a6397-115">I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo di esecuzione di più componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="a6397-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="a6397-116">Procedure di sicurezza del codice per Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6397-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="a6397-117">Di seguito sono riportate le procedure per la scrittura di applicazioni sicure per l'utilizzo con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="a6397-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="a6397-118">**Per le applicazioni di query:**</span><span class="sxs-lookup"><span data-stu-id="a6397-118">**For query applications:**</span></span>

-   <span data-ttu-id="a6397-119">Quando si scrivono i client di ricerca, è necessario scegliere l'API che viene eseguita in un contesto di sicurezza che consente all'utente il privilegio minimo.</span><span class="sxs-lookup"><span data-stu-id="a6397-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="a6397-120">Ad esempio, le pagine ASP possono usare l'oggetto query IXSSO, che viene eseguito come processo utente.</span><span class="sxs-lookup"><span data-stu-id="a6397-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="a6397-121">**Per IFilters e risorse della lingua:**</span><span class="sxs-lookup"><span data-stu-id="a6397-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="a6397-122">Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="a6397-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="a6397-123">Non esiste alcun meccanismo per concatenare i filtri.</span><span class="sxs-lookup"><span data-stu-id="a6397-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="a6397-124">Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="a6397-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="a6397-125">Gli IFilter, i Word breaker e gli stemmer per la ricerca di Windows vengono eseguiti nel contesto di sicurezza locale.</span><span class="sxs-lookup"><span data-stu-id="a6397-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="a6397-126">Devono essere scritti per gestire i buffer e per eseguire lo stack in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="a6397-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="a6397-127">Tutte le copie di stringhe devono avere controlli espliciti per evitare sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6397-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="a6397-128">Verificare sempre la dimensione allocata del buffer e verificare le dimensioni dei dati rispetto alle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6397-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="a6397-129">I sovraccarichi del buffer sono una tecnica comune per sfruttare il codice che non impone restrizioni per le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6397-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="a6397-130">I componenti [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), Word breaker e stemmer non devono mai chiamare la funzione [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o un'API simile che termina un processo e tutti i relativi thread.</span><span class="sxs-lookup"><span data-stu-id="a6397-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="a6397-131">Non allocare o liberare risorse nel punto di ingresso DllMain.</span><span class="sxs-lookup"><span data-stu-id="a6397-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="a6397-132">Questo può causare errori durante i test di stress con risorse insufficienti.</span><span class="sxs-lookup"><span data-stu-id="a6397-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="a6397-133">Codificare tutti gli oggetti in modo che siano thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a6397-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="a6397-134">Windows Search chiama una qualsiasi istanza di un Word breaker o uno stemmer in un thread alla volta, ma può chiamare più istanze contemporaneamente tra più thread.</span><span class="sxs-lookup"><span data-stu-id="a6397-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="a6397-135">Evitare di creare file temporanei o scrivere nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a6397-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="a6397-136">Se si usa il compilatore Microsoft Visual C++, assicurarsi di compilare l'applicazione con l'opzione **/GS** .</span><span class="sxs-lookup"><span data-stu-id="a6397-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="a6397-137">L'opzione **/GS** viene usata per rilevare i sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6397-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="a6397-138">L'opzione/GS inserisce i controlli di sicurezza nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="a6397-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="a6397-139">Per ulteriori informazioni, vedere [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (buffer Security Check) nella sezione Visual C++ opzioni del compilatore di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="a6397-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6397-140">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a6397-140">Additional Resources</span></span>

-   <span data-ttu-id="a6397-141">Nell'esempio [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a6397-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="a6397-142">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6397-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="a6397-143">Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a6397-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="a6397-144">Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6397-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6397-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6397-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6397-146">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="a6397-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="a6397-147">Informazioni sui gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6397-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="a6397-148">Restituzione di proprietà da un gestore di filtro</span><span class="sxs-lookup"><span data-stu-id="a6397-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="a6397-149">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="a6397-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="a6397-150">Implementazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6397-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="a6397-151">Registrazione di gestori di filtro</span><span class="sxs-lookup"><span data-stu-id="a6397-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="a6397-152">Test di gestori filtro</span><span class="sxs-lookup"><span data-stu-id="a6397-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
