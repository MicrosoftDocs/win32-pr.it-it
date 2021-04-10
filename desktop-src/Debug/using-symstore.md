---
description: SymStore (symstore.exe) è uno strumento per la creazione di archivi simboli. È incluso nel pacchetto di strumenti di debug per Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Uso di SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126813"
---
# <a name="using-symstore"></a><span data-ttu-id="a5f3d-104">Uso di SymStore</span><span class="sxs-lookup"><span data-stu-id="a5f3d-104">Using SymStore</span></span>

<span data-ttu-id="a5f3d-105">SymStore (symstore.exe) è uno strumento per la creazione di archivi simboli.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="a5f3d-106">È incluso nel pacchetto [di strumenti di debug per Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="a5f3d-107">SymStore archivia i simboli in un formato che consente al debugger di cercare i simboli in base al timestamp e alle dimensioni dell'immagine (per un file con estensione DBG o eseguibile) oppure la firma e l'età (per un file con estensione pdb).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="a5f3d-108">Il vantaggio dell'archivio dei simboli nel formato di archiviazione dei simboli tradizionale è che tutti i simboli possono essere archiviati o a cui viene fatto riferimento nello stesso server e recuperati dal debugger senza alcuna conoscenza precedente del prodotto che contiene il simbolo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="a5f3d-109">Si noti che più versioni dei file di simboli PDB, ad esempio le versioni Public e private, non possono essere archiviate nello stesso server, perché ognuna contengono la stessa firma e l'età.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="a5f3d-110">Transazioni SymStore</span><span class="sxs-lookup"><span data-stu-id="a5f3d-110">SymStore Transactions</span></span>

<span data-ttu-id="a5f3d-111">Ogni chiamata a SymStore viene registrata come transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="a5f3d-112">Esistono due tipi di transazioni: Add ed Delete.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="a5f3d-113">Quando viene creato l'archivio dei simboli, viene creata una directory denominata "000admin" nella radice del server.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="a5f3d-114">La directory 000admin contiene un file per ogni transazione, nonché i file di log Server.txt e History.txt.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="a5f3d-115">Il file di Server.txt contiene un elenco di tutte le transazioni attualmente presenti nel server.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="a5f3d-116">Il file di History.txt contiene una cronologia cronologica di tutte le transazioni.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="a5f3d-117">Ogni volta che SymStore archivia o rimuove i file di simboli, viene creato un nuovo numero di transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="a5f3d-118">Quindi, viene creato un file, il cui nome è il numero di transazione, in 000admin.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="a5f3d-119">Questo file contiene un elenco di tutti i file o puntatori che sono stati aggiunti all'archivio simboli durante la transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="a5f3d-120">Se viene eliminata una transazione, SymStore leggerà il file di transazione per individuare i file e i puntatori da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="a5f3d-121">Le opzioni **Add** e **Canc** specificano se deve essere eseguita una transazione Add o DELETE.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="a5f3d-122">Se si include l'opzione **/p** con un'operazione Add, viene specificato che deve essere aggiunto un puntatore. Se si omette l'opzione **/p** , viene specificato che è necessario aggiungere il file di simboli effettivo.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="a5f3d-123">È anche possibile creare l'archivio dei simboli in due fasi separate.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="a5f3d-124">Nella prima fase si usa SymStore con l'opzione **/x** per creare un file di indice.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="a5f3d-125">Nella seconda fase, si usa SymStore con l'opzione **/y** per creare l'archivio effettivo di file o puntatori dalle informazioni contenute nel file di indice.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="a5f3d-126">Questa tecnica può essere utile per svariati motivi.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="a5f3d-127">Questo consente, ad esempio, di ricreare facilmente l'archivio simboli se l'archivio è in qualche modo perduto, purché il file di indice esista ancora.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="a5f3d-128">O forse il computer che contiene i file di simboli ha una connessione di rete lenta al computer in cui verrà creato l'archivio dei simboli.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="a5f3d-129">In questo caso, è possibile creare il file di indice nello stesso computer dei file di simboli, trasferire il file di indice nel secondo computer, quindi creare l'archivio nel secondo computer.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="a5f3d-130">Per un elenco completo di tutti i parametri di SymStore, vedere [Opzioni di Command-Line SymStore](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="a5f3d-131">SymStore non supporta transazioni simultanee da più utenti.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="a5f3d-132">È consigliabile che un utente sia designato come "amministratore" dell'archivio simboli ed è responsabile di tutte le transazioni **Aggiungi** e **del** .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="a5f3d-133">Esempi di transazioni</span><span class="sxs-lookup"><span data-stu-id="a5f3d-133">Transaction Examples</span></span>

<span data-ttu-id="a5f3d-134">Ecco due esempi di SymStore che aggiungono puntatori a simboli per la build 3790 di Windows Server 2003 a \\ \\ SampleDir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="a5f3d-135">Nell'esempio seguente SymStore aggiunge i file di simboli effettivi per un progetto di applicazione in \\ \\ Largeapp \\ AppServer \\ bin a \\ \\ TestDir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="a5f3d-136">Di seguito è riportato un esempio di utilizzo di un file di indice.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="a5f3d-137">In primo luogo, SymStore crea un file di indice in base alla raccolta di file di simboli nei \\ \\ \\ bin Largeapp AppServer \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="a5f3d-138">In questo caso, il file di indice si trova in un terzo computer, \\ \\ HUBSERVER \\ hubshare.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="a5f3d-139">Usare l'opzione **/g** per specificare che il prefisso del file " \\ \\ Largeapp \\ AppServer" potrebbe cambiare in futuro:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="a5f3d-140">Si supponga ora di spostare tutti i file di simboli dal computer \\ \\ Largeapp \\ AppServer e inserirli in \\ \\ archivio \\ AppServer.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="a5f3d-141">È quindi possibile creare l'archivio dei simboli dal file di indice \\ \\ hubserver \\ hubshare \\myindex.txt come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="a5f3d-142">Infine, di seguito è riportato un esempio di SymStore che elimina un file aggiunto da una transazione precedente.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="a5f3d-143">Per una spiegazione su come determinare l'ID della transazione, in questo caso 0000000096, vedere la sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="a5f3d-144">File compressi</span><span class="sxs-lookup"><span data-stu-id="a5f3d-144">Compressed Files</span></span>

<span data-ttu-id="a5f3d-145">SymStore può essere usato con i file compressi in due modi diversi.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="a5f3d-146">Usare SymStore con l'opzione **/p** per archiviare i puntatori nei file di simboli.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="a5f3d-147">Al termine della SymStore, comprimere i file a cui fanno riferimento i puntatori.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="a5f3d-148">Usare SymStore con l'opzione **/x** per creare un file di indice.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="a5f3d-149">Al termine della SymStore, comprimere i file elencati nel file di indice.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="a5f3d-150">Usare quindi SymStore con l'opzione **/y** e, se si vuole, l'opzione **/p** , per archiviare i file o i puntatori ai file nell'archivio dei simboli.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="a5f3d-151">Per eseguire questa operazione, SymStore non dovrà decomprimere i file.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="a5f3d-152">Il server di simboli sarà responsabile della decompressione dei file quando sono necessari.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="a5f3d-153">Se si utilizza SymSrv come server di simboli, è necessario eseguire la compressione utilizzando lo strumento compress.exe distribuito con Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5f3d-154">I file compressi devono avere un carattere di sottolineatura come ultimo carattere nelle estensioni di file, ad esempio Module1. PD \_ o Module2. DB \_ .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="a5f3d-155">Per informazioni dettagliate, vedere [uso di symsrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="a5f3d-156">File server.txt e history.txt</span><span class="sxs-lookup"><span data-stu-id="a5f3d-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="a5f3d-157">Quando viene aggiunta una transazione, vengono aggiunti diversi elementi di informazioni a server.txt e history.txt per la funzionalità di ricerca futura.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="a5f3d-158">Di seguito è riportato un esempio di riga in server.txt e history.txt per una transazione di aggiunta:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="a5f3d-159">Si tratta di una riga delimitata da virgole.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-159">This is a comma-separated line.</span></span> <span data-ttu-id="a5f3d-160">I campi vengono definiti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="a5f3d-161">Campo</span><span class="sxs-lookup"><span data-stu-id="a5f3d-161">Field</span></span>      | <span data-ttu-id="a5f3d-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f3d-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f3d-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="a5f3d-163">0000000096</span></span> | <span data-ttu-id="a5f3d-164">Numero ID transazione, creato da SymStore.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="a5f3d-165">add</span><span class="sxs-lookup"><span data-stu-id="a5f3d-165">add</span></span>        | <span data-ttu-id="a5f3d-166">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-166">Type of transaction.</span></span> <span data-ttu-id="a5f3d-167">Questo campo può essere **Add** o **Canc**.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="a5f3d-168">ptr</span><span class="sxs-lookup"><span data-stu-id="a5f3d-168">ptr</span></span>        | <span data-ttu-id="a5f3d-169">Indica se i file o i puntatori sono stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-169">Whether files or pointers were added.</span></span> <span data-ttu-id="a5f3d-170">Questo campo può essere **file** o **ptr**.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="a5f3d-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="a5f3d-171">10/09/99</span></span>   | <span data-ttu-id="a5f3d-172">Data in cui si è verificata la transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="a5f3d-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="a5f3d-173">00:08:32</span></span>   | <span data-ttu-id="a5f3d-174">Ora di inizio della transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="a5f3d-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5f3d-175">Windows XP</span></span> | <span data-ttu-id="a5f3d-176">Prodotto.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-176">Product.</span></span>                                                                            |
| <span data-ttu-id="a5f3d-177">da x86 a fre</span><span class="sxs-lookup"><span data-stu-id="a5f3d-177">x86 fre</span></span>    | <span data-ttu-id="a5f3d-178">Version (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="a5f3d-179">Aggiunto da</span><span class="sxs-lookup"><span data-stu-id="a5f3d-179">Added from</span></span> | <span data-ttu-id="a5f3d-180">Commento (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="a5f3d-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="a5f3d-181">Non utilizzato</span><span class="sxs-lookup"><span data-stu-id="a5f3d-181">Unused</span></span>     | <span data-ttu-id="a5f3d-182">(Riservato per un uso successivo).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="a5f3d-183">Di seguito sono riportate alcune righe di esempio dal file di transazione 0000000096.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="a5f3d-184">Ogni riga registra la directory e il percorso del file o del puntatore aggiunto alla directory.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="a5f3d-185">Se si usa una **transazione per** annullare le transazioni di **aggiunta** originali, queste righe verranno rimosse da server.txt e la riga seguente verrà aggiunta al history.txt:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="a5f3d-186">I campi per la transazione DELETE vengono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="a5f3d-187">Campo</span><span class="sxs-lookup"><span data-stu-id="a5f3d-187">Field</span></span>      | <span data-ttu-id="a5f3d-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f3d-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="a5f3d-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="a5f3d-189">0000000105</span></span> | <span data-ttu-id="a5f3d-190">Numero ID transazione, creato da SymStore.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="a5f3d-191">del</span><span class="sxs-lookup"><span data-stu-id="a5f3d-191">del</span></span>        | <span data-ttu-id="a5f3d-192">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-192">Type of transaction.</span></span> <span data-ttu-id="a5f3d-193">Questo campo può essere **Add** o **Canc**.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="a5f3d-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="a5f3d-194">0000000096</span></span> | <span data-ttu-id="a5f3d-195">Transazione eliminata.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="a5f3d-196">Formato di archiviazione simboli</span><span class="sxs-lookup"><span data-stu-id="a5f3d-196">Symbol Storage Format</span></span>

<span data-ttu-id="a5f3d-197">SymStore usa il file system stesso come database.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="a5f3d-198">Viene creato un elevato albero di directory con nomi di directory basati su elementi quali i timestamp del file di simboli, le firme, l'età e altri dati.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="a5f3d-199">Ad esempio, dopo aver aggiunto al server diversi file ACPI. dbg diversi, le directory potrebbero avere un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="a5f3d-200">In questo esempio, il percorso di ricerca per il file di simboli ACPI. dbg potrebbe avere un aspetto simile al seguente: \\ \\ \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="a5f3d-201">All'interno della directory di ricerca potrebbero esistere tre file:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="a5f3d-202">Se il file è stato archiviato, ACPI. dbg sarà presente.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="a5f3d-203">Se è stato archiviato un puntatore, sarà presente un file denominato file. ptr che conterrà il percorso del file di simboli effettivo.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="a5f3d-204">Un file denominato refs. PTR, che contiene un elenco di tutti i percorsi correnti per ACPI. dbg con questo timestamp e le dimensioni dell'immagine che sono attualmente aggiunti all'archivio simboli.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="a5f3d-205">Visualizzazione dell'elenco di directory di \\ \\ Builds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 fornisce quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="a5f3d-206">Il file file. PTR contiene la stringa di testo " \\ \\ combuilds \\ symbols \\ x86 \\ 2128. chk \\ symbols \\ sys \\ ACPI. dbg".</span><span class="sxs-lookup"><span data-stu-id="a5f3d-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="a5f3d-207">Poiché in questa directory non è presente alcun file denominato ACPI. dbg, il debugger tenterà di trovare il file nei \\ \\ simboli di compilazione \\ \\ x86 \\ 2128. chk \\ simboli \\ sys \\ ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="a5f3d-208">Il contenuto di refs. ptr viene usato solo da SymStore, non dal debugger.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="a5f3d-209">Questo file contiene un record di tutte le transazioni eseguite in questa directory.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="a5f3d-210">Una riga di esempio da refs. PTR potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="a5f3d-211">Questo mostra che un puntatore a \\ \\ compiles \\ symbols \\ x86 \\ 2128. \\ chk symbols \\ sys \\ ACPI. dbg è stato aggiunto con la transazione "0000000026".</span><span class="sxs-lookup"><span data-stu-id="a5f3d-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="a5f3d-212">Alcuni file di simboli vengono mantenuti costanti tramite vari prodotti o compilazioni o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="a5f3d-213">Un esempio è il file Msvcrt. pdb.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="a5f3d-214">Eseguendo una directory di \\ \\ Builds \\ symsrv \\ Msvcrt. pdb viene mostrato che al server dei simboli sono state aggiunte solo due versioni di MSVCRT. pdb:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="a5f3d-215">Tuttavia, se si esegue una directory di \\ \\ \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 è indicato che refs. PTR contiene diversi puntatori.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="a5f3d-216">Il contenuto di \\ \\ Builds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 \\ refs. ptr è il seguente:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="a5f3d-217">Questo mostra che è stato usato lo stesso file Msvcrt. pdb per più compilazioni di simboli archiviati in \\ \\ symsrv di compilazione \\ .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="a5f3d-218">Di seguito è riportato un esempio di una directory che contiene una combinazione di aggiunte di file e puntatori:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="a5f3d-219">In questo caso refs. PTR presenta il contenuto seguente:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="a5f3d-220">Quindi, le transazioni 43, 44 e 45 aggiungono lo stesso file al server e le transazioni 46 e 47 aggiungono puntatori.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="a5f3d-221">Se vengono eliminate le transazioni 43, 44 e 45, il file Dbghelp. dbg verrà eliminato dalla directory.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="a5f3d-222">La directory avrà quindi il contenuto seguente:</span><span class="sxs-lookup"><span data-stu-id="a5f3d-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="a5f3d-223">Ora file. PTR contiene " \\ \\ sampledir2 \\ bin \\ symbols \\ retail \\ dll \\ dbghelp. dbg" e refs. PTR Contains</span><span class="sxs-lookup"><span data-stu-id="a5f3d-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="a5f3d-224">Ogni volta che la voce finale in refs. ptr è un puntatore, il file file. PTR sarà presente e conterrà il percorso del file associato.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="a5f3d-225">Ogni volta che la voce finale in refs. ptr è un file, non è presente alcun file. PTR presente in questa directory.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="a5f3d-226">Pertanto, qualsiasi operazione di eliminazione che rimuove la voce finale in refs. PTR può comportare la creazione, l'eliminazione o la modifica di file. ptr.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



