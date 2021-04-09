---
description: L'argomento briciolo supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argomento BRICIOLo (ricerca di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128595"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="43edc-103">Argomento BRICIOLo (ricerca di Windows)</span><span class="sxs-lookup"><span data-stu-id="43edc-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="43edc-104">L' `crumb` argomento supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="43edc-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="43edc-105">Oltre a AQS ements, l' `crumb` argomento può assumere un parametro speciale `location` in Windows Vista e i `kind` `store` parametri e in XP, come descritto più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="43edc-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="43edc-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="43edc-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="43edc-107">Sintassi briciola</span><span class="sxs-lookup"><span data-stu-id="43edc-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="43edc-108">Esempi generali</span><span class="sxs-lookup"><span data-stu-id="43edc-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="43edc-109">Uso di briciole con vista (percorso)</span><span class="sxs-lookup"><span data-stu-id="43edc-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="43edc-110">Esempi di vista</span><span class="sxs-lookup"><span data-stu-id="43edc-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="43edc-111">Costanti per le cartelle comuni</span><span class="sxs-lookup"><span data-stu-id="43edc-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="43edc-112">Uso di briciole con Windows XP (Kind e Store)</span><span class="sxs-lookup"><span data-stu-id="43edc-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="43edc-113">Esempi di XP</span><span class="sxs-lookup"><span data-stu-id="43edc-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="43edc-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43edc-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="43edc-115">Sintassi briciola</span><span class="sxs-lookup"><span data-stu-id="43edc-115">Crumb Syntax</span></span>

<span data-ttu-id="43edc-116">La sintassi della briciola è la seguente:</span><span class="sxs-lookup"><span data-stu-id="43edc-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="43edc-117">La <column> parte è qualsiasi proprietà nel sistema di proprietà e il</span><span class="sxs-lookup"><span data-stu-id="43edc-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="43edc-118">parte è un valore valido per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="43edc-118">portion is a valid value for that property.</span></span> <span data-ttu-id="43edc-119">La <label> parte è un alias facoltativo per la proprietà visualizzata come hint dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="43edc-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="43edc-120">Esempi generali</span><span class="sxs-lookup"><span data-stu-id="43edc-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="43edc-121">Uso di briciole con vista (percorso)</span><span class="sxs-lookup"><span data-stu-id="43edc-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="43edc-122">Nel parametro briciola, Windows Vista supporta AQS completi e anche la `location` proprietà, che dispone di un'implementazione speciale disponibile solo in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="43edc-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="43edc-123">È possibile usare una stringa AQS o la `location` proprietà all'interno di un singolo parametro briciolo, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="43edc-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="43edc-124">Se il parametro briciolo include AQS, tutto il resto del parametro briciolo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="43edc-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="43edc-125">La `location` proprietà consente di specificare un percorso per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="43edc-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="43edc-126">Windows Vista può ignorare l'indicizzatore e attraversare la directory direttamente se il percorso è esterno all'ambito di ricerca per indicizzazione dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="43edc-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="43edc-127">Di conseguenza, queste ricerche possono risultare più lente delle ricerche che usano l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="43edc-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="43edc-128">Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:</span><span class="sxs-lookup"><span data-stu-id="43edc-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="43edc-129">Parametro</span><span class="sxs-lookup"><span data-stu-id="43edc-129">Parameter</span></span> | <span data-ttu-id="43edc-130">Valori</span><span class="sxs-lookup"><span data-stu-id="43edc-130">Values</span></span>                  | <span data-ttu-id="43edc-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43edc-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43edc-132">inclusione</span><span class="sxs-lookup"><span data-stu-id="43edc-132">inclusion</span></span> | <span data-ttu-id="43edc-133">Includi, Escludi</span><span class="sxs-lookup"><span data-stu-id="43edc-133">include, exclude</span></span>        | <span data-ttu-id="43edc-134">Specifica se la query deve includere o escludere elementi da tale percorso.</span><span class="sxs-lookup"><span data-stu-id="43edc-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="43edc-135">Il valore predefinito è "include".</span><span class="sxs-lookup"><span data-stu-id="43edc-135">"Include" is the default.</span></span> <span data-ttu-id="43edc-136">Windows Vista non supporta le esclusioni senza inclusioni.</span><span class="sxs-lookup"><span data-stu-id="43edc-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="43edc-137">(Vedere l'esempio)</span><span class="sxs-lookup"><span data-stu-id="43edc-137">(See example)</span></span> |
| <span data-ttu-id="43edc-138">ricorsione</span><span class="sxs-lookup"><span data-stu-id="43edc-138">recursion</span></span> | <span data-ttu-id="43edc-139">ricorsivo, non ricorsivo</span><span class="sxs-lookup"><span data-stu-id="43edc-139">recursive, nonrecursive</span></span> | <span data-ttu-id="43edc-140">Specifica se la ricerca deve rimaledire tutte le sottocartelle a partire dal valore definito nel percorso:</span><span class="sxs-lookup"><span data-stu-id="43edc-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="43edc-141">.</span><span class="sxs-lookup"><span data-stu-id="43edc-141">.</span></span> <span data-ttu-id="43edc-142">Il valore predefinito è "ricorsivo".</span><span class="sxs-lookup"><span data-stu-id="43edc-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="43edc-143">Per definire l'ambito di una ricerca usando il protocollo search-ms:, sono disponibili opzioni diverse a seconda della destinazione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="43edc-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="43edc-144">Cartella in un computer locale:</span><span class="sxs-lookup"><span data-stu-id="43edc-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="43edc-145">Usare AQS (briciole = Folder: <percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="43edc-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="43edc-146">Usare l'argomento location (briciole = location: <percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="43edc-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="43edc-147">Cartella in un computer remoto/rete:</span><span class="sxs-lookup"><span data-stu-id="43edc-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="43edc-148">Usare l'argomento location (briciole = location: <percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="43edc-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="43edc-149">Cartella a cui si accede tramite un gestore di protocollo UNC noto:</span><span class="sxs-lookup"><span data-stu-id="43edc-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="43edc-150">Usare AQS (briciole = Store: <UNC protocol handler name> )</span><span class="sxs-lookup"><span data-stu-id="43edc-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="43edc-151">Usare l'argomento location (briciole = location: <percorso con codifica URL>)</span><span class="sxs-lookup"><span data-stu-id="43edc-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="43edc-152">Esempi di vista</span><span class="sxs-lookup"><span data-stu-id="43edc-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="43edc-153">Nel primo esempio viene eseguita una ricerca di "Vacation" a partire dalla posizione shell://Personal (un collegamento speciale alla cartella documenti dell'utente), inclusa la cartella e tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="43edc-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="43edc-154">Vedere la tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="43edc-154">See table below.</span></span>

<span data-ttu-id="43edc-155">Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in c: \\ Immagini \\ duplicati.</span><span class="sxs-lookup"><span data-stu-id="43edc-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="43edc-156">Il terzo esempio esegue una ricerca all'interno di C: \\ Documents, limitato a file con la proprietà Kind impostata su pics.</span><span class="sxs-lookup"><span data-stu-id="43edc-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="43edc-157">Costanti per le cartelle comuni</span><span class="sxs-lookup"><span data-stu-id="43edc-157">Constants for Common Folders</span></span>

<span data-ttu-id="43edc-158">Windows Vista consente l'utilizzo di valori [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) che forniscono un metodo univoco indipendente dal sistema per identificare le cartelle speciali utilizzate spesso dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un determinato sistema.</span><span class="sxs-lookup"><span data-stu-id="43edc-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="43edc-159">Ad esempio, la cartella di sistema può essere "C: \\ Windows" in un sistema e "c: \\ WinNT" in un altro.</span><span class="sxs-lookup"><span data-stu-id="43edc-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="43edc-160">Prima di Windows Vista, venivano usati [CSIDL](/windows/desktop/shell/csidl) .</span><span class="sxs-lookup"><span data-stu-id="43edc-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="43edc-161">Usare questi percorsi con questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="43edc-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="43edc-162">Uso di briciole con Windows XP (Kind e Store)</span><span class="sxs-lookup"><span data-stu-id="43edc-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="43edc-163">Per la ricerca di Windows in Windows XP (WDS 3. x), i termini "Kind" e "Store" di AQS hanno un'implementazione speciale.</span><span class="sxs-lookup"><span data-stu-id="43edc-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="43edc-164">I valori "Kind" sono gli stessi [valori usati in WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md).</span><span class="sxs-lookup"><span data-stu-id="43edc-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="43edc-165">I valori "Store" includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="43edc-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="43edc-166">MAPI</span><span class="sxs-lookup"><span data-stu-id="43edc-166">mapi</span></span>
-   <span data-ttu-id="43edc-167">file</span><span class="sxs-lookup"><span data-stu-id="43edc-167">file</span></span>
-   <span data-ttu-id="43edc-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="43edc-168">outlookexpress</span></span>
-   <span data-ttu-id="43edc-169">any</span><span class="sxs-lookup"><span data-stu-id="43edc-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="43edc-170">Esempi di XP</span><span class="sxs-lookup"><span data-stu-id="43edc-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="43edc-171">Nel primo esempio vengono restituiti i messaggi di posta elettronica di Microsoft Outlook Express da John con l'etichetta personalizzata "OE Mail".</span><span class="sxs-lookup"><span data-stu-id="43edc-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="43edc-172">Nel secondo esempio viene eseguita una ricerca di qualsiasi comunicazione da John.</span><span class="sxs-lookup"><span data-stu-id="43edc-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43edc-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43edc-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43edc-174">Introduzione con argomenti di Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="43edc-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="43edc-175">Argomenti dell'identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="43edc-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="43edc-176">Argomento della sintassi</span><span class="sxs-lookup"><span data-stu-id="43edc-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="43edc-177">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="43edc-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="43edc-178">Argomento SOTTOQUERY</span><span class="sxs-lookup"><span data-stu-id="43edc-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
