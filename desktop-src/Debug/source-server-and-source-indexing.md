---
description: Il server di origine consente a un client di recuperare la versione esatta dei file di origine utilizzati per compilare un'applicazione.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Server di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320052"
---
# <a name="source-server"></a><span data-ttu-id="4c194-103">Server di origine</span><span class="sxs-lookup"><span data-stu-id="4c194-103">Source Server</span></span>

<span data-ttu-id="4c194-104">Il server di origine consente a un client di recuperare la versione esatta dei file di origine utilizzati per compilare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="4c194-105">Poiché il codice sorgente di un modulo può variare tra le versioni e per un certo periodo di tempo, è importante esaminare il codice sorgente esistente quando la versione del modulo in questione è stata compilata.</span><span class="sxs-lookup"><span data-stu-id="4c194-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="4c194-106">Il server di origine recupera i file appropriati dal controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="4c194-107">Per usare il server di origine, l'applicazione deve essere stata indicizzata come origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="4c194-108">Indicizzazione origine</span><span class="sxs-lookup"><span data-stu-id="4c194-108">Source Indexing</span></span>

<span data-ttu-id="4c194-109">Il sistema di indicizzazione dell'origine è una raccolta di file eseguibili e script Perl.</span><span class="sxs-lookup"><span data-stu-id="4c194-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="4c194-110">Per gli script Perl è necessario Perl 5,6 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4c194-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="4c194-111">In genere, i file binari sono indicizzati all'origine durante il processo di compilazione dopo che l'applicazione è stata compilata.</span><span class="sxs-lookup"><span data-stu-id="4c194-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="4c194-112">Le informazioni necessarie per il server di origine vengono archiviate nei file PDB.</span><span class="sxs-lookup"><span data-stu-id="4c194-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="4c194-113">Il server di origine viene attualmente fornito con script che dovrebbero funzionare con i sistemi di controllo del codice sorgente seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c194-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="4c194-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="4c194-114">Team Foundation Server</span></span>
-   <span data-ttu-id="4c194-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="4c194-115">Perforce</span></span>
-   <span data-ttu-id="4c194-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="4c194-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="4c194-117">CVS</span><span class="sxs-lookup"><span data-stu-id="4c194-117">CVS</span></span>
-   <span data-ttu-id="4c194-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="4c194-118">Subversion</span></span>

<span data-ttu-id="4c194-119">È anche possibile creare uno script personalizzato per indicizzare il codice per un altro sistema di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="4c194-120">Nella tabella seguente sono elencati gli strumenti del server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="4c194-121">Strumento</span><span class="sxs-lookup"><span data-stu-id="4c194-121">Tool</span></span>        | <span data-ttu-id="4c194-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c194-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c194-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="4c194-123">Srcsrv.ini</span></span>  | <span data-ttu-id="4c194-124">Questo file è l'elenco principale di tutti i server del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="4c194-125">Ogni voce ha il formato seguente:*MyServer* = *la*</span><span class="sxs-lookup"><span data-stu-id="4c194-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="4c194-126">Quando si utilizza Perforce, le informazioni sul server sono costituite dal percorso di rete completo del server, seguito da due punti, seguito dal numero di porta utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4c194-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="4c194-127">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4c194-127">For example:</span></span><br/> <span data-ttu-id="4c194-128">MyServer = Machine. Corp. Company. com: 1666</span><span class="sxs-lookup"><span data-stu-id="4c194-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="4c194-129">Questo file può essere installato nel computer in cui è in esecuzione il debugger.</span><span class="sxs-lookup"><span data-stu-id="4c194-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="4c194-130">Quando viene avviato, il server di origine esamina Srcsrv.ini per i valori; questi valori eseguiranno l'override delle informazioni contenute nel file PDB.</span><span class="sxs-lookup"><span data-stu-id="4c194-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="4c194-131">Ciò consente agli utenti di configurare un debugger per l'utilizzo di un server del controllo del codice sorgente alternativo in fase di debug.</span><span class="sxs-lookup"><span data-stu-id="4c194-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="4c194-132">Per ulteriori informazioni, vedere l'esempio Srcsrv.ini installato con gli strumenti del server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="4c194-133">Ssindex. cmd</span><span class="sxs-lookup"><span data-stu-id="4c194-133">Ssindex.cmd</span></span> | <span data-ttu-id="4c194-134">Questo script compila l'elenco dei file archiviati nel controllo del codice sorgente insieme alle informazioni sulla versione di ogni file.</span><span class="sxs-lookup"><span data-stu-id="4c194-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="4c194-135">Archivia un subset di queste informazioni nei file con estensione pdb generati quando è stata compilata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="4c194-136">Lo script usa uno dei moduli Perl seguenti per interfacciarsi con il controllo del codice sorgente: P4.pm (Perforce) o Vss.pm (Visual Source Safe). Per ulteriori informazioni, eseguire lo script con il-?</span><span class="sxs-lookup"><span data-stu-id="4c194-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="4c194-137">o-??</span><span class="sxs-lookup"><span data-stu-id="4c194-137">or -??</span></span> <span data-ttu-id="4c194-138">(Guida dettagliata) o esaminare lo script.</span><span class="sxs-lookup"><span data-stu-id="4c194-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4c194-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="4c194-139">Srctool.exe</span></span> | <span data-ttu-id="4c194-140">Questa utilità elenca tutti i file indicizzati in un file con estensione pdb.</span><span class="sxs-lookup"><span data-stu-id="4c194-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="4c194-141">Per ogni file vengono elencati il percorso completo, il server di controllo del codice sorgente e il numero di versione del file.</span><span class="sxs-lookup"><span data-stu-id="4c194-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="4c194-142">È possibile usare queste informazioni per recuperare i file senza usare il server di origine. Per ulteriori informazioni, eseguire l'utilità con/?</span><span class="sxs-lookup"><span data-stu-id="4c194-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="4c194-143">opzione.</span><span class="sxs-lookup"><span data-stu-id="4c194-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4c194-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="4c194-144">Pdbstr.exe</span></span>  | <span data-ttu-id="4c194-145">Questa utilità viene utilizzata dagli script di indicizzazione per inserire le informazioni sul controllo della versione nel flusso alternativo "SrcSrv" del file con estensione PDB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="4c194-146">Può inoltre leggere qualsiasi flusso da un file con estensione pdb.</span><span class="sxs-lookup"><span data-stu-id="4c194-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="4c194-147">È possibile utilizzare queste informazioni per verificare che gli script di indicizzazione funzionino correttamente. Per ulteriori informazioni, eseguire l'utilità con/?</span><span class="sxs-lookup"><span data-stu-id="4c194-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="4c194-148">opzione.</span><span class="sxs-lookup"><span data-stu-id="4c194-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="4c194-149">Recupero del file di origine</span><span class="sxs-lookup"><span data-stu-id="4c194-149">Retrieving the Source File</span></span>

<span data-ttu-id="4c194-150">L'API DbgHelp fornisce l'accesso alle funzionalità del server di origine tramite la funzione [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="4c194-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="4c194-151">Per recuperare il nome del file di origine da recuperare, chiamare la funzione [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) o [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .</span><span class="sxs-lookup"><span data-stu-id="4c194-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="4c194-152">Uso del server di origine con un debugger</span><span class="sxs-lookup"><span data-stu-id="4c194-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="4c194-153">Per usare il server di origine con WinDbg, KD, NTSD o CDB, verificare di avere installato una versione recente del pacchetto strumenti di debug per Windows (versione 6,3 o successiva).</span><span class="sxs-lookup"><span data-stu-id="4c194-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="4c194-154">Includere quindi SRV \* nel comando. Srcpath come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4c194-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="4c194-155">**\. Srcpath SRV \* ;** _c: \\ origine_</span><span class="sxs-lookup"><span data-stu-id="4c194-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="4c194-156">Si noti che questo esempio include anche un percorso di origine tradizionale.</span><span class="sxs-lookup"><span data-stu-id="4c194-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="4c194-157">Se il debugger non è in grado di recuperare il file dal server di origine, eseguirà la ricerca nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="4c194-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="4c194-158">Se un file di origine viene recuperato dal server di origine, rimarrà sul disco rigido al termine della sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="4c194-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="4c194-159">I file di origine vengono archiviati localmente nella sottodirectory src della directory di installazione degli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="4c194-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="4c194-160">Blocchi di dati del server di origine</span><span class="sxs-lookup"><span data-stu-id="4c194-160">Source Server Data Blocks</span></span>

<span data-ttu-id="4c194-161">Il server di origine si basa su due blocchi di dati all'interno del file PDB.</span><span class="sxs-lookup"><span data-stu-id="4c194-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="4c194-162">Elenco dei file di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-162">Source file list.</span></span> <span data-ttu-id="4c194-163">La compilazione di un modulo crea automaticamente un elenco di percorsi completi per i file di origine usati per compilare il modulo.</span><span class="sxs-lookup"><span data-stu-id="4c194-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="4c194-164">Blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="4c194-164">Data block.</span></span> <span data-ttu-id="4c194-165">L'indicizzazione dell'origine, come descritto in precedenza, aggiunge un flusso alternativo al file PDB denominato "SrcSrv".</span><span class="sxs-lookup"><span data-stu-id="4c194-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="4c194-166">Lo script che inserisce questi dati dipende dal processo di compilazione specifico e dal sistema di controllo del codice sorgente in uso.</span><span class="sxs-lookup"><span data-stu-id="4c194-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="4c194-167">Nella specifica del linguaggio versione 1 il blocco di dati è suddiviso in tre sezioni: ini, variabili e file di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="4c194-168">Ha la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="4c194-168">It has the following syntax.</span></span>

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

<span data-ttu-id="4c194-169">Tutto il testo viene interpretato letteralmente, ad eccezione del testo racchiuso tra segni di percentuale (%).</span><span class="sxs-lookup"><span data-stu-id="4c194-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="4c194-170">Il testo racchiuso tra simboli di percentuale viene considerato come un nome di variabile da risolvere in modo ricorsivo, a meno che non si tratti di una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c194-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="4c194-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span><span class="sxs-lookup"><span data-stu-id="4c194-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="4c194-172">Il testo del parametro deve essere racchiuso tra simboli di percentuale e considerato come una variabile da espandere.</span><span class="sxs-lookup"><span data-stu-id="4c194-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span><span class="sxs-lookup"><span data-stu-id="4c194-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="4c194-174">Tutte le barre (/) nel testo del parametro devono essere sostituite con barre rovesciate ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="4c194-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="4c194-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span><span class="sxs-lookup"><span data-stu-id="4c194-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="4c194-176">Tutte le informazioni sul percorso nel testo del parametro devono essere rimosse, lasciando solo il nome del file.</span><span class="sxs-lookup"><span data-stu-id="4c194-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="4c194-177">La sezione INI contiene le variabili che descrivono i requisiti.</span><span class="sxs-lookup"><span data-stu-id="4c194-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="4c194-178">Lo script di indicizzazione può aggiungere un numero qualsiasi di variabili a questa sezione.</span><span class="sxs-lookup"><span data-stu-id="4c194-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="4c194-179">Alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="4c194-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="4c194-180"><span id="VERSION"></span><span id="version"></span>Versione</span><span class="sxs-lookup"><span data-stu-id="4c194-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="4c194-181">Versione della specifica del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="4c194-181">The language specification version.</span></span> <span data-ttu-id="4c194-182">Questa variabile è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="4c194-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span><span class="sxs-lookup"><span data-stu-id="4c194-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="4c194-184">Stringa che descrive il prodotto del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-184">A string that describes the source control product.</span></span> <span data-ttu-id="4c194-185">Questa variabile è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4c194-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span><span class="sxs-lookup"><span data-stu-id="4c194-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="4c194-187">Stringa che indica la data e l'ora di elaborazione del file PDB.</span><span class="sxs-lookup"><span data-stu-id="4c194-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="4c194-188">Questa variabile è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4c194-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="4c194-189">La sezione variables contiene variabili che descrivono come estrarre un file dal controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="4c194-190">Può inoltre essere utilizzato per definire il testo comunemente utilizzato come variabile per ridurre le dimensioni del blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="4c194-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="4c194-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span><span class="sxs-lookup"><span data-stu-id="4c194-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="4c194-192">Viene descritto come compilare il percorso di destinazione per il file estratto.</span><span class="sxs-lookup"><span data-stu-id="4c194-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="4c194-193">Si tratta di una variabile obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="4c194-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span><span class="sxs-lookup"><span data-stu-id="4c194-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="4c194-195">Viene descritto come compilare il comando per estrarre il file dal controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="4c194-196">Sono inclusi il nome del file eseguibile e i relativi parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4c194-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="4c194-197">Si tratta di una variabile obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="4c194-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span><span class="sxs-lookup"><span data-stu-id="4c194-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="4c194-199">Stringa che elenca le variabili di ambiente da creare durante l'estrazione del file.</span><span class="sxs-lookup"><span data-stu-id="4c194-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="4c194-200">Separare più voci con un carattere backspace ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="4c194-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="4c194-201">Si tratta di una variabile facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4c194-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="4c194-202">La sezione file di origine contiene una voce per ogni file di origine indicizzato.</span><span class="sxs-lookup"><span data-stu-id="4c194-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="4c194-203">Il contenuto di ogni riga viene interpretato come variabile con i nomi VAR1, VAR2, VAR3 e così via fino a VAR10.</span><span class="sxs-lookup"><span data-stu-id="4c194-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="4c194-204">Le variabili sono separate da asterischi.</span><span class="sxs-lookup"><span data-stu-id="4c194-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="4c194-205">VAR1 deve specificare il percorso completo del file di origine, come elencato altrove nel file PDB.</span><span class="sxs-lookup"><span data-stu-id="4c194-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="4c194-206">Ad esempio, la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="4c194-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="4c194-207">viene interpretato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="4c194-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="4c194-208">In questo esempio, VAR4 è un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="4c194-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="4c194-209">Tuttavia, la maggior parte dei sistemi di controllo del codice sorgente supporta l'assegnazione di etichette ai file in modo da poter ripristinare lo stato di origine di una determinata compilazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="4c194-210">Pertanto, è possibile usare in alternativa l'etichetta per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="4c194-211">Il blocco di dati di esempio può essere modificato in modo da contenere una variabile come la seguente:</span><span class="sxs-lookup"><span data-stu-id="4c194-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="4c194-212">Quindi, presumendo che il sistema di controllo del codice sorgente usi il simbolo di chiocciola (@) per indicare un'etichetta, è possibile modificare la variabile SRCSRVCMD nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="4c194-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="4c194-213">**sd.exe-p% fnvar%(% var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% label%**</span><span class="sxs-lookup"><span data-stu-id="4c194-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="4c194-214">Funzionamento del server di origine</span><span class="sxs-lookup"><span data-stu-id="4c194-214">How Source Server Works</span></span>

<span data-ttu-id="4c194-215">Il client del server di origine viene implementato in Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="4c194-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="4c194-216">Il client non estrae informazioni direttamente dal file PDB. Usa un gestore di simboli, ad esempio quello implementato in Dbghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="4c194-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="4c194-217">Si tratta essenzialmente di un motore di sostituzione di variabili ricorsive che consente di creare una riga di comando che può essere utilizzata per estrarre il file di origine appropriato dal sistema di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="4c194-218">Il codice non deve chiamare direttamente Symsrv.dll.</span><span class="sxs-lookup"><span data-stu-id="4c194-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="4c194-219">Per integrare le funzionalità nell'applicazione, usare la funzione [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .</span><span class="sxs-lookup"><span data-stu-id="4c194-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="4c194-220">La prima versione del server di origine funziona nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="4c194-220">The first version of source server works as follows.</span></span> <span data-ttu-id="4c194-221">Questo comportamento potrebbe cambiare nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="4c194-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="4c194-222">Il client chiama la funzione **SrcSrvInit** con il percorso di destinazione da utilizzare come base per tutte le estrazioni di file di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="4c194-223">Questo percorso viene archiviato nella variabile es.</span><span class="sxs-lookup"><span data-stu-id="4c194-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="4c194-224">Il client estrae il flusso SrcSrv dal PDB quando viene caricato il PDB del modulo e chiama la funzione **SrcSrvLoadModule** per passare il blocco di dati al server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="4c194-225">Quando dbghelp recupera un file di origine, il client chiama la funzione **SrcSrvGetFile** per recuperare i file di origine dal controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="4c194-226">Il server di origine Cerca nel blocco di dati le voci del file di origine per una voce corrispondente al file richiesto.</span><span class="sxs-lookup"><span data-stu-id="4c194-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="4c194-227">Inserisce VAR1 in VAR *n* con il contenuto della voce del file di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="4c194-228">Espande quindi la variabile SRCSRVTRG usando VAR1 a VAR *n*.</span><span class="sxs-lookup"><span data-stu-id="4c194-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="4c194-229">Se il file si trova già in questa posizione, restituisce il percorso al chiamante.</span><span class="sxs-lookup"><span data-stu-id="4c194-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="4c194-230">In caso contrario, espande la variabile SRCSRVCMD per compilare il comando necessario per recuperare il file dal controllo del codice sorgente e copiarlo nel percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c194-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="4c194-231">Infine, viene eseguito questo comando.</span><span class="sxs-lookup"><span data-stu-id="4c194-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="4c194-232">Creazione di un modulo del provider del controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="4c194-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="4c194-233">Il server di origine include i moduli provider per Perforce (p4.pm) e Visual Source Safe (vss.pm).</span><span class="sxs-lookup"><span data-stu-id="4c194-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="4c194-234">Per creare un modulo provider personalizzato, è necessario implementare il seguente set di interfacce.</span><span class="sxs-lookup"><span data-stu-id="4c194-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="4c194-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module:: SimpleUsage ()**</span><span class="sxs-lookup"><span data-stu-id="4c194-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-236">Scopo: Visualizza informazioni semplici sull'utilizzo del modulo in STDOUT.</span><span class="sxs-lookup"><span data-stu-id="4c194-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="4c194-237">Parametri: nessuno</span><span class="sxs-lookup"><span data-stu-id="4c194-237">Parameters: None</span></span>

<span data-ttu-id="4c194-238">Valore restituito: None</span><span class="sxs-lookup"><span data-stu-id="4c194-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4c194-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module:: VerboseUsage ()**</span><span class="sxs-lookup"><span data-stu-id="4c194-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-240">Scopo: Visualizza informazioni dettagliate sull'utilizzo del modulo in STDOUT.</span><span class="sxs-lookup"><span data-stu-id="4c194-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="4c194-241">Parametri: nessuno</span><span class="sxs-lookup"><span data-stu-id="4c194-241">Parameters: None</span></span>

<span data-ttu-id="4c194-242">Valore restituito: None</span><span class="sxs-lookup"><span data-stu-id="4c194-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4c194-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module:: New ( \@ CommandArguments)**</span><span class="sxs-lookup"><span data-stu-id="4c194-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-244">Scopo: Inizializza un'istanza del modulo provider.</span><span class="sxs-lookup"><span data-stu-id="4c194-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="4c194-245">Parameters: tutti gli @ARGV argomenti che non sono stati riconosciuti da SSIndex. cmd come argomenti generali.</span><span class="sxs-lookup"><span data-stu-id="4c194-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="4c194-246">Valore restituito: riferimento che può essere usato nelle operazioni successive.</span><span class="sxs-lookup"><span data-stu-id="4c194-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="4c194-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-248">Scopo: consente al modulo di raccogliere le informazioni di indicizzazione dell'origine necessarie per la directory specificata dal parametro $SourcePath.</span><span class="sxs-lookup"><span data-stu-id="4c194-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="4c194-249">Il modulo non presuppone che questa voce venga chiamata solo una volta per ogni istanza dell'oggetto, perché SSIndex. cmd può chiamarla più volte per percorsi diversi.</span><span class="sxs-lookup"><span data-stu-id="4c194-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="4c194-250">Parameters: (1) directory locale contenente l'origine da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="4c194-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="4c194-251">(2) riferimento a un hash contenente tutte le voci del file di Srcsrv.ini specificato.</span><span class="sxs-lookup"><span data-stu-id="4c194-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="4c194-252">Valore restituito: None</span><span class="sxs-lookup"><span data-stu-id="4c194-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4c194-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="4c194-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-254">Scopo: fornisce le informazioni necessarie per estrarre un singolo file specifico dal sistema di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="4c194-255">Parameters: un nome file completo</span><span class="sxs-lookup"><span data-stu-id="4c194-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="4c194-256">Valore restituito: (1) un riferimento hash delle variabili necessarie per interpretare il $FileEntry restituito.</span><span class="sxs-lookup"><span data-stu-id="4c194-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="4c194-257">SSIndex. cmd memorizza nella cache queste variabili per ogni file di origine utilizzato da un singolo file di debug per ridurre la quantità di informazioni scritte nel flusso dell'indice di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="4c194-258">(2) la voce del file da scrivere nel flusso dell'indice di origine per consentire SrcSrv.dll estrarre il file dal controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="4c194-259">Il formato esatto di questa riga è specifico del sistema di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**</span><span class="sxs-lookup"><span data-stu-id="4c194-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-261">Scopo: fornisce una stringa descrittiva per identificare il provider del controllo del codice sorgente per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="4c194-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="4c194-262">Parametri: nessuno</span><span class="sxs-lookup"><span data-stu-id="4c194-262">Parameters: None</span></span>

<span data-ttu-id="4c194-263">Valore restituito: nome descrittivo del sistema di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4c194-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="4c194-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**</span><span class="sxs-lookup"><span data-stu-id="4c194-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="4c194-265">Scopo: consente al provider del controllo del codice sorgente di aggiungere variabili specifiche del controllo del codice sorgente al flusso di origine per ogni file di debug.</span><span class="sxs-lookup"><span data-stu-id="4c194-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="4c194-266">I moduli di esempio usano questo metodo per scrivere le \_ variabili di destinazione Extract cmd ed Extract \_ .</span><span class="sxs-lookup"><span data-stu-id="4c194-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="4c194-267">Parametri: nessuno</span><span class="sxs-lookup"><span data-stu-id="4c194-267">Parameters: None</span></span>

<span data-ttu-id="4c194-268">Valore restituito: elenco di voci per le variabili del flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="4c194-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




