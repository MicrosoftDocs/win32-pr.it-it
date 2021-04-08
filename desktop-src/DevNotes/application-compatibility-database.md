---
description: L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Database di compatibilità delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747967"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="03112-103">Database di compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="03112-103">Application Compatibility Database</span></span>

<span data-ttu-id="03112-104">L'infrastruttura di compatibilità usa un database per identificare i problemi di compatibilità delle applicazioni e le relative soluzioni.</span><span class="sxs-lookup"><span data-stu-id="03112-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="03112-105">Questo database è un file binario indicizzato con estensione sdb.</span><span class="sxs-lookup"><span data-stu-id="03112-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="03112-106">L'infrastruttura di compatibilità fornisce un'interfaccia di programmazione per accedere al database.</span><span class="sxs-lookup"><span data-stu-id="03112-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="03112-107">I problemi di compatibilità possono essere risolti in base alle singole applicazioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03112-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="03112-108">Ogni applicazione specificata nel database contiene uno o più componenti che necessitano di una soluzione.</span><span class="sxs-lookup"><span data-stu-id="03112-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="03112-109">I componenti sono file eseguibili che vengono in genere descritti utilizzando i rispettivi attributi di file, ad esempio checksum.</span><span class="sxs-lookup"><span data-stu-id="03112-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="03112-110">Il processo di ricerca del database e di determinazione delle soluzioni per ogni applicazione viene chiamato *corrispondente*.</span><span class="sxs-lookup"><span data-stu-id="03112-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="03112-111">Per creare una corrispondenza univoca, è possibile usare gli attributi di file e la presenza di file associati nella cartella o nella sottocartella che contiene il file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="03112-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="03112-112">I file associati sono denominati *file corrispondenti*.</span><span class="sxs-lookup"><span data-stu-id="03112-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="03112-113">Un *tag* è un identificatore univoco per le voci e gli attributi nel database.</span><span class="sxs-lookup"><span data-stu-id="03112-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="03112-114">Il *tipo di tag* indica il formato dei dati associati al [**tag**](tag.md).</span><span class="sxs-lookup"><span data-stu-id="03112-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="03112-115">Ad esempio, **il \_ nome del tag** è di tipo **tag \_ \_ STRINGREF**. i dati per il **\_ nome del tag** sono una stringa del nome.</span><span class="sxs-lookup"><span data-stu-id="03112-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="03112-116">Un *TagId* è un puntatore a una voce in un particolare database.</span><span class="sxs-lookup"><span data-stu-id="03112-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="03112-117">Un *TAGREF* è un puntatore a una voce che può essere utilizzata in più database.</span><span class="sxs-lookup"><span data-stu-id="03112-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="03112-118">*Gli attributi di file* sono metadati associati a un file su disco.</span><span class="sxs-lookup"><span data-stu-id="03112-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="03112-119">Questi attributi includono il nome file, le dimensioni del file, il checksum, la versione e la data.</span><span class="sxs-lookup"><span data-stu-id="03112-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="03112-120">Questi attributi vengono utilizzati per determinare se un file caricato dal sistema corrisponde a una voce di database.</span><span class="sxs-lookup"><span data-stu-id="03112-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="03112-121">Pertanto, questi attributi di file sono denominati anche *attributi corrispondenti*.</span><span class="sxs-lookup"><span data-stu-id="03112-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="03112-122">Soluzioni</span><span class="sxs-lookup"><span data-stu-id="03112-122">Solutions</span></span>

<span data-ttu-id="03112-123">Le soluzioni più comuni applicate ai componenti di un'applicazione sono AppHelp e AppFix.</span><span class="sxs-lookup"><span data-stu-id="03112-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="03112-124">Con AppHelp, viene visualizzata una notifica di messaggio localizzata personalizzata, in genere quando l'applicazione viene installata o avviata.</span><span class="sxs-lookup"><span data-stu-id="03112-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="03112-125">Contiene un breve testo che illustra il problema di compatibilità e fornisce la possibilità di continuare a eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03112-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="03112-126">Tuttavia, alcune applicazioni avranno esito negativo in modo significativo. Apphelp non fornirà all'utente la possibilità di continuare a eseguire queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="03112-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="03112-127">Con AppFix, vengono installati hook per le API chiamate dai componenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03112-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="03112-128">Questi hook puntano alle funzioni stub che possono essere chiamate al posto delle funzioni di sistema (note anche come *spessoramento*).</span><span class="sxs-lookup"><span data-stu-id="03112-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="03112-129">Le funzioni Stub eseguono le operazioni necessarie per consentire l'esecuzione dell'applicazione nella versione installata di Windows.</span><span class="sxs-lookup"><span data-stu-id="03112-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="03112-130">Ogni funzione stub può chiamare facoltativamente la funzione di sistema dopo aver completato il lavoro.</span><span class="sxs-lookup"><span data-stu-id="03112-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="03112-131">Un *livello* o una *modalità* di compatibilità contiene uno o più shim e flag.</span><span class="sxs-lookup"><span data-stu-id="03112-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="03112-132">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="03112-132">In this section</span></span>

-   [<span data-ttu-id="03112-133">**\_dati APPHELP**</span><span class="sxs-lookup"><span data-stu-id="03112-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="03112-134">**ATTRINFO**</span><span class="sxs-lookup"><span data-stu-id="03112-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="03112-135">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="03112-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="03112-136">**TROVA \_ informazioni**</span><span class="sxs-lookup"><span data-stu-id="03112-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="03112-137">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="03112-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="03112-138">**tipo di percorso \_**</span><span class="sxs-lookup"><span data-stu-id="03112-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="03112-139">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="03112-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="03112-140">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="03112-141">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="03112-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="03112-142">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="03112-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="03112-143">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="03112-144">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="03112-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="03112-145">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="03112-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="03112-146">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="03112-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="03112-147">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="03112-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="03112-148">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="03112-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="03112-149">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="03112-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="03112-150">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="03112-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="03112-151">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="03112-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="03112-152">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="03112-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="03112-153">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="03112-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="03112-154">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="03112-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="03112-155">**SdbGetIndex**</span><span class="sxs-lookup"><span data-stu-id="03112-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="03112-156">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="03112-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="03112-157">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="03112-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="03112-158">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="03112-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="03112-159">**SdbGetTagFromTagID**</span><span class="sxs-lookup"><span data-stu-id="03112-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="03112-160">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="03112-161">**SdbIsStandardDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="03112-162">**SdbMakeIndexKeyFromString**</span><span class="sxs-lookup"><span data-stu-id="03112-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="03112-163">**SdbOpenApphelpDetailsDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="03112-164">**SdbOpenApphelpResourceFile**</span><span class="sxs-lookup"><span data-stu-id="03112-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="03112-165">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="03112-166">**SdbQueryDataExTagID**</span><span class="sxs-lookup"><span data-stu-id="03112-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="03112-167">**SDBQUERYRESULT**</span><span class="sxs-lookup"><span data-stu-id="03112-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="03112-168">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="03112-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="03112-169">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="03112-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="03112-170">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="03112-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="03112-171">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="03112-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="03112-172">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="03112-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="03112-173">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="03112-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="03112-174">**SdbReleaseDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="03112-175">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="03112-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="03112-176">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="03112-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="03112-177">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="03112-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="03112-178">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="03112-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="03112-179">**SdbTagToString**</span><span class="sxs-lookup"><span data-stu-id="03112-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="03112-180">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="03112-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="03112-181">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="03112-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="03112-182">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="03112-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="03112-183">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="03112-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="03112-184">**SdbWriteNULLTag**</span><span class="sxs-lookup"><span data-stu-id="03112-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="03112-185">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="03112-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="03112-186">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="03112-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="03112-187">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="03112-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="03112-188">**Tipi di database shim**</span><span class="sxs-lookup"><span data-stu-id="03112-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="03112-189">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="03112-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="03112-190">**TAG**</span><span class="sxs-lookup"><span data-stu-id="03112-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="03112-191">**Tipi di TAG**</span><span class="sxs-lookup"><span data-stu-id="03112-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="03112-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="03112-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="03112-193">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="03112-193">**TAGREF**</span></span>](tagref.md)

 

 



