---
description: "La ricerca: il protocollo applicativo è una convenzione estendibile per chiamare l'applicazione di ricerca desktop in Windows Vista con Service Pack 1 (SP1) e versioni successive."
title: Uso del protocollo di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995029"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="15f18-103">Uso del protocollo di ricerca</span><span class="sxs-lookup"><span data-stu-id="15f18-103">Using the search Protocol</span></span>

<span data-ttu-id="15f18-104">La **ricerca:** il [protocollo applicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) è una convenzione estendibile per chiamare l'applicazione di ricerca desktop in Windows Vista con Service Pack 1 (SP1) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="15f18-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="15f18-105">Il protocollo è stato creato in Windows Vista con SP1 (per informazioni, vedere la panoramica dell'articolo della Knowledge Base relativo alle [modifiche di ricerca desktop di Windows Vista in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) per consentire a Windows di determinare e chiamare l'applicazione di ricerca desktop predefinita.</span><span class="sxs-lookup"><span data-stu-id="15f18-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="15f18-106">La sintassi del protocollo fornisce una serie di parametri utili per eseguire ricerche comuni sui desktop, ad esempio i termini di ricerca immessi dall'utente o il percorso in cui è stata avviata la ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="15f18-107">Quando gli utenti effettuano la ricerca da uno dei due punti di ingresso di ricerca disponibili, ovvero dal menu **Start** o da Esplora risorse, il sistema operativo usa il protocollo di ricerca per avviare l'applicazione di ricerca desktop predefinita.</span><span class="sxs-lookup"><span data-stu-id="15f18-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="15f18-108">Questa operazione viene eseguita aggiungendo i termini di ricerca immessi dall'utente alla sintassi del protocollo di ricerca standard e passando le informazioni all'applicazione registrata come applicazione di ricerca predefinita.</span><span class="sxs-lookup"><span data-stu-id="15f18-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="15f18-109">Se non sono installate altre applicazioni di ricerca desktop, una ricerca immessa in questi punti di ingresso avvia Esplora ricerche di Windows.</span><span class="sxs-lookup"><span data-stu-id="15f18-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="15f18-110">Tuttavia, gli sviluppatori di terze parti possono creare, installare e registrare le proprie applicazioni per gestire il protocollo di ricerca e l'applicazione di ricerca predefinita.</span><span class="sxs-lookup"><span data-stu-id="15f18-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="15f18-111">Tali applicazioni devono supportare la sintassi del protocollo di ricerca ed eseguire la registrazione con la funzionalità [programmi predefiniti](default-programs.md) per garantire un'esperienza senza problemi con Windows.</span><span class="sxs-lookup"><span data-stu-id="15f18-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="15f18-112">Se si sviluppa un'applicazione destinata all'utilizzo o alla compilazione di un'applicazione di ricerca desktop specifica, è consigliabile non basarsi esclusivamente sul protocollo **Search:** .</span><span class="sxs-lookup"><span data-stu-id="15f18-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="15f18-113">Poiché molte applicazioni possono essere proprietarie del protocollo **Search:** , non c'è alcuna garanzia che l'applicazione di ricerca desktop di destinazione ne sarà proprietaria in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="15f18-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="15f18-114">È invece consigliabile usare un protocollo di ricerca privato definito da tale applicazione di ricerca desktop di destinazione.</span><span class="sxs-lookup"><span data-stu-id="15f18-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="15f18-115">Ciò significa che le applicazioni di ricerca desktop destinate a essere una piattaforma per le applicazioni di terze parti devono supportare sia il protocollo **Search:** che il protocollo di ricerca proprietario.</span><span class="sxs-lookup"><span data-stu-id="15f18-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="15f18-116">Il protocollo **Search:** non sostituisce il protocollo di [ricerca proprietario-MS:](../search/-search-3x-wds-qryidx-searchms.md) .</span><span class="sxs-lookup"><span data-stu-id="15f18-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="15f18-117">Le applicazioni possono comunque usare il protocollo **search-ms:** per avviare Esplora ricerche finestre o per eseguire una query in modo invisibile all'indicizzatore di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="15f18-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="15f18-118">Questo argomento illustra quanto segue:</span><span class="sxs-lookup"><span data-stu-id="15f18-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="15f18-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15f18-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="15f18-120">Windows Vista con SP1 utilizzo del protocollo di ricerca:</span><span class="sxs-lookup"><span data-stu-id="15f18-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="15f18-121">esempi</span><span class="sxs-lookup"><span data-stu-id="15f18-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="15f18-122">Registrazione dell'applicazione che gestisce il protocollo</span><span class="sxs-lookup"><span data-stu-id="15f18-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="15f18-123">Voci del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="15f18-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="15f18-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15f18-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="15f18-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15f18-125">Syntax</span></span>

<span data-ttu-id="15f18-126">Il protocollo di ricerca usa la sintassi standard codificata con URL seguente:</span><span class="sxs-lookup"><span data-stu-id="15f18-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="15f18-127">La sintassi inizia identificando il protocollo stesso (**Search:**).</span><span class="sxs-lookup"><span data-stu-id="15f18-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="15f18-128">Le coppie parametro/valore sono argomenti passati al motore di ricerca, come descritto nella tabella seguente, che Mostra tutti i parametri possibili per la sintassi del protocollo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="15f18-129">Parametro</span><span class="sxs-lookup"><span data-stu-id="15f18-129">Parameter</span></span>                                              | <span data-ttu-id="15f18-130">Valore</span><span class="sxs-lookup"><span data-stu-id="15f18-130">Value</span></span>                                                         | <span data-ttu-id="15f18-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15f18-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f18-132">query</span><span class="sxs-lookup"><span data-stu-id="15f18-132">query</span></span>                                                  | <span data-ttu-id="15f18-133">Testo con codifica URL</span><span class="sxs-lookup"><span data-stu-id="15f18-133">URL-encoded text</span></span>                                              | <span data-ttu-id="15f18-134">Testo della query immesso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="15f18-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="15f18-135">InputLocale</span><span class="sxs-lookup"><span data-stu-id="15f18-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="15f18-136">Qualsiasi identificatore di codice lingua (LCID) valido</span><span class="sxs-lookup"><span data-stu-id="15f18-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="15f18-137">Identificatore LCID che identifica la lingua di input per la query.</span><span class="sxs-lookup"><span data-stu-id="15f18-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="15f18-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="15f18-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="15f18-139">Qualsiasi LCID valido</span><span class="sxs-lookup"><span data-stu-id="15f18-139">Any valid LCID</span></span>                                                | <span data-ttu-id="15f18-140">Identificatore LCID che identifica la lingua della versione internazionale dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="15f18-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="15f18-141">Il valore predefinito è 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="15f18-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="15f18-142">navigazione</span><span class="sxs-lookup"><span data-stu-id="15f18-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="15f18-143">AQS-istruzione</span><span class="sxs-lookup"><span data-stu-id="15f18-143">AQS statement</span></span>                                                 | <span data-ttu-id="15f18-144">Questo argomento limita l'ambito di ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="15f18-145">In Windows Vista il protocollo di ricerca supporta AQS completi e un'implementazione speciale per un `location` argomento.</span><span class="sxs-lookup"><span data-stu-id="15f18-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="15f18-146">In Windows XP il protocollo di ricerca supporta anche AQS completi, ad eccezione di una speciale implementazione di `kind` e `store` .</span><span class="sxs-lookup"><span data-stu-id="15f18-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="15f18-147">sintassi</span><span class="sxs-lookup"><span data-stu-id="15f18-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="15f18-148">NQS, AQS (senza distinzione tra maiuscole e minuscole)</span><span class="sxs-lookup"><span data-stu-id="15f18-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="15f18-149">Sintassi di query da utilizzare per la ricerca nell'indice: la sintassi di query naturale o la sintassi di query avanzata (AQS).</span><span class="sxs-lookup"><span data-stu-id="15f18-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="15f18-150">AQS è l'impostazione predefinita e viene sempre utilizzata come analizzata e supportata.</span><span class="sxs-lookup"><span data-stu-id="15f18-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="15f18-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="15f18-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="15f18-152">Qualsiasi proprietà valida del sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="15f18-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="15f18-153">Proprietà che specifica la colonna in base alla quale eseguire lo stack dei risultati.</span><span class="sxs-lookup"><span data-stu-id="15f18-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="15f18-154">subquery</span><span class="sxs-lookup"><span data-stu-id="15f18-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="15f18-155">Percorso specificato completamente per un file di ricerca salvato ( \* . search-ms)</span><span class="sxs-lookup"><span data-stu-id="15f18-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="15f18-156">I risultati della sottoquery vengono utilizzati come origine per la query.</span><span class="sxs-lookup"><span data-stu-id="15f18-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="15f18-157">Ovvero i termini della query vengono cercati in base ai risultati della sottoquery.</span><span class="sxs-lookup"><span data-stu-id="15f18-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="15f18-158">displayname</span><span class="sxs-lookup"><span data-stu-id="15f18-158">displayname</span></span>                                            | <span data-ttu-id="15f18-159">Stringa con codifica URL</span><span class="sxs-lookup"><span data-stu-id="15f18-159">URL-encoded string</span></span>                                            | <span data-ttu-id="15f18-160">Nome della ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="15f18-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="15f18-161">Windows Vista con SP1 utilizzo del protocollo di ricerca:</span><span class="sxs-lookup"><span data-stu-id="15f18-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="15f18-162">Windows Vista con SP1 include diversi punti di ingresso da cui viene chiamato il protocollo **Search:** .</span><span class="sxs-lookup"><span data-stu-id="15f18-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="15f18-163">Questi punti di ingresso sono descritti sotto, oltre alla sintassi comune associata a ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="15f18-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="15f18-164">Cerca punto di ingresso del protocollo</span><span class="sxs-lookup"><span data-stu-id="15f18-164">Search protocol entry point</span></span> | <span data-ttu-id="15f18-165">Location</span><span class="sxs-lookup"><span data-stu-id="15f18-165">Location</span></span>         | <span data-ttu-id="15f18-166">Query chiamata</span><span class="sxs-lookup"><span data-stu-id="15f18-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="15f18-167">**Cerca in tutto il mondo**</span><span class="sxs-lookup"><span data-stu-id="15f18-167">**Search Everywhere**</span></span>       | <span data-ttu-id="15f18-168">Menu **Start**</span><span class="sxs-lookup"><span data-stu-id="15f18-168">**Start** menu</span></span>   | <span data-ttu-id="15f18-169">ricerca: query = *termine di ricerca*<></span><span class="sxs-lookup"><span data-stu-id="15f18-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="15f18-170">**Cerca in tutto il mondo**</span><span class="sxs-lookup"><span data-stu-id="15f18-170">**Search Everywhere**</span></span>       | <span data-ttu-id="15f18-171">Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="15f18-171">Windows Explorer</span></span> | <span data-ttu-id="15f18-172">ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*></span><span class="sxs-lookup"><span data-stu-id="15f18-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="15f18-173">Tasto logo Windows+F</span><span class="sxs-lookup"><span data-stu-id="15f18-173">Windows logo key+F</span></span>          | <span data-ttu-id="15f18-174">Ovunque</span><span class="sxs-lookup"><span data-stu-id="15f18-174">Anywhere</span></span>         | <span data-ttu-id="15f18-175">ricerca</span><span class="sxs-lookup"><span data-stu-id="15f18-175">search:</span></span>                                                              |
| <span data-ttu-id="15f18-176">CTRL+F</span><span class="sxs-lookup"><span data-stu-id="15f18-176">CTRL+F</span></span>                      | <span data-ttu-id="15f18-177">Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="15f18-177">Windows Explorer</span></span> | <span data-ttu-id="15f18-178">ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*></span><span class="sxs-lookup"><span data-stu-id="15f18-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="15f18-179">F3</span><span class="sxs-lookup"><span data-stu-id="15f18-179">F3</span></span>                          | <span data-ttu-id="15f18-180">Menu **Start**</span><span class="sxs-lookup"><span data-stu-id="15f18-180">**Start** menu</span></span>   | <span data-ttu-id="15f18-181">ricerca</span><span class="sxs-lookup"><span data-stu-id="15f18-181">search:</span></span>                                                              |
| <span data-ttu-id="15f18-182">F3</span><span class="sxs-lookup"><span data-stu-id="15f18-182">F3</span></span>                          | <span data-ttu-id="15f18-183">Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="15f18-183">Windows Explorer</span></span> | <span data-ttu-id="15f18-184">ricerca: query =<*termine di ricerca*>&briciolo = posizione: <*località*></span><span class="sxs-lookup"><span data-stu-id="15f18-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="15f18-185">I punti di ingresso del protocollo di ricerca di Windows Vista con SP1 non sfruttano tutti i possibili parametri nel protocollo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="15f18-186">Le applicazioni che riguardano solo la gestione delle chiamate del protocollo di ricerca da Windows Vista con SP1 possono utilizzare la tabella seguente come guida al valore minimo necessario per l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="15f18-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="15f18-187">Parametro</span><span class="sxs-lookup"><span data-stu-id="15f18-187">Parameter</span></span>                                              | <span data-ttu-id="15f18-188">Usato da Windows?</span><span class="sxs-lookup"><span data-stu-id="15f18-188">Used by Windows?</span></span> | <span data-ttu-id="15f18-189">Modalità di utilizzo di Windows Vista con SP1 durante la chiamata alla ricerca:</span><span class="sxs-lookup"><span data-stu-id="15f18-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f18-190">query</span><span class="sxs-lookup"><span data-stu-id="15f18-190">query</span></span>                                                  | <span data-ttu-id="15f18-191">Sì</span><span class="sxs-lookup"><span data-stu-id="15f18-191">Yes</span></span>              | <span data-ttu-id="15f18-192">Testo della query immesso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="15f18-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="15f18-193">navigazione</span><span class="sxs-lookup"><span data-stu-id="15f18-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="15f18-194">Sì</span><span class="sxs-lookup"><span data-stu-id="15f18-194">Yes</span></span>              | <span data-ttu-id="15f18-195">[briciola](search-protocol-crumb.md) usa l' `location` argomento per specificare da dove proviene la query.</span><span class="sxs-lookup"><span data-stu-id="15f18-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="15f18-196">subquery</span><span class="sxs-lookup"><span data-stu-id="15f18-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="15f18-197">Sì</span><span class="sxs-lookup"><span data-stu-id="15f18-197">Yes</span></span>              | <span data-ttu-id="15f18-198">I risultati dell'argomento [sottoquery](search-protocol-subquery.md) vengono utilizzati come ambito degli elementi in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="15f18-199">Questa operazione viene in genere usata se un utente usa un file. search-ms per eseguire la ricerca e quindi chiama l'applicazione di ricerca desktop predefinita dall'interno di tale ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="15f18-200">InputLocale</span><span class="sxs-lookup"><span data-stu-id="15f18-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="15f18-201">No</span><span class="sxs-lookup"><span data-stu-id="15f18-201">No</span></span>               | <span data-ttu-id="15f18-202">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15f18-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="15f18-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="15f18-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="15f18-204">No</span><span class="sxs-lookup"><span data-stu-id="15f18-204">No</span></span>               | <span data-ttu-id="15f18-205">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15f18-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="15f18-206">sintassi</span><span class="sxs-lookup"><span data-stu-id="15f18-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="15f18-207">No</span><span class="sxs-lookup"><span data-stu-id="15f18-207">No</span></span>               | <span data-ttu-id="15f18-208">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15f18-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="15f18-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="15f18-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="15f18-210">No</span><span class="sxs-lookup"><span data-stu-id="15f18-210">No</span></span>               | <span data-ttu-id="15f18-211">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15f18-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="15f18-212">displayname</span><span class="sxs-lookup"><span data-stu-id="15f18-212">displayname</span></span>                                            | <span data-ttu-id="15f18-213">No</span><span class="sxs-lookup"><span data-stu-id="15f18-213">No</span></span>               | <span data-ttu-id="15f18-214">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15f18-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="15f18-215">Esempio</span><span class="sxs-lookup"><span data-stu-id="15f18-215">Examples</span></span>

<span data-ttu-id="15f18-216">Se un utente immette "Microsoft" nel menu **Start** e fa clic su **Cerca ovunque**, viene effettuata la chiamata al protocollo di ricerca risultante:</span><span class="sxs-lookup"><span data-stu-id="15f18-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="15f18-217">Se un utente immette "Seattle" in Esplora risorse all'interno di C: \\ cartella e quindi fa clic su **Cerca ovunque**, viene eseguita la chiamata seguente, usando i caratteri di escape per ":" e " \\ ":</span><span class="sxs-lookup"><span data-stu-id="15f18-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="15f18-218">Registrazione dell'applicazione che gestisce il protocollo</span><span class="sxs-lookup"><span data-stu-id="15f18-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="15f18-219">Poiché più applicazioni possono sostenere il protocollo di ricerca, è necessario registrare l'applicazione con la funzionalità [programmi predefiniti](default-programs.md) durante l'installazione per consentire all'utente di configurare più facilmente il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="15f18-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="15f18-220">Oltre alle procedure di installazione normalmente disponibili in Windows XP, un'applicazione basata su Windows Vista deve eseguire la registrazione con la funzionalità programmi predefiniti, in modo che l'applicazione e gli utenti possano configurare facilmente le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="15f18-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="15f18-221">Dopo aver installato i file binari necessari nel computer dell'utente, la routine di installazione deve completare le attività generali seguenti:</span><span class="sxs-lookup"><span data-stu-id="15f18-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="15f18-222">Scrivere i ProgID nel **\_ \_ computer locale HKEY**, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="15f18-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="15f18-223">Si noti che le applicazioni devono creare ProgID specifici dell'applicazione per il protocollo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="15f18-224">Associazione del protocollo di ricerca a livello di computer Claim.</span><span class="sxs-lookup"><span data-stu-id="15f18-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="15f18-225">Registrare l'applicazione con i [programmi predefiniti](default-programs.md), come illustrato in [registrazione di un'applicazione per l'utilizzo con i programmi predefiniti](default-programs.md), come un contendente per il protocollo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="15f18-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="15f18-226">Voci del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="15f18-226">Registry Entries</span></span>

<span data-ttu-id="15f18-227">Di seguito sono riportati alcuni esempi delle voci del registro di sistema necessarie per un'applicazione di ricerca desktop fittizia, contoso search.</span><span class="sxs-lookup"><span data-stu-id="15f18-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="15f18-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15f18-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15f18-229">Sintassi di ricerca avanzata</span><span class="sxs-lookup"><span data-stu-id="15f18-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="15f18-230">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="15f18-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
