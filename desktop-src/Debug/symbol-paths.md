---
description: La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione PDB e DBG). Il percorso di ricerca può essere costituito da uno o più elementi Path separati da punti e virgola.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Percorsi dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966046"
---
# <a name="symbol-paths"></a><span data-ttu-id="2a7e1-104">Percorsi dei simboli</span><span class="sxs-lookup"><span data-stu-id="2a7e1-104">Symbol Paths</span></span>

<span data-ttu-id="2a7e1-105">La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione PDB e DBG).</span><span class="sxs-lookup"><span data-stu-id="2a7e1-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="2a7e1-106">Il percorso di ricerca può essere costituito da uno o più elementi Path separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="2a7e1-107">Specifica dei percorsi di ricerca</span><span class="sxs-lookup"><span data-stu-id="2a7e1-107">Specifying Search Paths</span></span>

<span data-ttu-id="2a7e1-108">Per specificare la posizione in cui il gestore di simboli eseguirà la ricerca di file di simboli nelle directory del disco, chiamare la funzione [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="2a7e1-109">In alternativa, è possibile specificare un percorso di ricerca dei simboli nel parametro *UserSearchPath* della funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="2a7e1-110">Il parametro *UserSearchPath* in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e il parametro *SearchPath* in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) accettano un puntatore a una stringa con terminazione null che specifica un percorso o una serie di percorsi separati da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="2a7e1-111">Il gestore di simboli utilizza questi percorsi per la ricerca di file di simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="2a7e1-112">Se questo parametro è **null**, il gestore di simboli Cerca nella directory che contiene il modulo per il quale vengono cercati i simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="2a7e1-113">In caso contrario, se questo parametro viene specificato come valore non **null** , il gestore di simboli cerca innanzitutto nei percorsi impostati dall'applicazione prima di eseguire ricerche nella directory del modulo.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="2a7e1-114">Se si imposta il \_ \_ percorso del simbolo NT o la variabile di \_ \_ \_ ambiente NT ALT \_ Symbol \_ path, il gestore di simboli Cerca i file di simboli nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="2a7e1-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="2a7e1-115">\_Variabile di \_ ambiente del percorso dei simboli NT \_ .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="2a7e1-116">\_Variabile di \_ ambiente del percorso dei simboli Alt NT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="2a7e1-117">Directory che contiene il modulo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="2a7e1-118">Per recuperare i percorsi di ricerca, chiamare la funzione [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="2a7e1-119">Il percorso di ricerca per i file di database di programma (con estensione pdb) è diverso dal percorso dei file di debug (con estensione dbg).</span><span class="sxs-lookup"><span data-stu-id="2a7e1-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="2a7e1-120">L'algoritmo è determinato dalla funzionalità della libreria dei simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="2a7e1-121">Per impostazione predefinita, Microsoft Visual C/C++ Crea simboli di formato Microsoft, li rimuove dall'immagine e li inserisce in un file con estensione PDB separato.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="2a7e1-122">Il file con estensione PDB, in genere, si trova nella directory che contiene l'immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="2a7e1-123">Visual C/C++ incorpora il percorso assoluto del file con estensione pdb nell'immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="2a7e1-124">Se il gestore di simboli non riesce a trovare il file con estensione PDB in tale percorso o se il file con estensione PDB è stato spostato in un'altra directory, il gestore dei simboli individuerà il file con estensione PDB utilizzando il percorso di ricerca descritto per i file con estensione dbg.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="2a7e1-125">Tipi di elemento Path</span><span class="sxs-lookup"><span data-stu-id="2a7e1-125">Path Element Types</span></span>

<span data-ttu-id="2a7e1-126">Sono disponibili tre tipi di elementi Path.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="2a7e1-127">Elemento Path standard</span><span class="sxs-lookup"><span data-stu-id="2a7e1-127">Standard Path Element</span></span>

<span data-ttu-id="2a7e1-128">Viene eseguita la ricerca di un elemento Path standard cercando nella radice della directory specificata dall'elemento Path.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="2a7e1-129">Il gestore di simboli Cerca anche in una sottodirectory di "symbols" che corrisponde all'estensione di file del modulo che vengono cercati i simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="2a7e1-130">Si tratta in genere di "dll", "exe" o "sys".</span><span class="sxs-lookup"><span data-stu-id="2a7e1-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="2a7e1-131">Infine, Cerca in una sottodirectory denominata "simboli" con una directory con lo stesso nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="2a7e1-132">Se, ad esempio, l'elemento del percorso dei simboli è "c: i simboli \\ " e il file in cui vengono cercati i simboli è "boo.dll", verrà eseguita una ricerca nelle directory seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="2a7e1-133">c: \\ simboli</span><span class="sxs-lookup"><span data-stu-id="2a7e1-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="2a7e1-134">c: \\ simbologia \\ dll</span><span class="sxs-lookup"><span data-stu-id="2a7e1-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="2a7e1-135">c: file \\ \\ \\ dll simboli</span><span class="sxs-lookup"><span data-stu-id="2a7e1-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="2a7e1-136">Il gestore di simboli usa questa logica per cercare qualsiasi elemento del percorso che non soddisfi i criteri per essere un *server di simboli* o una *cache* (descritto di seguito).</span><span class="sxs-lookup"><span data-stu-id="2a7e1-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="2a7e1-137">Elemento Path del server di simboli</span><span class="sxs-lookup"><span data-stu-id="2a7e1-137">Symbol Server Path Element</span></span>

<span data-ttu-id="2a7e1-138">Un elemento Path del *Server dei simboli* usa una tecnologia speciale che può individuare un simbolo che corrisponde esattamente al modulo in questione.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="2a7e1-139">Per altri dettagli, vedere [uso di symsrv](using-symsrv.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="2a7e1-140">Il gestore di simboli considera un elemento Path come un server di simboli se inizia con il testo "SRV \* ".</span><span class="sxs-lookup"><span data-stu-id="2a7e1-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="2a7e1-141">Se il testo "SRV \* " non è specificato ma l'elemento Path effettivo è un archivio del server dei simboli, il gestore di simboli fungerà da se è \* stato specificato "SRV".</span><span class="sxs-lookup"><span data-stu-id="2a7e1-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="2a7e1-142">Il gestore di simboli esegue questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="2a7e1-143">Elemento Path della cache</span><span class="sxs-lookup"><span data-stu-id="2a7e1-143">Cache Path Element</span></span>

<span data-ttu-id="2a7e1-144">Un elemento del percorso *della cache* è una variante di un elemento Path del server di simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="2a7e1-145">Questa directory viene cercata come qualsiasi altro server di simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="2a7e1-146">Tuttavia, se il simbolo non viene trovato qui e si trova in un elemento path più in basso nella catena del percorso dei simboli, il simbolo verrà copiato e archiviato nel server di simboli specificato in questo elemento.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="2a7e1-147">Il gestore di simboli considera un elemento Path come elemento della cache se inizia con il testo "cache \* ".</span><span class="sxs-lookup"><span data-stu-id="2a7e1-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="2a7e1-148">Per specificare una cache in "c: cache \\ ", usare un elemento del percorso dei simboli "cache \* c: cache \\ ".</span><span class="sxs-lookup"><span data-stu-id="2a7e1-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="2a7e1-149">Percorso di ricerca di esempio</span><span class="sxs-lookup"><span data-stu-id="2a7e1-149">Example Search Path</span></span>

<span data-ttu-id="2a7e1-150">Per verificarne il funzionamento, impostare questo percorso di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="2a7e1-151">Di seguito è riportato un elenco dell'output dettagliato del gestore di simboli durante la ricerca di ntdll. pdb, usando il percorso di ricerca riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

<span data-ttu-id="2a7e1-152">Le prime tre righe di output mostrano il gestore di simboli che elabora il primo elemento Path di `.` .</span><span class="sxs-lookup"><span data-stu-id="2a7e1-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="2a7e1-153">Si tratta di un elemento Path standard.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-153">This is a standard path element.</span></span>

<span data-ttu-id="2a7e1-154">La quarta riga indica il gestore di simboli che usa il server di simboli per cercare il file nel secondo elemento Path di `cache*c:\myCache` , che è un elemento Path della cache.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="2a7e1-155">La Quinta riga indica che il file si trova nel terzo elemento Path di `srv*\\symbols\symbols` , che è un elemento Path del server dei simboli.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="2a7e1-156">La sesta riga indica che il file viene copiato nella cache.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="2a7e1-157">Le ultime due righe che il file viene aperto dalla cache.</span><span class="sxs-lookup"><span data-stu-id="2a7e1-157">The last two lines that the file is opened from the cache.</span></span>
