---
description: In questa sezione vengono descritte le funzioni di gestione dei percorsi della shell di Windows. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.
title: Funzioni di gestione del percorso della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995072"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="8230f-104">Funzioni di gestione del percorso della shell</span><span class="sxs-lookup"><span data-stu-id="8230f-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="8230f-105">In questa sezione vengono descritte le funzioni di gestione dei percorsi della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="8230f-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="8230f-106">Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="8230f-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8230f-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8230f-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8230f-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="8230f-108">Topic</span></span></th>
<th><span data-ttu-id="8230f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8230f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8230f-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-111">Aggiunge una barra rovesciata alla fine di una stringa per creare la sintassi corretta per un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="8230f-112">Se il percorso di origine dispone già di una barra rovesciata finale, non verrà aggiunta alcuna barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="8230f-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-113">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-114">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-116">Aggiunge un'estensione del nome di file a una stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-117">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-118">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-120">Accoda un percorso alla fine di un altro.</span><span class="sxs-lookup"><span data-stu-id="8230f-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-121">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-122">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-124">Crea un percorso radice da un numero di unità specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-126">Semplifica un percorso rimuovendo gli elementi di navigazione, ad esempio &quot; . &quot; e &quot; .. &quot; , per produrre un percorso diretto e ben formato.</span><span class="sxs-lookup"><span data-stu-id="8230f-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-128">Concatena due stringhe che rappresentano i percorsi correttamente formattati in un unico percorso. concatena inoltre tutti gli elementi del percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="8230f-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-129">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-130">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-132">Confronta due percorsi per determinare se condividono un prefisso comune.</span><span class="sxs-lookup"><span data-stu-id="8230f-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="8230f-133">Un prefisso è uno dei seguenti tipi: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; \\ &quot; ...</span><span class="sxs-lookup"><span data-stu-id="8230f-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-135">Tronca un percorso di file per adattarsi alla larghezza di un determinato pixel sostituendo i componenti del percorso con ellissi.</span><span class="sxs-lookup"><span data-stu-id="8230f-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-137">Tronca un percorso per adattarsi a un certo numero di caratteri sostituendo i componenti del percorso con ellissi.</span><span class="sxs-lookup"><span data-stu-id="8230f-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-139">Converte un URL di file in un percorso Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="8230f-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-141">Crea un percorso da un URL di file.</span><span class="sxs-lookup"><span data-stu-id="8230f-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-143">Determina se il percorso di un oggetto file system, ad esempio un file o una cartella, è valido.</span><span class="sxs-lookup"><span data-stu-id="8230f-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-145">Cerca un'estensione in un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-147">Cerca un nome file in un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-149">Analizza un percorso e restituisce la parte del percorso che segue la prima barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="8230f-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-151">Cerca un file.</span><span class="sxs-lookup"><span data-stu-id="8230f-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-153">Determina se un nome file specificato presenta uno degli elenchi di suffissi.</span><span class="sxs-lookup"><span data-stu-id="8230f-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-155">Trova gli argomenti della riga di comando all'interno di un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-157">Determina il tipo di carattere in relazione a un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-159">Cerca in un percorso una lettera di unità compresa nell'intervallo tra' A ' è Z ' e restituisce il numero di unità corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8230f-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-161">Determina se il tipo di contenuto registrato di un file corrisponde al tipo di contenuto specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="8230f-162">Questa funzione ottiene il tipo di contenuto per il tipo di file specificato e confronta tale stringa con <em>pszContentType</em>.</span><span class="sxs-lookup"><span data-stu-id="8230f-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="8230f-163">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8230f-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-165">Verifica che un percorso sia una directory valida.</span><span class="sxs-lookup"><span data-stu-id="8230f-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-167">Determina se un percorso specificato è una directory vuota.</span><span class="sxs-lookup"><span data-stu-id="8230f-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-169">Cerca in un percorso eventuali caratteri di delimitazione del percorso (ad esempio,':' o ' \' ).</span><span class="sxs-lookup"><span data-stu-id="8230f-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="8230f-170">Se non sono presenti caratteri di delimitazione del percorso, il percorso viene considerato un percorso di specifica del file.</span><span class="sxs-lookup"><span data-stu-id="8230f-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-172">Determina se un file è un file HTML.</span><span class="sxs-lookup"><span data-stu-id="8230f-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="8230f-173">La determinazione viene eseguita in base al tipo di contenuto registrato per l'estensione del file.</span><span class="sxs-lookup"><span data-stu-id="8230f-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-175">Determina se un nome di file è nel formato lungo.</span><span class="sxs-lookup"><span data-stu-id="8230f-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-177">Determina se una stringa di percorso rappresenta una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="8230f-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-179">Cerca un percorso per determinare se contiene un prefisso valido del tipo passato da <em>pszPrefix</em>.</span><span class="sxs-lookup"><span data-stu-id="8230f-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="8230f-180">Un prefisso è uno dei seguenti tipi: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; \\ &quot; ...</span><span class="sxs-lookup"><span data-stu-id="8230f-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-182">Cerca un percorso e determina se è relativo.</span><span class="sxs-lookup"><span data-stu-id="8230f-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-184">Determina se una stringa di percorso fa riferimento alla radice di un volume.</span><span class="sxs-lookup"><span data-stu-id="8230f-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-186">Confronta due percorsi per determinare se hanno un componente radice comune.</span><span class="sxs-lookup"><span data-stu-id="8230f-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-188">Determina se una cartella esistente contiene gli attributi che lo rendono una cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="8230f-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="8230f-189">In alternativa, questa funzione indica se determinati attributi qualificano una cartella come cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="8230f-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-191">Determina se una stringa di percorso è un percorso UNC (Universal Naming Convention) valido, anziché un percorso basato su una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="8230f-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-193">Determina se una stringa è un UNC valido solo per un percorso server.</span><span class="sxs-lookup"><span data-stu-id="8230f-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-195">Determina se una stringa è un percorso di condivisione UNC valido, ovvero una \\ <em></em> \ <em>condivisione</em>server.</span><span class="sxs-lookup"><span data-stu-id="8230f-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-197">Verifica una determinata stringa per determinare se è conforme a un formato di URL valido.</span><span class="sxs-lookup"><span data-stu-id="8230f-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-199">Converte un percorso all-maiuscolo in tutti i caratteri minuscoli per fornire al percorso un aspetto coerente.</span><span class="sxs-lookup"><span data-stu-id="8230f-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-201">Assegna a una cartella esistente gli attributi appropriati che diventano una cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="8230f-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-203">Cerca una stringa usando un tipo di corrispondenza con caratteri jolly MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="8230f-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-205">Corrisponde a un nome file da un percorso rispetto a uno o più modelli di nome file.</span><span class="sxs-lookup"><span data-stu-id="8230f-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-207">Analizza una stringa del percorso del file che contiene un percorso di file e un indice di icona e restituisce valori distinti.</span><span class="sxs-lookup"><span data-stu-id="8230f-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-209">Cerca gli spazi in un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-209">Searches a path for spaces.</span></span> <span data-ttu-id="8230f-210">Se vengono trovati spazi, l'intero percorso è racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="8230f-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-212">Crea un percorso relativo da un file o una cartella a un altro.</span><span class="sxs-lookup"><span data-stu-id="8230f-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-214">Rimuove tutti gli argomenti da un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-216">Rimuove la barra rovesciata finale da un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-217">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8230f-217">This function is deprecated.</span></span> <span data-ttu-id="8230f-218">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-220">Rimuove tutti gli spazi iniziali e finali da una stringa.</span><span class="sxs-lookup"><span data-stu-id="8230f-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-222">Rimuove l'estensione del nome file da un percorso, se presente.</span><span class="sxs-lookup"><span data-stu-id="8230f-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-223">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8230f-223">This function is deprecated.</span></span> <span data-ttu-id="8230f-224">Si consiglia di usare <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-226">Rimuove il nome del file finale e la barra rovesciata da un percorso, se presenti.</span><span class="sxs-lookup"><span data-stu-id="8230f-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-227">Questa funzione è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8230f-227">This function is deprecated.</span></span> <span data-ttu-id="8230f-228">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-230">Sostituisce l'estensione di un nome file con una nuova estensione.</span><span class="sxs-lookup"><span data-stu-id="8230f-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="8230f-231">Se il nome file non contiene un'estensione, l'estensione verrà allegata alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="8230f-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-232">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-233">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-235">Determina se un percorso specificato è formattato correttamente e completo.</span><span class="sxs-lookup"><span data-stu-id="8230f-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-237">Imposta il testo di un controllo figlio in una finestra o in una finestra di dialogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> per garantire che il percorso corrisponda al controllo.</span><span class="sxs-lookup"><span data-stu-id="8230f-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-239">Recupera un puntatore al primo carattere in un percorso che segue la lettera di unità o gli elementi del percorso di condivisione o del server UNC.</span><span class="sxs-lookup"><span data-stu-id="8230f-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-241">Rimuove la parte del percorso di un percorso e un file completi.</span><span class="sxs-lookup"><span data-stu-id="8230f-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-243">Rimuove tutti gli elementi di file e directory in un percorso tranne le informazioni radice.</span><span class="sxs-lookup"><span data-stu-id="8230f-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8230f-244">Un uso improprio di questa funzione può causare un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="8230f-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="8230f-245">È consigliabile usare la funzione <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> più sicura al suo posto.</span><span class="sxs-lookup"><span data-stu-id="8230f-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-247">Rimuove la decorazione da una stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-249">Sostituisce determinati nomi di cartella in un percorso completo con la relativa stringa di ambiente associata.</span><span class="sxs-lookup"><span data-stu-id="8230f-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-251">Rimuove gli attributi da una cartella che lo rende una cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="8230f-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="8230f-252">Questa cartella deve esistere effettivamente nella file system.</span><span class="sxs-lookup"><span data-stu-id="8230f-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-254">Rimuove le virgolette dall'inizio e dalla fine di un percorso.</span><span class="sxs-lookup"><span data-stu-id="8230f-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-256">Controlla un contesto di associazione per verificare se è sicuro eseguire un'associazione a un particolare oggetto componente.</span><span class="sxs-lookup"><span data-stu-id="8230f-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-258">Determina uno schema per una stringa URL specificata e restituisce una stringa con un prefisso appropriato.</span><span class="sxs-lookup"><span data-stu-id="8230f-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-260">Converte una stringa dell'URL in forma canonica.</span><span class="sxs-lookup"><span data-stu-id="8230f-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-262">Se fornito con un URL relativo e la relativa base, restituisce un URL in formato canonico.</span><span class="sxs-lookup"><span data-stu-id="8230f-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-264">Esegue un confronto con distinzione tra maiuscole e minuscole di due stringhe URL.</span><span class="sxs-lookup"><span data-stu-id="8230f-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-266">Converte un percorso MS-DOS in un URL canonico.</span><span class="sxs-lookup"><span data-stu-id="8230f-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-268">Converte i caratteri o le coppie di surrogati in un URL che può essere modificato durante il trasporto su Internet ( &quot; caratteri non sicuri &quot; ) nelle corrispondenti sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="8230f-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="8230f-269">Le coppie di surrogati sono caratteri compresi tra U + 10000 e U + 10FFFF (in UTF-32) o tra DC00 e DFFF (in UTF-16).</span><span class="sxs-lookup"><span data-stu-id="8230f-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-271">Una macro che converte i caratteri spazio nella sequenza di escape corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8230f-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-273">Recupera il percorso da un URL.</span><span class="sxs-lookup"><span data-stu-id="8230f-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-275">Accetta una stringa URL e restituisce una parte specificata di tale URL.</span><span class="sxs-lookup"><span data-stu-id="8230f-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-277">Viene eseguito l'hashing di una stringa URL.</span><span class="sxs-lookup"><span data-stu-id="8230f-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-279">Verifica se un URL è un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="8230f-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-281">Verifica un URL per determinare se si tratta di un URL di file.</span><span class="sxs-lookup"><span data-stu-id="8230f-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-283">Restituisce un valore che indica se un URL è un URL che in genere non include nei browser la cronologia di navigazione.</span><span class="sxs-lookup"><span data-stu-id="8230f-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-285">Restituisce un valore che indica se un URL è opaco.</span><span class="sxs-lookup"><span data-stu-id="8230f-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8230f-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-287">Converte le sequenze di escape in caratteri normali.</span><span class="sxs-lookup"><span data-stu-id="8230f-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8230f-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="8230f-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="8230f-289">Converte le sequenze di escape in caratteri ordinari e sovrascrive la stringa originale.</span><span class="sxs-lookup"><span data-stu-id="8230f-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




