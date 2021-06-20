---
description: Informazioni su come usare l'argomento CRUMB Windows Search come mezzo per controllare l'ambito di una ricerca.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argomento CRUMB (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403734"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="67c6c-103">Argomento CRUMB (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="67c6c-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="67c6c-104">L'argomento supporta istruzioni AQS (Advanced Query Syntax) complete ed è particolarmente utile per controllare `crumb` l'ambito di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="67c6c-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="67c6c-105">Oltre agli argomenti AQS, l'argomento può assumere un parametro speciale in Windows Vista e i parametri e in XP, come descritto `crumb` più avanti in questo `location` `kind` `store` argomento.</span><span class="sxs-lookup"><span data-stu-id="67c6c-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="67c6c-106">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="67c6c-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="67c6c-107">Sintassi crumb</span><span class="sxs-lookup"><span data-stu-id="67c6c-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="67c6c-108">Esempi generali</span><span class="sxs-lookup"><span data-stu-id="67c6c-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="67c6c-109">Uso di crumb con Vista (posizione)</span><span class="sxs-lookup"><span data-stu-id="67c6c-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="67c6c-110">Esempi di Vista</span><span class="sxs-lookup"><span data-stu-id="67c6c-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="67c6c-111">Costanti per cartelle comuni</span><span class="sxs-lookup"><span data-stu-id="67c6c-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="67c6c-112">Uso di crumb con Windows XP (tipo e archivio)</span><span class="sxs-lookup"><span data-stu-id="67c6c-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="67c6c-113">Esempi di XP</span><span class="sxs-lookup"><span data-stu-id="67c6c-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="67c6c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67c6c-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="67c6c-115">Sintassi crumb</span><span class="sxs-lookup"><span data-stu-id="67c6c-115">Crumb Syntax</span></span>

<span data-ttu-id="67c6c-116">La sintassi di base è la seguente:</span><span class="sxs-lookup"><span data-stu-id="67c6c-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="67c6c-117">La <column> parte è qualsiasi proprietà nel sistema di proprietà e</span><span class="sxs-lookup"><span data-stu-id="67c6c-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="67c6c-118">portion è un valore valido per tale proprietà.</span><span class="sxs-lookup"><span data-stu-id="67c6c-118">portion is a valid value for that property.</span></span> <span data-ttu-id="67c6c-119">La <label> parte è un alias facoltativo per la proprietà visualizzata come suggerimento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="67c6c-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="67c6c-120">Esempi generali</span><span class="sxs-lookup"><span data-stu-id="67c6c-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="67c6c-121">Uso di crumb con Vista (posizione)</span><span class="sxs-lookup"><span data-stu-id="67c6c-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="67c6c-122">Nel parametro crumb Windows Vista supporta AQS completo e anche la proprietà , che ha un'implementazione speciale `location` disponibile solo in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67c6c-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="67c6c-123">È possibile usare una stringa AQS o la proprietà `location` all'interno di un singolo parametro crumb, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="67c6c-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="67c6c-124">Se il parametro crumb include AQS, tutti gli altri elementi nel parametro crumb vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="67c6c-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="67c6c-125">La `location` proprietà consente di specificare un percorso in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="67c6c-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="67c6c-126">Windows Vista può ignorare l'indicizzatore e attraversare direttamente la directory se il percorso non rientra nell'ambito della ricerca per indicizzazione dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="67c6c-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="67c6c-127">Di conseguenza, queste ricerche possono essere più lente delle ricerche che usano l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="67c6c-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="67c6c-128">Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:</span><span class="sxs-lookup"><span data-stu-id="67c6c-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="67c6c-129">Parametro</span><span class="sxs-lookup"><span data-stu-id="67c6c-129">Parameter</span></span> | <span data-ttu-id="67c6c-130">Valori</span><span class="sxs-lookup"><span data-stu-id="67c6c-130">Values</span></span>                  | <span data-ttu-id="67c6c-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67c6c-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c6c-132">Inclusione</span><span class="sxs-lookup"><span data-stu-id="67c6c-132">inclusion</span></span> | <span data-ttu-id="67c6c-133">include, exclude</span><span class="sxs-lookup"><span data-stu-id="67c6c-133">include, exclude</span></span>        | <span data-ttu-id="67c6c-134">Specifica se la query deve includere o escludere elementi da tale percorso.</span><span class="sxs-lookup"><span data-stu-id="67c6c-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="67c6c-135">L'impostazione predefinita è "Include".</span><span class="sxs-lookup"><span data-stu-id="67c6c-135">"Include" is the default.</span></span> <span data-ttu-id="67c6c-136">Windows Vista non supporta le esclusioni senza inclusioni.</span><span class="sxs-lookup"><span data-stu-id="67c6c-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="67c6c-137">(Vedere l'esempio)</span><span class="sxs-lookup"><span data-stu-id="67c6c-137">(See example)</span></span> |
| <span data-ttu-id="67c6c-138">ricorsione</span><span class="sxs-lookup"><span data-stu-id="67c6c-138">recursion</span></span> | <span data-ttu-id="67c6c-139">ricorsivo, non ricorsivo</span><span class="sxs-lookup"><span data-stu-id="67c6c-139">recursive, nonrecursive</span></span> | <span data-ttu-id="67c6c-140">Specifica se la ricerca deve essere ricorsiva di tutte le sottocartelle a partire dal valore definito nel percorso:</span><span class="sxs-lookup"><span data-stu-id="67c6c-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="67c6c-141">.</span><span class="sxs-lookup"><span data-stu-id="67c6c-141">.</span></span> <span data-ttu-id="67c6c-142">L'impostazione predefinita è "Recursive".</span><span class="sxs-lookup"><span data-stu-id="67c6c-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="67c6c-143">Per impostare l'ambito di una ricerca usando il protocollo search-ms:, sono disponibili opzioni diverse a seconda della destinazione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="67c6c-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="67c6c-144">Cartella in un computer locale:</span><span class="sxs-lookup"><span data-stu-id="67c6c-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="67c6c-145">Usare AQS (crumb=folder:<percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="67c6c-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="67c6c-146">Usare l'argomento location (crumb=location:<percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="67c6c-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="67c6c-147">Cartella in un computer/rete remoto:</span><span class="sxs-lookup"><span data-stu-id="67c6c-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="67c6c-148">Usare l'argomento location (crumb=location:<percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="67c6c-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="67c6c-149">Cartella a cui si accede tramite un gestore di protocollo UNC noto:</span><span class="sxs-lookup"><span data-stu-id="67c6c-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="67c6c-150">Usare AQS (crumb=store: <UNC protocol handler name> )</span><span class="sxs-lookup"><span data-stu-id="67c6c-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="67c6c-151">Usare l'argomento location (crumb=location:<percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="67c6c-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="67c6c-152">Esempi di Vista</span><span class="sxs-lookup"><span data-stu-id="67c6c-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="67c6c-153">Nel primo esempio viene eseguita una ricerca di "vacation" a partire dal percorso shell://Personal (un collegamento speciale alla cartella Documenti dell'utente), incluse tale cartella e tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="67c6c-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="67c6c-154">Vedere la tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="67c6c-154">See table below.</span></span>

<span data-ttu-id="67c6c-155">Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in C: \\ Immagini \\ duplicate.</span><span class="sxs-lookup"><span data-stu-id="67c6c-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="67c6c-156">Il terzo esempio esegue una ricerca all'interno di C: Documenti, limitata ai file con la proprietà \\ kind impostata su pics.</span><span class="sxs-lookup"><span data-stu-id="67c6c-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="67c6c-157">Costanti per cartelle comuni</span><span class="sxs-lookup"><span data-stu-id="67c6c-157">Constants for Common Folders</span></span>

<span data-ttu-id="67c6c-158">Windows Vista consente l'uso di valori [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) che forniscono un modo univoco indipendente dal sistema per identificare le cartelle speciali usate di frequente dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="67c6c-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="67c6c-159">Ad esempio, la cartella di sistema può essere "C: Windows" in un \\ sistema e "C: \\ Winnt" in un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="67c6c-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="67c6c-160">Nelle versioni precedenti a Windows Vista [venivano usati i CSID.](/windows/desktop/shell/csidl)</span><span class="sxs-lookup"><span data-stu-id="67c6c-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="67c6c-161">Usare queste posizioni con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="67c6c-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="67c6c-162">Uso di crumb con Windows XP (tipo e archivio)</span><span class="sxs-lookup"><span data-stu-id="67c6c-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="67c6c-163">Per Windows Search in Windows XP (WDS 3.x), i termini "kind" e "store" di AQS hanno un'implementazione speciale.</span><span class="sxs-lookup"><span data-stu-id="67c6c-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="67c6c-164">I valori "kind" sono gli stessi [usati in WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md)</span><span class="sxs-lookup"><span data-stu-id="67c6c-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="67c6c-165">I valori "store" includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="67c6c-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="67c6c-166">Mapi</span><span class="sxs-lookup"><span data-stu-id="67c6c-166">mapi</span></span>
-   <span data-ttu-id="67c6c-167">file</span><span class="sxs-lookup"><span data-stu-id="67c6c-167">file</span></span>
-   <span data-ttu-id="67c6c-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="67c6c-168">outlookexpress</span></span>
-   <span data-ttu-id="67c6c-169">any</span><span class="sxs-lookup"><span data-stu-id="67c6c-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="67c6c-170">Esempi di XP</span><span class="sxs-lookup"><span data-stu-id="67c6c-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="67c6c-171">Nel primo esempio vengono restituiti messaggi di posta elettronica di Microsoft Outlook Express da John con l'etichetta personalizzata "OE Mail".</span><span class="sxs-lookup"><span data-stu-id="67c6c-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="67c6c-172">Nel secondo esempio viene eseguita una ricerca di qualsiasi comunicazione da John.</span><span class="sxs-lookup"><span data-stu-id="67c6c-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67c6c-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67c6c-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67c6c-174">Attività iniziali con Parameter-Value argomenti</span><span class="sxs-lookup"><span data-stu-id="67c6c-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="67c6c-175">Argomenti dell'identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="67c6c-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="67c6c-176">Argomento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67c6c-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="67c6c-177">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="67c6c-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="67c6c-178">Argomento SUBQUERY</span><span class="sxs-lookup"><span data-stu-id="67c6c-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
