---
description: Il gruppo di test IFilter convalida i gestori dei filtri.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Test di gestori filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128563"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="b118c-103">Test di gestori filtro</span><span class="sxs-lookup"><span data-stu-id="b118c-103">Testing Filter Handlers</span></span>

<span data-ttu-id="b118c-104">Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) convalida i gestori dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b118c-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="b118c-105">Il gruppo di test esegue questa operazione: chiamando i metodi [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e controllando la conformità dei valori restituiti con la specifica dell'interfaccia **IFilter** ; e verificare che gli identificatori del blocco siano univoci e in aumento, che l'interfaccia **IFilter** si comportano in modo coerente dopo la reinizializzazione e che tutte le chiamate al metodo **IFilter** con parametri non validi restituiscono codici di errore previsti.</span><span class="sxs-lookup"><span data-stu-id="b118c-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="b118c-106">I programmi del gruppo di test effettuano inoltre il dump dell'output di un file filtrato da un gestore di filtri e controllano le informazioni di registrazione **IFilter** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b118c-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="b118c-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="b118c-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="b118c-108">Chiamata della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b118c-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="b118c-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="b118c-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="b118c-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="b118c-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="b118c-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="b118c-113">Procedura di test di IFilter</span><span class="sxs-lookup"><span data-stu-id="b118c-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="b118c-114">Test di convalida</span><span class="sxs-lookup"><span data-stu-id="b118c-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="b118c-115">Test di coerenza</span><span class="sxs-lookup"><span data-stu-id="b118c-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="b118c-116">Test di input non valido</span><span class="sxs-lookup"><span data-stu-id="b118c-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="b118c-117">Test di configurazioni IFilter diverse</span><span class="sxs-lookup"><span data-stu-id="b118c-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="b118c-118">Verifica dell'indicizzazione degli elementi registrati</span><span class="sxs-lookup"><span data-stu-id="b118c-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="b118c-119">File di log di esempio</span><span class="sxs-lookup"><span data-stu-id="b118c-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="b118c-120">File di dump di esempio</span><span class="sxs-lookup"><span data-stu-id="b118c-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="b118c-121">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="b118c-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="b118c-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b118c-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="b118c-123">Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="b118c-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="b118c-124">Non esiste alcun meccanismo per concatenare i filtri.</span><span class="sxs-lookup"><span data-stu-id="b118c-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="b118c-125">Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="b118c-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="b118c-126">Chiamata di Command-Line</span><span class="sxs-lookup"><span data-stu-id="b118c-126">Command-Line Invocation</span></span>

<span data-ttu-id="b118c-127">Il gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è costituito da tre applicazioni da riga di comando: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)e [filtreg.exe](#filtregexe) e da un file di inizializzazione, [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="b118c-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b118c-128">In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="b118c-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="b118c-129">I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b118c-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="b118c-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-130">ifilttst.exe</span></span>

<span data-ttu-id="b118c-131">Il programma ifilttst.exe esegue diversi test per convalidare un gestore di filtro.</span><span class="sxs-lookup"><span data-stu-id="b118c-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="b118c-132">Nell'esempio seguente viene illustrato come richiamare il programma ifilttst.exe dalla riga di comando:</span><span class="sxs-lookup"><span data-stu-id="b118c-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="b118c-133">Nell'esempio vengono eseguite le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="b118c-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="b118c-134">Indica al programma di filtrare il file test.htm</span><span class="sxs-lookup"><span data-stu-id="b118c-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="b118c-135">Reindirizza i messaggi di log a test.htm. log</span><span class="sxs-lookup"><span data-stu-id="b118c-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="b118c-136">Reindirizza i messaggi di dump a test.htm. dmp</span><span class="sxs-lookup"><span data-stu-id="b118c-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="b118c-137">Imposta il livello di dettaglio su 1</span><span class="sxs-lookup"><span data-stu-id="b118c-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="b118c-138">Per il corretto funzionamento del comando precedente, è necessario che i tre file si trovino nella directory di lavoro corrente: `test.htm` , [ifilttst.exe](#ifilttstexe)e [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="b118c-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="b118c-139">Nella tabella seguente sono elencate le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b118c-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b118c-140">Switch e possibili variabili</span><span class="sxs-lookup"><span data-stu-id="b118c-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="b118c-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b118c-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b118c-142"><strong>nome file/i</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="b118c-143">File o directory di input da filtrare.</span><span class="sxs-lookup"><span data-stu-id="b118c-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="b118c-144">Il nome del file può contenere i caratteri jolly <code>\*</code> e <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="b118c-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b118c-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="b118c-146">I messaggi di log vengono indirizzati a un file anziché allo schermo.</span><span class="sxs-lookup"><span data-stu-id="b118c-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="b118c-147">I messaggi di log descrivono i singoli test eseguiti e i risultati superati o non superati dei test.</span><span class="sxs-lookup"><span data-stu-id="b118c-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="b118c-148">Il nome del file di log corrisponde al nome del file di input ma con estensione. log.</span><span class="sxs-lookup"><span data-stu-id="b118c-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b118c-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="b118c-150">Il dump dei messaggi viene indirizzato a un file anziché allo schermo.</span><span class="sxs-lookup"><span data-stu-id="b118c-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="b118c-151">I messaggi dump descrivono il contenuto dei blocchi.</span><span class="sxs-lookup"><span data-stu-id="b118c-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="b118c-152">Il dump della struttura del blocco viene eseguito quando il livello di dettaglio è 3.</span><span class="sxs-lookup"><span data-stu-id="b118c-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="b118c-153">Il nome del file di dump corrisponde al nome del file di input ma con estensione dmp.</span><span class="sxs-lookup"><span data-stu-id="b118c-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b118c-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="b118c-155">Disabilitare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="b118c-155">Disable logging.</span></span> <span data-ttu-id="b118c-156">Questo flag sostituisce l' <code>/l</code> opzione.</span><span class="sxs-lookup"><span data-stu-id="b118c-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b118c-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="b118c-158">Disabilitare il dump.</span><span class="sxs-lookup"><span data-stu-id="b118c-158">Disable dumping.</span></span> <span data-ttu-id="b118c-159">Questo flag sostituisce l' <code>/d</code> opzione.</span><span class="sxs-lookup"><span data-stu-id="b118c-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b118c-160"><strong>/v Integer</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="b118c-161">Livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b118c-161">The verbosity level.</span></span> <span data-ttu-id="b118c-162">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="b118c-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="b118c-163">0: il test registra solo i messaggi relativi a errori di interfaccia <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> specifici.</span><span class="sxs-lookup"><span data-stu-id="b118c-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="b118c-164">Il test eseguirà il dump del contenuto del blocco.</span><span class="sxs-lookup"><span data-stu-id="b118c-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="b118c-165">1-il test registra i messaggi di avviso e quelli per il livello 0.</span><span class="sxs-lookup"><span data-stu-id="b118c-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="b118c-166">2: il test registra i messaggi relativi ai test superati, oltre a quelli per il livello 1.</span><span class="sxs-lookup"><span data-stu-id="b118c-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="b118c-167">3: il test registra i messaggi informativi e quelli per il livello 2.</span><span class="sxs-lookup"><span data-stu-id="b118c-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="b118c-168">Inoltre, il test eseguirà il dump della struttura del blocco.</span><span class="sxs-lookup"><span data-stu-id="b118c-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b118c-169"><strong>/t Integer</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="b118c-170">Numero di thread da avviare.</span><span class="sxs-lookup"><span data-stu-id="b118c-170">The number of threads to launch.</span></span> <span data-ttu-id="b118c-171">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="b118c-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b118c-172"><strong>/r Integer</strong>]</span><span class="sxs-lookup"><span data-stu-id="b118c-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="b118c-173">Filtra in modo ricorsivo le sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="b118c-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="b118c-174">Il parametro integer facoltativo specifica la profondità a cui esercitare la ricorsione.</span><span class="sxs-lookup"><span data-stu-id="b118c-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="b118c-175">Se non viene specificato alcun Integer o se il valore integer è 0, viene utilizzata la ricorsione completa.</span><span class="sxs-lookup"><span data-stu-id="b118c-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="b118c-176">Per impostazione predefinita, la profondità di ricorsione è 1.</span><span class="sxs-lookup"><span data-stu-id="b118c-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b118c-177"><strong>/c Integer</strong></span><span class="sxs-lookup"><span data-stu-id="b118c-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="b118c-178">Il numero di volte in cui eseguire il ciclo.</span><span class="sxs-lookup"><span data-stu-id="b118c-178">The number of times to loop.</span></span> <span data-ttu-id="b118c-179">Se il valore integer è 0, il test viene eseguito in un ciclo infinito.</span><span class="sxs-lookup"><span data-stu-id="b118c-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="b118c-180">Per impostazione predefinita, i cicli di test sono una sola volta.</span><span class="sxs-lookup"><span data-stu-id="b118c-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="b118c-181">È necessario includere uno spazio tra l'opzione della riga di comando e il valore.</span><span class="sxs-lookup"><span data-stu-id="b118c-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="b118c-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-182">filtdump.exe</span></span>

<span data-ttu-id="b118c-183">Il programma filtdump.exe carica un gestore di filtro per un documento specificato e stampa l'output generato dalla dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="b118c-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="b118c-184">Nell'esempio seguente viene illustrato come richiamare il programma filtdump.exe.</span><span class="sxs-lookup"><span data-stu-id="b118c-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="b118c-185">Filtdump.exe usa il metodo [ILoadFilter:: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) per caricare la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) appropriata per l'estensione del nome file specificata e stampa i risultati.</span><span class="sxs-lookup"><span data-stu-id="b118c-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="b118c-186">Il comando seguente, ad esempio, indica filtdump.exe di caricare il gestore di filtri smpfilt.dll per l'estensione SMP, estrarre tutto il testo e le proprietà dal file MyFile. SMP e stampare i risultati.</span><span class="sxs-lookup"><span data-stu-id="b118c-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="b118c-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="b118c-187">filtreg.exe</span></span>

<span data-ttu-id="b118c-188">Il programma filtreg.exe controlla le informazioni di installazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b118c-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="b118c-189">Per richiamare il programma filtreg.exe dalla riga di comando, digitarne il nome, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="b118c-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="b118c-190">Filtreg.exe enumera tutte le estensioni di file a cui sono associati gestori di filtro stampando l'estensione del nome file e il nome della dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b118c-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="b118c-191">Si tratta di un modo semplice per verificare l'installazione corretta di un **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="b118c-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="b118c-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="b118c-192">ifilttst.ini</span></span>

<span data-ttu-id="b118c-193">Un'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) viene inizializzata chiamando il metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="b118c-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="b118c-194">Il metodo **IFilter:: init** accetta i quattro parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b118c-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="b118c-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="b118c-195">*grfFlags*</span></span>
2. <span data-ttu-id="b118c-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="b118c-196">*cAttributes*</span></span>
3. <span data-ttu-id="b118c-197">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="b118c-197">*aAttributes*</span></span>
4. <span data-ttu-id="b118c-198">*pdwFlags*</span><span class="sxs-lookup"><span data-stu-id="b118c-198">*pdwFlags*</span></span>

<span data-ttu-id="b118c-199">L'utente del programma ifilttst.exe del gruppo di test [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) può specificare i valori per questi parametri in un file denominato ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="b118c-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="b118c-200">Nella tabella seguente vengono descritte le voci del file ifilttst.ini che specificano i primi tre parametri, ovvero i parametri di input.</span><span class="sxs-lookup"><span data-stu-id="b118c-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="b118c-201">Per un file di esempio, vedere [esempio di file di ifilttst.ini](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="b118c-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="b118c-202">Non è presente alcuna voce di tabella per il parametro *pdwFlags* perché è un parametro di output. non deve avere alcun valore speciale prima della chiamata al metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="b118c-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="b118c-203">Voce</span><span class="sxs-lookup"><span data-stu-id="b118c-203">Entry</span></span>         | <span data-ttu-id="b118c-204">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b118c-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b118c-205">Flags</span><span class="sxs-lookup"><span data-stu-id="b118c-205">Flags</span></span>         | <span data-ttu-id="b118c-206">Nomi dei flag di [**\_ inizializzazione IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) che devono essere Uniti dall'operatore OR per formare il parametro *grfFlags* del metodo [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="b118c-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="b118c-207">I nomi dei flag devono essere tutti in maiuscolo e sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="b118c-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b118c-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="b118c-208">*cAttributes*</span></span> | <span data-ttu-id="b118c-209">Intero decimale che rappresenta il valore del parametro *CAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b118c-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b118c-210">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="b118c-210">*aAttributes*</span></span> | <span data-ttu-id="b118c-211">Questa voce deve iniziare con *aAttributes* e deve essere diversa dalle altre voci *aAttributes* nella sezione.</span><span class="sxs-lookup"><span data-stu-id="b118c-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="b118c-212">I nomi validi per la voce *aAttributes* sono: *aAttributes*, *aAttributes1*, *aAttributes2* e così via.</span><span class="sxs-lookup"><span data-stu-id="b118c-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="b118c-213">Il primo token deve essere un GUID.</span><span class="sxs-lookup"><span data-stu-id="b118c-213">The first token must be a GUID.</span></span> <span data-ttu-id="b118c-214">Il GUID deve essere formattato esattamente come illustrato nella `[Test3]` sezione del [File di ifilttst.ini di esempio](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="b118c-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="b118c-215">Il secondo token può essere un identificatore di proprietà (PID) costituito da un numero in notazione esadecimale o un puntatore a una stringa di caratteri wide (LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="b118c-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="b118c-216">È possibile specificare LPWSTR racchiudendo la stringa tra virgolette doppie, come illustrato nella `[Test6]` sezione del file di ifilttst.ini di esempio.</span><span class="sxs-lookup"><span data-stu-id="b118c-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="b118c-217">Se non si specificano le voci Flags e *CAttributes* , il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="b118c-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="b118c-218">Se si imposta *CAttributes* uguale a 2, è necessario specificare due nomi *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b118c-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="b118c-219">Nella `[Test5]` sezione dell'esempio *CAttributes* è 1, ma non è stato specificato alcun *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b118c-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="b118c-220">Il test chiama quindi il metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *CAttributes* uguale a 1 e *aAttributes* uguale a **null**.</span><span class="sxs-lookup"><span data-stu-id="b118c-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="b118c-221">Si tratta di un test case utile perché è probabile che si verifichi una violazione di accesso nel metodo **IFilter:: init** .</span><span class="sxs-lookup"><span data-stu-id="b118c-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="b118c-222">Se ifilttst.exe non riesce a trovare un file denominato ifilttst.ini nella directory di lavoro, viene usata una configurazione predefinita per inizializzare l'oggetto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="b118c-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="b118c-223">Nell'esempio seguente viene illustrata la configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b118c-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="b118c-224">File ifilttst.ini di esempio</span><span class="sxs-lookup"><span data-stu-id="b118c-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="b118c-225">Il file di ifilttst.ini è organizzato in sezioni, con il nome della sezione racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="b118c-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="b118c-226">Nell'esempio, le sezioni sono denominate `[Test1]` , `[Test2]` e così via.</span><span class="sxs-lookup"><span data-stu-id="b118c-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="b118c-227">Tutti i nomi di sezione devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="b118c-227">All section names must be unique.</span></span> <span data-ttu-id="b118c-228">Il test legge i valori dalla prima sezione e Inizializza l' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con tali valori.</span><span class="sxs-lookup"><span data-stu-id="b118c-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="b118c-229">Quindi, tutti i test vengono eseguiti utilizzando questa configurazione **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="b118c-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="b118c-230">Quindi, l' **IFilter** viene rilasciato e reinizializzato, usando i parametri elencati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b118c-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="b118c-231">Il processo viene ripetuto fino a quando non vengono testate tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="b118c-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="b118c-232">Procedura di test di IFilter</span><span class="sxs-lookup"><span data-stu-id="b118c-232">IFilter Test Procedure</span></span>

<span data-ttu-id="b118c-233">Dopo l'inizializzazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , il programma ifilttst.exe esegue una serie di test sull' **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="b118c-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="b118c-234">Oltre a seguire le procedure di test di **IFilter** , assicurarsi che l'implementazione di **IFilter** usi procedure di codice sicure.</span><span class="sxs-lookup"><span data-stu-id="b118c-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="b118c-235">Vedere "procedure di sicurezza del codice per la ricerca di Windows" nell' [implementazione di gestori di filtri in Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b118c-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="b118c-236">Test di convalida</span><span class="sxs-lookup"><span data-stu-id="b118c-236">Validation Test</span></span>

<span data-ttu-id="b118c-237">Il test di convalida passa l'oggetto un blocco alla volta, verificando ogni singolo blocco e tutti i codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b118c-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="b118c-238">Il test di convalida Salva tutte le strutture di [**\_ blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk) restituite in un elenco.</span><span class="sxs-lookup"><span data-stu-id="b118c-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="b118c-239">Il test di convalida verifica le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b118c-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="b118c-240">[**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* gli ID blocco idChunk devono essere univoci e incrementali.</span><span class="sxs-lookup"><span data-stu-id="b118c-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="b118c-241">[**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*il parametro flags* è uno stato di blocco riconosciuto, ad esempio [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), chunk \_ text o CenabledHUNK \_ value costanti.</span><span class="sxs-lookup"><span data-stu-id="b118c-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="b118c-242">[**\_ Blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* il parametro breakType è un tipo di break riconosciuto (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="b118c-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="b118c-243">Se gli attributi di inizializzazione [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) specificano che **IFilter** deve restituire solo blocchi contenenti proprietà del tipo di valore interno, *idChunkSource* deve essere uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="b118c-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="b118c-244">Se il blocco non è derivato, ovvero se non è una proprietà del tipo di valore interna, il blocco [**Stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* deve essere uguale a **\_ blocco stat**.*idChunk*.</span><span class="sxs-lookup"><span data-stu-id="b118c-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="b118c-245">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce \_ OK o un altro valore restituito accettabile, ad esempio il filtro \_ e la \_ fine \_ dei \_ blocchi, il \_ collegamento filtro e non \_ \_ disponibile e così via.</span><span class="sxs-lookup"><span data-stu-id="b118c-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="b118c-246">Se il blocco contiene testo, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce \_ OK, \_ Last Text del \_ filtro \_ o filtro \_ E non è \_ \_ più \_ testo.</span><span class="sxs-lookup"><span data-stu-id="b118c-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="b118c-247">Se [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce \_ il filtro S \_ Last \_ text, la chiamata successiva a **IFILTER:: GetText** restituisce Filter \_ E \_ non \_ più \_ testo.</span><span class="sxs-lookup"><span data-stu-id="b118c-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="b118c-248">Se il blocco contiene un valore, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce S \_ OK o Filter \_ E \_ non \_ più \_ valori.</span><span class="sxs-lookup"><span data-stu-id="b118c-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="b118c-249">Test di coerenza</span><span class="sxs-lookup"><span data-stu-id="b118c-249">Consistency Test</span></span>

<span data-ttu-id="b118c-250">Il programma di ifilttxt.exe Reinizializza nuovamente l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri del test di convalida ed esegue un test di coerenza.</span><span class="sxs-lookup"><span data-stu-id="b118c-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="b118c-251">Se l'implementazione di **IFilter** è stata inizializzata con il flag IFilter [**\_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ indicizzazione \_ solo, il test rilascia l'interfaccia **IFilter** e la associa nuovamente prima di effettuare un'altra chiamata al metodo [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="b118c-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="b118c-252">Il test di coerenza verifica le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b118c-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="b118c-253">Ogni struttura del [**\_ blocco stat**](/windows/win32/api/filter/ns-filter-stat_chunk) restituita dal metodo [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) è identica al **\_ blocco stat** corrispondente restituito nel test di convalida.</span><span class="sxs-lookup"><span data-stu-id="b118c-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="b118c-254">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce \_ OK o un altro valore restituito accettabile, ad esempio il filtro \_ e la \_ fine \_ dei \_ blocchi, il \_ collegamento filtro e non \_ \_ disponibile e così via.</span><span class="sxs-lookup"><span data-stu-id="b118c-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="b118c-255">Test di input non valido</span><span class="sxs-lookup"><span data-stu-id="b118c-255">Invalid Input Test</span></span>

<span data-ttu-id="b118c-256">Il programma di ifilttst.exe Reinizializza nuovamente l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con gli stessi parametri ed esegue un test di input non valido.</span><span class="sxs-lookup"><span data-stu-id="b118c-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="b118c-257">Questo test esegue il documento un blocco alla volta, facendo in modo non corretto le chiamate di funzione, ad esempio chiamando il metodo [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) quando il mandrino corrente contiene testo.</span><span class="sxs-lookup"><span data-stu-id="b118c-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="b118c-258">Il test controlla tutti i codici restituiti per la conformità con la specifica **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="b118c-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="b118c-259">Il test di input non valido verifica le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b118c-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="b118c-260">Se il blocco corrente contiene testo, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce il filtro \_ e \_ nessun \_ valore e una chiamata a [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b118c-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="b118c-261">Se il blocco corrente contiene un valore, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) restituisce Filter \_ e \_ nessun \_ testo e una chiamata a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b118c-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="b118c-262">Se la chiamata precedente a [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ha restituito Filter \_ e \_ nessun \_ altro \_ testo, le chiamate successive a **IFILTER:: GetText** restituiscono Filter \_ e \_ non \_ più \_ testo.</span><span class="sxs-lookup"><span data-stu-id="b118c-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="b118c-263">Se la chiamata precedente a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ha restituito \_ un filtro e \_ non \_ più \_ valori, le chiamate successive a **IFILTER:: GetValue** restituiscono il filtro \_ e \_ non \_ più \_ valori.</span><span class="sxs-lookup"><span data-stu-id="b118c-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="b118c-264">Se la chiamata precedente a [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito il filtro \_ e \_ \_ la fine dei \_ blocchi, le chiamate successive a **IFilter:: GetChunk** restituiscono il filtro \_ e \_ \_ la fine dei \_ blocchi.</span><span class="sxs-lookup"><span data-stu-id="b118c-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="b118c-265">Il test di input non valido Confronta le strutture dei blocchi correnti con quelle restituite nel test di convalida per assicurarsi che siano identiche.</span><span class="sxs-lookup"><span data-stu-id="b118c-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="b118c-266">Test di configurazioni IFilter diverse</span><span class="sxs-lookup"><span data-stu-id="b118c-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="b118c-267">Il programma ifilttst.exe rilascia l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e la riassociazione, questa volta inizializzarla con il set di parametri successivo.</span><span class="sxs-lookup"><span data-stu-id="b118c-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="b118c-268">Il test ripete il ciclo: test di convalida, test di coerenza e test di input non valido, fino a quando non sono state testate tutte le configurazioni **IFilter** desiderate specificate in [ifilttst.ini](#ifilttstini) file.</span><span class="sxs-lookup"><span data-stu-id="b118c-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="b118c-269">Verifica dell'indicizzazione degli elementi registrati</span><span class="sxs-lookup"><span data-stu-id="b118c-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="b118c-270">Il test finale dell' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantisce che **IFilter** sia registrato correttamente e che venga richiamato per indicizzare gli elementi registrati per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="b118c-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="b118c-271">È possibile utilizzare Gestione catalogo per avviare la reindicizzazione o utilizzare il gestore dell'ambito di ricerca per indicizzazione (CSM) per configurare le regole predefinite che indicano gli URL di cui si desidera eseguire la ricerca nell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="b118c-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="b118c-272">Al termine dell'indicizzazione, utilizzare l'interfaccia utente di ricerca di Windows per cercare una stringa nel contenuto o nelle proprietà degli elementi.</span><span class="sxs-lookup"><span data-stu-id="b118c-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="b118c-273">Se gli elementi sono stati indicizzati, verranno visualizzati nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="b118c-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="b118c-274">Per ulteriori informazioni sulla reindicizzazione, vedere [utilizzo di gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) e [utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="b118c-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="b118c-275">L'esempio di codice ReindexMatchingUrls illustra i modi per specificare i file da indicizzare e il modo in cui.</span><span class="sxs-lookup"><span data-stu-id="b118c-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="b118c-276">Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM).</span><span class="sxs-lookup"><span data-stu-id="b118c-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="b118c-277">Entrambi gli esempi di codice sono disponibili in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="b118c-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="b118c-278">File di log di esempio</span><span class="sxs-lookup"><span data-stu-id="b118c-278">Sample Log File</span></span>

<span data-ttu-id="b118c-279">Al momento della richiesta, il programma Ifilttst.exe può produrre un log contenente una descrizione dei passaggi necessari durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b118c-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="b118c-280">Gli esempi seguenti sono estratti da un file di log, con il livello di dettaglio impostato sul valore massimo possibile 3.</span><span class="sxs-lookup"><span data-stu-id="b118c-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="b118c-281">La prima riga è un messaggio informativo, che indica che una nuova configurazione è stata caricata dal file di ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="b118c-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="b118c-282">Riga (3) indica il nome della sezione nel file di ifilttst.ini da cui è stata letta la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="b118c-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="b118c-283">Righe (4) fino a (7) elenca i parametri per [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span><span class="sxs-lookup"><span data-stu-id="b118c-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="b118c-284">Le righe che iniziano con `INFO` sono messaggi informativi sull'associazione dell' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e sull'inizio del test di convalida.</span><span class="sxs-lookup"><span data-stu-id="b118c-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="b118c-285">Le righe che iniziano con `PASS` sono messaggi relativi a test specifici che sono stati superati.</span><span class="sxs-lookup"><span data-stu-id="b118c-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="b118c-286">La riga nell'esempio di log seguente è un avviso.</span><span class="sxs-lookup"><span data-stu-id="b118c-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="b118c-287">Gli avvisi chiamano l'attenzione sul comportamento di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) problematico, anche se valido.</span><span class="sxs-lookup"><span data-stu-id="b118c-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="b118c-288">Questo avviso indica che il metodo [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha restituito un blocco di testo che non contiene testo.</span><span class="sxs-lookup"><span data-stu-id="b118c-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="b118c-289">Il messaggio di errore di esempio seguente indica che [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha emesso un blocco non richiesto.</span><span class="sxs-lookup"><span data-stu-id="b118c-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="b118c-290">Nel caso di questo messaggio di errore di esempio, l' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ha emesso un blocco con un PID di `0x5` .</span><span class="sxs-lookup"><span data-stu-id="b118c-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="b118c-291">L'ispezione della sezione `[Test1]` in ifilttst.ini indicherà che **IFilter** è stato configurato in modo da non generare blocchi con questo PID.</span><span class="sxs-lookup"><span data-stu-id="b118c-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="b118c-292">Se, ad esempio, non \_ si applicano gli attributi di indice di IFilter init \_ \_ \_ o IFilter \_ init, gli \_ \_ altri \_ attributi sono stati specificati nella voce dei flag e se *CAttributes* è 0, **IFilter** genera solo i blocchi con un PID di `0x13` e corrispondente al \_ \_ contenuto del valore del PID.</span><span class="sxs-lookup"><span data-stu-id="b118c-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="b118c-293">File di dump di esempio</span><span class="sxs-lookup"><span data-stu-id="b118c-293">Sample Dump File</span></span>

<span data-ttu-id="b118c-294">Al momento della richiesta, il programma Ifilttst.exe può produrre un dump contenente i blocchi trovati e il relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="b118c-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="b118c-295">L'esempio seguente è un Estratto di un file dump di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="b118c-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="b118c-296">Le prime nove righe descrivono la struttura del blocco corrente.</span><span class="sxs-lookup"><span data-stu-id="b118c-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="b118c-297">Il GUID e il PID corrispondono al contenuto dell'PSGUID di \_ archiviazione/PID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="b118c-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="b118c-298">Si tratta di un blocco contenente testo normale.</span><span class="sxs-lookup"><span data-stu-id="b118c-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="b118c-299">Il testo si trova nella struttura di blocco seguente:</span><span class="sxs-lookup"><span data-stu-id="b118c-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="b118c-300">Il blocco successivo, a partire dalla riga 11, ha un GUID diverso, corrispondente a `HTML IFilter` e un PID diverso, corrispondente a un href HTML.</span><span class="sxs-lookup"><span data-stu-id="b118c-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="b118c-301">Si tratta di una proprietà del tipo di valore interna, esportata da `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="b118c-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="b118c-302">Il blocco successivo, a partire dalla riga 21, ha lo stesso GUID e PID, ma lo stato del blocco è `VALUE` invece di `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="b118c-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="b118c-303">Si noti che il testo negli ultimi due blocchi è identico a quello del primo blocco.</span><span class="sxs-lookup"><span data-stu-id="b118c-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="b118c-304">Tuttavia, poiché [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è progettato per tre attributi (testo normale, html href come testo e html href come valore) da applicare a questa frase, i risultati vengono emessi in tre blocchi distinti.</span><span class="sxs-lookup"><span data-stu-id="b118c-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b118c-305">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="b118c-305">Additional Resources</span></span>

- <span data-ttu-id="b118c-306">Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="b118c-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="b118c-307">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b118c-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="b118c-308">Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="b118c-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="b118c-309">Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b118c-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b118c-310">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b118c-310">Related topics</span></span>

[<span data-ttu-id="b118c-311">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="b118c-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="b118c-312">Informazioni sui gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="b118c-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="b118c-313">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="b118c-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="b118c-314">Restituzione di proprietà da un gestore di filtro</span><span class="sxs-lookup"><span data-stu-id="b118c-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="b118c-315">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="b118c-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="b118c-316">Implementazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="b118c-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="b118c-317">Registrazione di gestori di filtro</span><span class="sxs-lookup"><span data-stu-id="b118c-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
