---
title: Strumento compilatore servizio Web
description: Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio. Genera il file proxy C per il lato client e il file stub C per il lato del servizio, in base alle esigenze.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Servizi Web per lo strumento di compilazione del servizio Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399961"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="19dea-107">Strumento compilatore servizio Web</span><span class="sxs-lookup"><span data-stu-id="19dea-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="19dea-108">Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="19dea-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="19dea-109">Genera il file proxy C per il lato client e il file stub C per il lato del servizio, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="19dea-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="19dea-110">Per supportare la [serializzazione](serialization.md), il compilatore genera intestazioni per le descrizioni di elementi per le definizioni di elementi globali e tutte le informazioni sulla definizione del tipo nel file proxy che devono essere utilizzate dal motore di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="19dea-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="19dea-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="19dea-111">Usage</span></span>

<span data-ttu-id="19dea-112">**WsUtil.exe \[ Opzioni switch della riga di comando \[ \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="19dea-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="19dea-113">opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="19dea-113">command-line-switches</span></span>

<span data-ttu-id="19dea-114">Specifica WsUtil.exe opzioni del compilatore.</span><span class="sxs-lookup"><span data-stu-id="19dea-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="19dea-115">Le opzioni possono essere visualizzate in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="19dea-115">Switches can appear in any order.</span></span> <span data-ttu-id="19dea-116">Il trattino ('-') e la barra ('/') vengono considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="19dea-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="19dea-117">Elenco di opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="19dea-117">List of command line options</span></span>

-   <span data-ttu-id="19dea-118">@filename Specifica che il file di input deve essere trattato come un file di risposta.</span><span class="sxs-lookup"><span data-stu-id="19dea-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="19dea-119">Questa opzione può essere usata più volte, in qualsiasi posizione nell'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="19dea-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="19dea-120">/WSDL: <filename> : <\_ url facoltativo> specifica che il file di input deve essere trattato come un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="19dea-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="19dea-121">Sono consentiti più input WSDL e vengono elaborati tutti i file WSDL specificati.</span><span class="sxs-lookup"><span data-stu-id="19dea-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="19dea-122">L' \_ URL facoltativo specifica il percorso da cui vengono recuperati i metadati.</span><span class="sxs-lookup"><span data-stu-id="19dea-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="19dea-123">Se non \_ viene specificato alcun URL facoltativo, WSUTIL genera internamente un URL univoco.</span><span class="sxs-lookup"><span data-stu-id="19dea-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="19dea-124">Vedere anche [supporto dei criteri](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="19dea-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="19dea-125">/xsd: <filename> specifica che il nome file di input deve essere considerato come un file di schema.</span><span class="sxs-lookup"><span data-stu-id="19dea-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="19dea-126">Sono consentiti più input XSD e vengono elaborati tutti i file di schema specificati.</span><span class="sxs-lookup"><span data-stu-id="19dea-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="19dea-127">/wsp: <filename> : <\_ url facoltativo> specifica che il nome del file di input deve essere trattato come metadati del criterio.</span><span class="sxs-lookup"><span data-stu-id="19dea-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="19dea-128">Sono consentiti più input WSP e vengono elaborati tutti i file di criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="19dea-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="19dea-129">L' \_ URL facoltativo specifica il percorso da cui vengono recuperati i metadati.</span><span class="sxs-lookup"><span data-stu-id="19dea-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="19dea-130">Se non \_ viene specificato alcun URL facoltativo, WSUTIL genera internamente un URL univoco.</span><span class="sxs-lookup"><span data-stu-id="19dea-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="19dea-131">I file dei criteri vengono ignorati se viene specificato il flag/nopolicy.</span><span class="sxs-lookup"><span data-stu-id="19dea-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="19dea-132">Vedere anche [supporto dei criteri](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="19dea-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="19dea-133">/nopolicy Disabilita l'elaborazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="19dea-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="19dea-134">/out: <dirname> specifica il nome di directory per i file di output</span><span class="sxs-lookup"><span data-stu-id="19dea-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="19dea-135">/NoClient non generano lo stub lato client.</span><span class="sxs-lookup"><span data-stu-id="19dea-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="19dea-136">/noservice non genera lo stub del lato servizio.</span><span class="sxs-lookup"><span data-stu-id="19dea-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="19dea-137">/prefix: <string> anteporre la stringa specificata a tutti gli identificatori generati.</span><span class="sxs-lookup"><span data-stu-id="19dea-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="19dea-138">/FullName anteporre il nome file normalizzato agli identificatori generati.</span><span class="sxs-lookup"><span data-stu-id="19dea-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="19dea-139">Per impostazione predefinita, solo il nome specificato nell'attributo "Name" verrà usato per generare gli identificatori per le descrizioni correlate.</span><span class="sxs-lookup"><span data-stu-id="19dea-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="19dea-140">/String: <WS \_ string>\|<WCHAR \*> per impostazione predefinita, WSUTIL genera WCHAR \* per il tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="19dea-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="19dea-141">L'applicazione può utilizzare questo flag per sovrascrivere tale comportamento e genera \_ invece una stringa WS per xsd: Type.</span><span class="sxs-lookup"><span data-stu-id="19dea-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="19dea-142">/Help Visualizza il messaggio della Guida</span><span class="sxs-lookup"><span data-stu-id="19dea-142">/help Display help message</span></span>
-   <span data-ttu-id="19dea-143">/?</span><span class="sxs-lookup"><span data-stu-id="19dea-143">/?</span></span> <span data-ttu-id="19dea-144">Uguale a/Help</span><span class="sxs-lookup"><span data-stu-id="19dea-144">Same as /help</span></span>
-   <span data-ttu-id="19dea-145">/W: x opzioni di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="19dea-145">/W:x Error handling options.</span></span> <span data-ttu-id="19dea-146">Potrebbe essere W:0-W: 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="19dea-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="19dea-147">/nologo non generano informazioni specifiche del compilatore nell'output della console.</span><span class="sxs-lookup"><span data-stu-id="19dea-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="19dea-148">/nostamp non generano informazioni specifiche del compilatore sui file generati.</span><span class="sxs-lookup"><span data-stu-id="19dea-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="19dea-149">Per impostazione predefinita, il compilatore genera i file seguenti per il file WSDL o WSDL restituito dallo scambio di metadati:</span><span class="sxs-lookup"><span data-stu-id="19dea-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="19dea-150">Proxy client ({inputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="19dea-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="19dea-151">Stub servizio ({inputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="19dea-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="19dea-152">File di intestazione ({inputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="19dea-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="19dea-153">La radice del nome file generato è il nome del file di input.</span><span class="sxs-lookup"><span data-stu-id="19dea-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="19dea-154">Le estensioni di file di input originali vengono mantenute per impedire il conflitto di nomi di file per i file generati.</span><span class="sxs-lookup"><span data-stu-id="19dea-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="19dea-155">Per impostazione predefinita, gli stub client e servizio vengono generati nello stesso file, con codice stub servizio generato dopo il codice proxy.</span><span class="sxs-lookup"><span data-stu-id="19dea-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="19dea-156">Per impostazione predefinita, il compilatore genera i seguenti file per un file XSD per lo schema restituito dallo scambio di metadati:</span><span class="sxs-lookup"><span data-stu-id="19dea-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="19dea-157">descrizioni della serializzazione ({inputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="19dea-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="19dea-158">File di intestazione ({inputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="19dea-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="19dea-159">La radice del nome file è il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="19dea-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="19dea-160">Wsutil.exe genera una sezione "timbro" all'inizio di tutti i file generati, che indica l'opzione del compilatore, la versione dello strumento, l'opzione della riga di comando applicabile e così via. Questa sezione può essere disattivata utilizzando l'opzione/nostamp per evitare rumore con il confronto dei file generati.</span><span class="sxs-lookup"><span data-stu-id="19dea-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="19dea-161">Wsutil non supporta il download dei metadati</span><span class="sxs-lookup"><span data-stu-id="19dea-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="19dea-162">Il compilatore WSUTIL funziona solo dal file di metadati locale.</span><span class="sxs-lookup"><span data-stu-id="19dea-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="19dea-163">Lo strumento non supporta il download dei metadati dall'esecuzione di servizi Web.</span><span class="sxs-lookup"><span data-stu-id="19dea-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="19dea-164">Gli sviluppatori possono utilizzare altri strumenti WebService supportati, ad esempio Svcutil, per scaricare i metadati nel computer locale, controllare i file salvati e passare i file a wsutil.exe per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="19dea-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="19dea-165">Supporto di più file di input/output</span><span class="sxs-lookup"><span data-stu-id="19dea-165">Multiple input/output file support</span></span>

<span data-ttu-id="19dea-166">WSDL e XML Schema consentono di includere/importare definizioni da altri spazi dei nomi specificati in altri percorsi o file.</span><span class="sxs-lookup"><span data-stu-id="19dea-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="19dea-167">Wsutil supporta più input schema/WSDL/Policy e genera un set di Stub/intestazione per ogni file di input.</span><span class="sxs-lookup"><span data-stu-id="19dea-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="19dea-168">Wsutil non segue le istruzioni include e Import.</span><span class="sxs-lookup"><span data-stu-id="19dea-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="19dea-169">Al contrario, l'applicazione deve passare i file contenenti tutti gli spazi dei nomi necessari a WSUTIL in modo che lo strumento possa risolvere tutte le dipendenze durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="19dea-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="19dea-170">**WsUtil.exe/xsd: stockquote. xsd/WSDL: stockquote. WSDL/WSDL: StockQuoteService. WSDL**</span><span class="sxs-lookup"><span data-stu-id="19dea-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="19dea-171">wsutil genera tre set di file di output:</span><span class="sxs-lookup"><span data-stu-id="19dea-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="19dea-172">stockquote. xsd. c stockquote. xsd. h</span><span class="sxs-lookup"><span data-stu-id="19dea-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="19dea-173">stockquote. WSDL. c stockquote. WSDL. h</span><span class="sxs-lookup"><span data-stu-id="19dea-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="19dea-174">StockQuoteService. WSDL. h stockquoteservices. WSDL. c</span><span class="sxs-lookup"><span data-stu-id="19dea-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="19dea-175">Tipi di file di output</span><span class="sxs-lookup"><span data-stu-id="19dea-175">Output file format</span></span>

<span data-ttu-id="19dea-176">Per ogni file di output, WSUTIL genera definizioni disponibili esternamente nel file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="19dea-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="19dea-177">A parte le definizioni della struttura C e i prototipi di funzioni stub, tutte le altre definizioni correlate ai servizi Web sono incapsulate in una struttura globale denominata con il nome file normalizzato.</span><span class="sxs-lookup"><span data-stu-id="19dea-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="19dea-178">Si noti che non tutti i campi vengono generati per la struttura globale.</span><span class="sxs-lookup"><span data-stu-id="19dea-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="19dea-179">Un campo di livello principale viene generato solo quando le definizioni correlate vengono specificate nel file di input.</span><span class="sxs-lookup"><span data-stu-id="19dea-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="19dea-180">Per i file XSD, ad esempio, non viene generato alcun campo relativo a messaggi, operazioni e contratti.</span><span class="sxs-lookup"><span data-stu-id="19dea-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="19dea-181">Livelli di avviso e livello di errore</span><span class="sxs-lookup"><span data-stu-id="19dea-181">Warning Levels and error level</span></span>

<span data-ttu-id="19dea-182">Analogamente al compilatore C, WsUtil.exe supporta quattro livelli di avviso e un livello di errore:</span><span class="sxs-lookup"><span data-stu-id="19dea-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="19dea-183">WsUtil.exe genera errori con errori irreversibili, ad esempio file WSDL non valido, opzioni del compilatore non valide e così via.</span><span class="sxs-lookup"><span data-stu-id="19dea-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="19dea-184">WsUtil genera avvisi W1 con gravi problemi reversibili.</span><span class="sxs-lookup"><span data-stu-id="19dea-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="19dea-185">Il compilatore può continuare, ma è necessario che l'utente sia a conoscenza del problema.</span><span class="sxs-lookup"><span data-stu-id="19dea-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="19dea-186">Ad esempio, verrà generato un avviso W1 se sono presenti attributi non supportati, come alcuni facet WSDL, in WSDL che non influisce sulla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="19dea-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="19dea-187">WsUtil genera avvisi W2 con problemi meno gravi.</span><span class="sxs-lookup"><span data-stu-id="19dea-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="19dea-188">Non vi è alcuna perdita di funzionalità, ma lo sviluppatore di applicazioni potrebbe volerne saperlo.</span><span class="sxs-lookup"><span data-stu-id="19dea-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="19dea-189">Comportamenti simili che potrebbero essere diversi dalle altre piattaforme.</span><span class="sxs-lookup"><span data-stu-id="19dea-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="19dea-190">WsUtil genera avvisi W3 con un minimo effetto sul codice generato.</span><span class="sxs-lookup"><span data-stu-id="19dea-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="19dea-191">wsutil.exe, ad esempio, genera un avviso W3 quando la stringa normalizzata è diversa dalla stringa originale.</span><span class="sxs-lookup"><span data-stu-id="19dea-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="19dea-192">W4 Warning è più simile a "Informational" Warnings e WsUtil Issue W4 in casi come ignorare l'attributo Documentation in WSDL.</span><span class="sxs-lookup"><span data-stu-id="19dea-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="19dea-193">WX indica che il compilatore considera l'avviso come errore.</span><span class="sxs-lookup"><span data-stu-id="19dea-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="19dea-194">Ad esempio, WSUTIL genera un errore per tutti gli avvisi W1 se/W: 1/WX è specificato.</span><span class="sxs-lookup"><span data-stu-id="19dea-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="19dea-195">/W: {N} specificare il livello di messaggio di avviso da generare.</span><span class="sxs-lookup"><span data-stu-id="19dea-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="19dea-196">/W: 1 indica che devono essere generati avvisi di livello 1, mentre gli avvisi di livello 2 e di avviso indicati di seguito devono essere mascherati e non generati dallo strumento.</span><span class="sxs-lookup"><span data-stu-id="19dea-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="19dea-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="19dea-197">/fullname</span></span>

<span data-ttu-id="19dea-198">Questa opzione indica che WsUtil.exe genera il nome completo per gli identificatori per evitare potenziali conflitti di nomi.</span><span class="sxs-lookup"><span data-stu-id="19dea-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="19dea-199">Ad esempio, in XSD sono disponibili:</span><span class="sxs-lookup"><span data-stu-id="19dea-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="19dea-200">Per impostazione predefinita WsUtil.exe genera:</span><span class="sxs-lookup"><span data-stu-id="19dea-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="19dea-201">Tuttavia, se viene specificata l'opzione della riga di comando/FullName, WsUtil.exe genera invece la definizione della struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="19dea-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="19dea-202">Globalizzazione</span><span class="sxs-lookup"><span data-stu-id="19dea-202">Globalization</span></span>

<span data-ttu-id="19dea-203">Lo strumento è indipendente dalla lingua e può essere localizzato in lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="19dea-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="19dea-204">È possibile localizzare tutti i messaggi di errore o l'output della console.</span><span class="sxs-lookup"><span data-stu-id="19dea-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="19dea-205">Tuttavia, le opzioni della riga di comando restano in inglese.</span><span class="sxs-lookup"><span data-stu-id="19dea-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="19dea-206">Variabile di ambiente</span><span class="sxs-lookup"><span data-stu-id="19dea-206">Environment Variable</span></span>

<span data-ttu-id="19dea-207">WsUtil.exe non utilizza alcuna variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="19dea-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="19dea-208">Indipendente dalla piattaforma</span><span class="sxs-lookup"><span data-stu-id="19dea-208">Platform independent</span></span>

<span data-ttu-id="19dea-209">I file di output di WsUtil.exe sono indipendenti dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="19dea-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="19dea-210">Nessun codice dipendente dall'architettura generato nello stub; qualsiasi architettura specifica verrà gestita dal compilatore C.</span><span class="sxs-lookup"><span data-stu-id="19dea-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="19dea-211">Lo stub può essere usato in tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="19dea-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="19dea-212">La descrizione dell'output wsutil.exe è disponibile nel [supporto WSDL](wsdl-support.md) e nella parte relativa al [supporto dello schema](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="19dea-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 




