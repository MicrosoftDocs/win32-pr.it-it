---
title: Chiamata di WDS dalla riga di comando
description: È possibile avviare l'interfaccia utente di ricerca desktop Microsoft Windows con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (BHO) usando la sintassi della riga di comando windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724020"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="b909c-103">Chiamata di WDS dalla riga di comando</span><span class="sxs-lookup"><span data-stu-id="b909c-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="b909c-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b909c-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b909c-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="b909c-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="b909c-106">È possibile avviare l'interfaccia utente di ricerca desktop Microsoft Windows con un filtro, un archivio e una query specifici da un'altra applicazione o da una pagina Web che usa l'oggetto browser helper (BHO) usando la sintassi della riga di comando windowssearch.exe.</span><span class="sxs-lookup"><span data-stu-id="b909c-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="b909c-107">Quando si chiama WDS dalla riga di comando, non vengono restituite informazioni sulle azioni dell'utente o sulla selezione nella finestra WDS nell'applicazione chiamante o nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="b909c-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="b909c-108">Il percorso di installazione di WDS è specificato nell'impostazione del registro di sistema InstallDir in HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="b909c-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="b909c-109">Il percorso predefinito in cui è installato windowssearch.exe è file di programma \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="b909c-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="b909c-110">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b909c-110">Command Line Syntax</span></span>

<span data-ttu-id="b909c-111">La sintassi seguente si applica all'interfaccia della riga di comando di Windows Desktop Search 2. x.</span><span class="sxs-lookup"><span data-stu-id="b909c-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b909c-112">Opzioni</span><span class="sxs-lookup"><span data-stu-id="b909c-112">Options</span></span></th>
<th><span data-ttu-id="b909c-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="b909c-113">Parameter</span></span></th>
<th><span data-ttu-id="b909c-114">Significato</span><span class="sxs-lookup"><span data-stu-id="b909c-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b909c-115">/Startup</span><span class="sxs-lookup"><span data-stu-id="b909c-115">/startup</span></span></td>

<td><span data-ttu-id="b909c-116">Inizializza la ricerca desktop di Windows</span><span class="sxs-lookup"><span data-stu-id="b909c-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b909c-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="b909c-117">/indexnow</span></span></td>

<td><span data-ttu-id="b909c-118">Disattiva l'indicizzazione e ripete l'analisi di tutte le posizioni degli indici</span><span class="sxs-lookup"><span data-stu-id="b909c-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b909c-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="b909c-119">/showstatus</span></span></td>

<td><span data-ttu-id="b909c-120">Mostra la finestra stato indicizzazione</span><span class="sxs-lookup"><span data-stu-id="b909c-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b909c-121">/launchsearchwindow o/URL</span><span class="sxs-lookup"><span data-stu-id="b909c-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="b909c-122">Apre una finestra di WDS con una query vuota</span><span class="sxs-lookup"><span data-stu-id="b909c-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b909c-123">/URL</span><span class="sxs-lookup"><span data-stu-id="b909c-123">/url</span></span></td>
<td><span data-ttu-id="b909c-124">ricerca: [Store | Show | query] stringa di query</span><span class="sxs-lookup"><span data-stu-id="b909c-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="b909c-125">Apre una finestra di WDS con una query e un filtro in base ai parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b909c-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="b909c-126">Store: specifica l'origine dati su cui eseguire la query: files, Outlook e outlookexpress.</span><span class="sxs-lookup"><span data-stu-id="b909c-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="b909c-127">Se non viene specificato, verranno cercati tutti gli archivi.</span><span class="sxs-lookup"><span data-stu-id="b909c-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="b909c-128">Sebbene la sintassi di query avanzata supporti il riferimento a Microsoft Outlook come ' oe ', il parametro Store nella riga di comando deve essere ' outlookexpress '.</span><span class="sxs-lookup"><span data-stu-id="b909c-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="b909c-129">Show-specifica il tipo di risultati percepito da restituire.</span><span class="sxs-lookup"><span data-stu-id="b909c-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="b909c-130">Vedere <a href="-search-2x-wds-perceivedtype.md">tipi percepiti</a> per un elenco completo di tipi.</span><span class="sxs-lookup"><span data-stu-id="b909c-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="b909c-131">Se non specificato, verranno restituiti tutti i tipi.</span><span class="sxs-lookup"><span data-stu-id="b909c-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="b909c-132">Esistono tre differenze tra i valori di tipo percepito e i valori per show.</span><span class="sxs-lookup"><span data-stu-id="b909c-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="b909c-133">Per <code>show</code> , usare ' Documents ' anziché' doc ',' Pictures ' anziché' Pics ' è textdocuments ' anziché' text '.</span><span class="sxs-lookup"><span data-stu-id="b909c-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="b909c-134">query: specifica i criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b909c-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="b909c-135">Questo valore supporta i parametri della <a href="-search-2x-wds-aqsreference.md">sintassi di query avanzati</a> per affinare i risultati.</span><span class="sxs-lookup"><span data-stu-id="b909c-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="b909c-136">Il parametro di query deve essere l'ultimo parametro nell'URL.</span><span class="sxs-lookup"><span data-stu-id="b909c-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="b909c-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="b909c-137">Example</span></span>

<span data-ttu-id="b909c-138">Per cercare, ad esempio, tutti i file per le immagini corrispondenti al criterio ' Wallpaper ', utilizzare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="b909c-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="b909c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b909c-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b909c-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b909c-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b909c-141">Sintassi di ricerca avanzata</span><span class="sxs-lookup"><span data-stu-id="b909c-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="b909c-142">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="b909c-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="b909c-143">Chiamata di WDS da pagine Web</span><span class="sxs-lookup"><span data-stu-id="b909c-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





