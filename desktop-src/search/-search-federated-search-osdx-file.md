---
description: Viene descritto come creare un file di descrizione OpenSearch (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il protocollo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966536"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="9cb8e-103">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="9cb8e-104">Viene descritto come creare un file di descrizione OpenSearch (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il protocollo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="9cb8e-105">La ricerca federata consente agli utenti di eseguire ricerche in un archivio dati remoto e di visualizzare i risultati da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="9cb8e-106">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9cb8e-107">File di descrizione OpenSearch</span><span class="sxs-lookup"><span data-stu-id="9cb8e-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="9cb8e-108">Minima elementi figlio obbligatori</span><span class="sxs-lookup"><span data-stu-id="9cb8e-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="9cb8e-109">Elementi standard in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="9cb8e-110">Nome breve</span><span class="sxs-lookup"><span data-stu-id="9cb8e-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="9cb8e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cb8e-111">Description</span></span>](#description)
    -   [<span data-ttu-id="9cb8e-112">Modello di URL per i risultati RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="9cb8e-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="9cb8e-113">Modello di URL per i risultati Web</span><span class="sxs-lookup"><span data-stu-id="9cb8e-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="9cb8e-114">Parametri del modello URL</span><span class="sxs-lookup"><span data-stu-id="9cb8e-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="9cb8e-115">Risultati di paging</span><span class="sxs-lookup"><span data-stu-id="9cb8e-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="9cb8e-116">Paging mediante l'indice dell'elemento</span><span class="sxs-lookup"><span data-stu-id="9cb8e-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="9cb8e-117">Paging tramite l'indice della pagina</span><span class="sxs-lookup"><span data-stu-id="9cb8e-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="9cb8e-118">Dimensioni pagina</span><span class="sxs-lookup"><span data-stu-id="9cb8e-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="9cb8e-119">Elementi estesi in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="9cb8e-120">Numero massimo di risultati</span><span class="sxs-lookup"><span data-stu-id="9cb8e-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="9cb8e-121">Mapping di proprietà</span><span class="sxs-lookup"><span data-stu-id="9cb8e-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="9cb8e-122">Anteprime</span><span class="sxs-lookup"><span data-stu-id="9cb8e-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="9cb8e-123">Voce di menu Apri percorso file</span><span class="sxs-lookup"><span data-stu-id="9cb8e-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="9cb8e-124">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9cb8e-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="9cb8e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cb8e-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="9cb8e-126">File di descrizione OpenSearch</span><span class="sxs-lookup"><span data-stu-id="9cb8e-126">OpenSearch Description File</span></span>

<span data-ttu-id="9cb8e-127">Un file di descrizione OpenSearch (. osdx) per la ricerca federata di Windows deve rispettare le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="9cb8e-128">Essere un documento OpenSearch Description valido, come definito dalla specifica [OpenSearch](https://github.com/dewitt/opensearch) 1,1.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="9cb8e-129">Fornire un modello di URL con un tipo di formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="9cb8e-130">Utilizzare l'estensione del nome di file. osdx o associarla all'estensione di file osdx durante il download dal Web.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="9cb8e-131">Ad esempio, non è necessario che un server usi. osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="9cb8e-132">Un server può restituire il file con qualsiasi estensione di file, ad esempio. XML, e considerato come se fosse un file. osdx se usa il tipo MIME corretto per i documenti di descrizione OpenSearch (file con estensione osdx).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="9cb8e-133">Fornire un valore di elemento **ShortName** (scelta consigliata).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="9cb8e-134">Minima elementi figlio obbligatori</span><span class="sxs-lookup"><span data-stu-id="9cb8e-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="9cb8e-135">Il file osdx di esempio seguente è costituito da **ShortName** e `Url` Elements, che sono gli elementi figlio minimi richiesti.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="9cb8e-136">Elementi standard in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="9cb8e-137">Oltre agli elementi figlio minimi, la ricerca federata supporta i seguenti elementi standard.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="9cb8e-138">Nome breve</span><span class="sxs-lookup"><span data-stu-id="9cb8e-138">Shortname</span></span>

<span data-ttu-id="9cb8e-139">Windows usa il valore dell'elemento **ShortName** per denominare il file. searchconnector-ms (connettore di ricerca) che viene creato quando l'utente apre il file. osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="9cb8e-140">Windows garantisce che il nome file generato usi solo i caratteri consentiti nei nomi file di Windows.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="9cb8e-141">Se non viene specificato alcun valore **ShortName** , il file. searchconnector-ms tenta di usare invece il nome file del file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="9cb8e-142">Il codice seguente illustra come usare l'elemento **ShortName** in un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="9cb8e-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cb8e-143">Description</span></span>

<span data-ttu-id="9cb8e-144">Windows utilizza il valore dell'elemento **Description** per popolare la descrizione del file visualizzata nel riquadro dei dettagli di Esplora risorse quando un utente seleziona un file con estensione searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="9cb8e-145">Modello di URL per i risultati RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="9cb8e-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="9cb8e-146">Il file. osdx deve includere un elemento del **formato dell'URL** e un attributo di **modello** (un modello di URL) che restituisce i risultati in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="9cb8e-147">L'attributo Format deve essere impostato su `application/rss+xml` per i risultati in formato RSS o `application/atom+xml` per i risultati in formato Atom, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="9cb8e-148">L'elemento **formato URL** e l'attributo **modello** sono comunemente noti come modello di URL.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="9cb8e-149">Modello di URL per i risultati Web</span><span class="sxs-lookup"><span data-stu-id="9cb8e-149">URL Template for web Results</span></span>

<span data-ttu-id="9cb8e-150">Se è presente una versione dei risultati della ricerca che può essere visualizzata in un Web browser, è necessario specificare un **URL Format =** `text/html` Element e **template** Attribute, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="9cb8e-151">Se si specifica un elemento **URL Format = "text/html"** e un attributo **template** , viene visualizzato un pulsante nella barra dei comandi di Esplora risorse, come illustrato nello screenshot seguente, che consente all'utente di aprire un Web browser per visualizzare i risultati della ricerca quando l'utente esegue una query.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![screenshot che mostra il pulsante di ricerca Web.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="9cb8e-153">Il rollup della query all'interfaccia utente Web dell'archivio dati è importante in alcuni scenari.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="9cb8e-154">Ad esempio, è possibile che un utente desideri visualizzare più di 100 risultati (il numero predefinito di elementi richiesti dal provider OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="9cb8e-155">In tal caso, è possibile che l'utente desideri utilizzare anche le funzionalità di ricerca disponibili solo sul sito Web dell'archivio dati, ad esempio l'esecuzione di una nuova query con un ordinamento diverso, oppure la trasformazione e il filtraggio della query con i metadati correlati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="9cb8e-156">Parametri del modello URL</span><span class="sxs-lookup"><span data-stu-id="9cb8e-156">URL Template Parameters</span></span>

<span data-ttu-id="9cb8e-157">Il provider OpenSearch esegue sempre le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="9cb8e-158">Usa il modello di URL per inviare la richiesta al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="9cb8e-159">Tenta di sostituire i token trovati nel modello di URL prima di inviare la richiesta al servizio Web, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="9cb8e-160">Sostituisce i token OpenSearch standard elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="9cb8e-161">Rimuove tutti i token non elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="9cb8e-162">Token supportato</span><span class="sxs-lookup"><span data-stu-id="9cb8e-162">Supported token</span></span>  | <span data-ttu-id="9cb8e-163">Modalità di utilizzo del provider OpenSearch</span><span class="sxs-lookup"><span data-stu-id="9cb8e-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb8e-164">searchTerms</span><span class="sxs-lookup"><span data-stu-id="9cb8e-164">{searchTerms}</span></span>    | <span data-ttu-id="9cb8e-165">Sostituito con i termini di ricerca che l'utente digita nella casella di input di ricerca di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="9cb8e-166">startIndex</span><span class="sxs-lookup"><span data-stu-id="9cb8e-166">{startIndex}</span></span>     | <span data-ttu-id="9cb8e-167">Utilizzato quando si recuperano i risultati in "Pages".</span><span class="sxs-lookup"><span data-stu-id="9cb8e-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="9cb8e-168">Sostituito con l'indice per il primo elemento di risultato da restituire.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="9cb8e-169">Startpage</span><span class="sxs-lookup"><span data-stu-id="9cb8e-169">{startPage}</span></span>      | <span data-ttu-id="9cb8e-170">Utilizzato quando si recuperano i risultati in "Pages".</span><span class="sxs-lookup"><span data-stu-id="9cb8e-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="9cb8e-171">Sostituito con il numero di pagina del set di risultati della ricerca da restituire.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="9cb8e-172">conteggio</span><span class="sxs-lookup"><span data-stu-id="9cb8e-172">{count}</span></span>          | <span data-ttu-id="9cb8e-173">Utilizzato quando si recuperano i risultati in "Pages".</span><span class="sxs-lookup"><span data-stu-id="9cb8e-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="9cb8e-174">Sostituito con il numero di risultati della ricerca per ogni pagina richiesta da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="9cb8e-175">linguaggio</span><span class="sxs-lookup"><span data-stu-id="9cb8e-175">{language}</span></span>       | <span data-ttu-id="9cb8e-176">Sostituito con una stringa che indica il linguaggio della query inviata.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="9cb8e-177">InputEncoding</span><span class="sxs-lookup"><span data-stu-id="9cb8e-177">{inputEncoding}</span></span>  | <span data-ttu-id="9cb8e-178">Sostituito con una stringa (ad esempio "UTF-16") che indica la codifica dei caratteri della query inviata.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="9cb8e-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="9cb8e-179">{outputEncoding}</span></span> | <span data-ttu-id="9cb8e-180">Sostituito con una stringa (ad esempio "UTF-16") che indica la codifica dei caratteri desiderata per la risposta del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="9cb8e-181">Risultati di paging</span><span class="sxs-lookup"><span data-stu-id="9cb8e-181">Paged Results</span></span>

<span data-ttu-id="9cb8e-182">È possibile che si desideri limitare il numero di risultati restituiti per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="9cb8e-183">È possibile scegliere di restituire una "pagina" di risultati alla volta oppure di fare in modo che il provider OpenSearch ottenga ulteriori pagine di risultati in base al numero di elemento o al numero di pagina.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="9cb8e-184">Se, ad esempio, si inviano venti risultati per pagina, la prima pagina inviata inizia in corrispondenza dell'indice dell'elemento 1 e della pagina 1; la seconda pagina inviata inizia in corrispondenza dell'indice degli elementi 21 e della pagina 2.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="9cb8e-185">È possibile definire il modo in cui si vuole che il provider OpenSearch richieda elementi usando il `{startItem}` `{startPage}` token o nel modello di URL.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="9cb8e-186">Paging mediante l'indice dell'elemento</span><span class="sxs-lookup"><span data-stu-id="9cb8e-186">Paging Using the Item Index</span></span>

<span data-ttu-id="9cb8e-187">Un indice di elemento identifica il primo elemento di risultato in una pagina di risultati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="9cb8e-188">Se si vuole che i client inviino richieste usando un indice di elemento, è possibile usare il `{startIndex}` token nell'attributo del **modello** di elemento **URL** , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="9cb8e-189">Il provider [OpenSearch](https://github.com/dewitt/opensearch) sostituisce quindi il token nell'URL con un valore di indice iniziale.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="9cb8e-190">La prima richiesta inizia con il primo elemento, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="9cb8e-191">Il provider OpenSearch può ottenere elementi aggiuntivi modificando il `{startIndex}` valore del parametro ed eseguendo una nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="9cb8e-192">Il provider ripete questo processo fino a ottenere risultati sufficienti per soddisfare il limite o raggiunge la fine dei risultati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="9cb8e-193">Il provider OpenSearch esamina il numero di elementi restituiti dal servizio Web nella prima pagina di risultati e imposta la dimensione di pagina prevista su tale numero.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="9cb8e-194">USA tale numero per incrementare il `{startIndex}` valore delle richieste successive.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="9cb8e-195">Se, ad esempio, il servizio Web restituisce 20 risultati nella prima richiesta, il provider imposta la dimensione di pagina prevista su 20.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="9cb8e-196">Per la richiesta successiva, il provider sostituisce `{startIndex}` con il valore 21 per ottenere i successivi 20 elementi.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="9cb8e-197">Se una pagina di risultati restituiti dal servizio Web dispone di un numero inferiore di elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e interrompa l'esecuzione delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="9cb8e-198">Paging tramite l'indice della pagina</span><span class="sxs-lookup"><span data-stu-id="9cb8e-198">Paging Using the Page Index</span></span>

<span data-ttu-id="9cb8e-199">Un indice di pagina identifica la pagina di risultati specificata.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="9cb8e-200">Se si vuole che i client inviino richieste usando un numero di pagina, è possibile usare il `{startPage}` token nell'attributo del **modello** di elemento **formato URL** per indicare che, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="9cb8e-201">Il provider OpenSearch sostituisce quindi il token nell'URL con un parametro di numero di pagina.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="9cb8e-202">La prima richiesta inizia con la prima pagina, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="9cb8e-203">Se una pagina di risultati restituiti dal servizio Web dispone di un numero inferiore di elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e interrompa l'esecuzione delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="9cb8e-204">Dimensioni pagina</span><span class="sxs-lookup"><span data-stu-id="9cb8e-204">Page Size</span></span>

<span data-ttu-id="9cb8e-205">È possibile configurare il servizio Web per consentire a una richiesta di specificare le dimensioni delle pagine usando un parametro nell'URL.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="9cb8e-206">È necessario specificare una richiesta nel file con estensione osdx usando il `{count}` token, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="9cb8e-207">Il provider [OpenSearch](https://github.com/dewitt/opensearch) può quindi impostare le dimensioni di pagina desiderate, in numero di risultati per pagina, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="9cb8e-208">Per impostazione predefinita, il provider OpenSearch esegue richieste usando una dimensione di pagina di 50.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="9cb8e-209">Se si desiderano dimensioni di pagina diverse, non fornire un `{count}` token e inserire invece il numero desiderato direttamente nell'elemento del **modello URL** .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="9cb8e-210">Il provider OpenSearch determina le dimensioni della pagina in base al numero di risultati restituiti alla prima richiesta.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="9cb8e-211">Se la prima pagina di risultati ricevuta ha un numero di elementi inferiore al numero richiesto, il provider Reimposta le dimensioni di pagina per tutte le richieste di pagina successive.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="9cb8e-212">Se le richieste di pagina successive restituiscono un numero di elementi inferiore a quello richiesto, il provider OpenSearch presuppone che abbia raggiunto la fine dei risultati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="9cb8e-213">Elementi estesi in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="9cb8e-214">Oltre agli elementi standard, la ricerca federata supporta gli elementi estesi seguenti: **MaximumResultCount** e **ResultsProcessing**.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="9cb8e-215">Poiché questi elementi figlio estesi non sono supportati nella specifica [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, è necessario aggiungerli usando lo spazio dei nomi seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="9cb8e-216">Numero massimo di risultati</span><span class="sxs-lookup"><span data-stu-id="9cb8e-216">Maximum Result Count</span></span>

<span data-ttu-id="9cb8e-217">Per impostazione predefinita, i connettori di ricerca sono limitati a 100 risultati per query utente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="9cb8e-218">Questo limite può essere personalizzato includendo l'elemento **MaximumResultCount** all'interno del file OSD, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="9cb8e-219">Nell'esempio precedente viene dichiarato il prefisso dello spazio dei nomi `ms-ose` nell'elemento **OpenSearchDescription** di primo livello, che viene quindi utilizzato come prefisso nel nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="9cb8e-220">Questa dichiarazione è obbligatoria perché **MaximumResultCount** non è supportato nella specifica [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="9cb8e-221">Mapping di proprietà</span><span class="sxs-lookup"><span data-stu-id="9cb8e-221">Property Mapping</span></span>

<span data-ttu-id="9cb8e-222">Quando i risultati vengono restituiti dal servizio Web come feed RSS o Atom, il provider OpenSearch deve eseguire il mapping dei metadati degli elementi nei feed alle proprietà che possono essere utilizzate dalla shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="9cb8e-223">Lo screenshot seguente illustra il modo in cui il provider OpenSearch esegue il mapping di alcuni degli elementi RSS predefiniti.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![screenshot che mostra i mapping incorporati di proprietà da RSS a Windows Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="9cb8e-225">Mapping predefiniti</span><span class="sxs-lookup"><span data-stu-id="9cb8e-225">Default Mappings</span></span>

<span data-ttu-id="9cb8e-226">I mapping predefiniti degli elementi XML RSS alle proprietà di sistema della shell di Windows sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="9cb8e-227">I percorsi XML sono relativi all'elemento Item.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="9cb8e-228">Il `"media:"` prefisso viene definito dallo spazio dei nomi dello [spazio dei nomi di Yahoo Search](https://www.rssboard.org/media-rss) .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="9cb8e-229">Percorso XML RSS</span><span class="sxs-lookup"><span data-stu-id="9cb8e-229">RSS XML path</span></span>                  | <span data-ttu-id="9cb8e-230">Proprietà della shell di Windows (nome canonico)</span><span class="sxs-lookup"><span data-stu-id="9cb8e-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="9cb8e-231">Collegamento</span><span class="sxs-lookup"><span data-stu-id="9cb8e-231">Link</span></span>                          | <span data-ttu-id="9cb8e-232">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="9cb8e-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="9cb8e-233">Titolo</span><span class="sxs-lookup"><span data-stu-id="9cb8e-233">Title</span></span>                         | <span data-ttu-id="9cb8e-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="9cb8e-234">System.ItemName</span></span>                         |
| <span data-ttu-id="9cb8e-235">Autore</span><span class="sxs-lookup"><span data-stu-id="9cb8e-235">Author</span></span>                        | <span data-ttu-id="9cb8e-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="9cb8e-236">System.Author</span></span>                           |
| <span data-ttu-id="9cb8e-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="9cb8e-237">pubDate</span></span>                       | <span data-ttu-id="9cb8e-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="9cb8e-238">System.DateModified</span></span>                     |
| <span data-ttu-id="9cb8e-239">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cb8e-239">Description</span></span>                   | <span data-ttu-id="9cb8e-240">System. AutoSummary</span><span class="sxs-lookup"><span data-stu-id="9cb8e-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="9cb8e-241">Category</span><span class="sxs-lookup"><span data-stu-id="9cb8e-241">Category</span></span>                      | <span data-ttu-id="9cb8e-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="9cb8e-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="9cb8e-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="9cb8e-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="9cb8e-244">System. size</span><span class="sxs-lookup"><span data-stu-id="9cb8e-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="9cb8e-245">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="9cb8e-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="9cb8e-246">supporto: Categoria</span><span class="sxs-lookup"><span data-stu-id="9cb8e-246">media:category</span></span>                | <span data-ttu-id="9cb8e-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="9cb8e-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="9cb8e-248">System. size</span><span class="sxs-lookup"><span data-stu-id="9cb8e-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="9cb8e-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="9cb8e-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="9cb8e-250">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="9cb8e-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="9cb8e-251">System. size</span><span class="sxs-lookup"><span data-stu-id="9cb8e-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="9cb8e-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="9cb8e-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="9cb8e-253">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="9cb8e-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="9cb8e-254">System. ItemThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="9cb8e-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="9cb8e-255">Oltre ai mapping predefiniti degli elementi RSS o Atom standard, è possibile eseguire il mapping di altre proprietà di sistema della shell di Windows includendo elementi XML aggiuntivi nello spazio dei nomi Windows per ciascuna proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="9cb8e-256">È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML esistenti, ad esempio MediaRSS, iTunes e così via, aggiungendo un mapping personalizzato delle proprietà nel file. osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="9cb8e-257">Mapping di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="9cb8e-257">Custom Property Mappings</span></span>

<span data-ttu-id="9cb8e-258">È possibile personalizzare il mapping degli elementi dall'output RSS alle proprietà di sistema della shell di Windows specificando il mapping nel file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="9cb8e-259">L'output RSS specifica:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="9cb8e-260">Uno spazio dei nomi XML e</span><span class="sxs-lookup"><span data-stu-id="9cb8e-260">An XML namespace, and</span></span>
-   <span data-ttu-id="9cb8e-261">Per qualsiasi elemento figlio di un elemento, il nome di un elemento su cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="9cb8e-262">Il file con estensione osdx identifica una proprietà della shell di Windows per ogni nome di elemento in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="9cb8e-263">I mapping di proprietà definiti nel file con estensione osdx sostituiscono i mapping predefiniti, se esistenti, per le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="9cb8e-264">Il diagramma seguente illustra come viene eseguito il mapping di un'estensione RSS alle proprietà di Windows (nome canonico).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![diagramma che mostra che la combinazione di spazio dei nomi XML e percorso XML produce il nome canonico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="9cb8e-266">Risultati RSS di esempio e mapping di proprietà OSD</span><span class="sxs-lookup"><span data-stu-id="9cb8e-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="9cb8e-267">L'output RSS di esempio seguente identifica lo `https://example.com/schema/2009` spazio dei nomi XML con il prefisso "example".</span><span class="sxs-lookup"><span data-stu-id="9cb8e-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="9cb8e-268">Questo prefisso deve essere visualizzato di nuovo prima dell'elemento di **posta elettronica** .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="9cb8e-269">Nel file osdx di esempio seguente l'elemento di **posta elettronica** XML viene mappato alla proprietà della shell di Windows [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="9cb8e-270">Alcune proprietà non possono essere mappate perché i valori per esse sono sostituiti in un secondo momento o non sono modificabili.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="9cb8e-271">Non è ad esempio possibile eseguire il mapping di [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) perché vengono calcolati dal valore dell'URL fornito negli elementi del collegamento o dell'enclosure.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="9cb8e-272">Anteprime</span><span class="sxs-lookup"><span data-stu-id="9cb8e-272">Thumbnails</span></span>

<span data-ttu-id="9cb8e-273">Gli URL dell'immagine di anteprima possono essere forniti per qualsiasi elemento usando l'elemento **media: thumbnail URL = ""** .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="9cb8e-274">La risoluzione ideale è 150 x 150 pixel.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="9cb8e-275">Le anteprime più grandi supportate sono 256 x 256 pixel.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="9cb8e-276">Fornire immagini più grandi richiede una maggiore larghezza di banda senza alcun vantaggio aggiuntivo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="9cb8e-277">Apri il menu di scelta rapida percorso file</span><span class="sxs-lookup"><span data-stu-id="9cb8e-277">Open File Location Context Menu</span></span>

<span data-ttu-id="9cb8e-278">In Windows è disponibile un menu di scelta rapida denominato **Apri percorso file** per gli elementi dei risultati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="9cb8e-279">Se l'utente seleziona un elemento da tale menu, viene aperto l'URL "padre" per l'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="9cb8e-280">Se l'URL è un URL Web, ad esempio `https://...` , il Web browser viene aperto e passa a tale URL.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="9cb8e-281">Il feed deve fornire un URL personalizzato per ogni elemento per assicurarsi che Windows apra un URL valido.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="9cb8e-282">Questa operazione può essere eseguita includendo l'URL all'interno di un elemento all'interno del codice XML dell'elemento, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="9cb8e-283">Se questa proprietà non è impostata in modo esplicito nel codice XML dell'elemento, il provider OpenSearch lo imposta sulla cartella padre dell'URL dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="9cb8e-284">Nell'esempio precedente il provider OpenSearch usa il valore del collegamento e imposta il valore della proprietà della shell di Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) su `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="9cb8e-285">Personalizzare le visualizzazioni di Esplora risorse con elenchi di descrizioni delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9cb8e-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="9cb8e-286">Alcuni layout di visualizzazione di Esplora risorse sono definiti da elenchi di descrizioni delle proprietà, o proplists.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="9cb8e-287">Un oggetto prop è un elenco delimitato da punti e virgola di proprietà, ad esempio `"prop:System.ItemName; System.Author"` , usato per controllare la modalità di visualizzazione dei risultati in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="9cb8e-288">Le aree dell'interfaccia utente di Esplora risorse che possono essere personalizzate tramite proplists sono illustrate nella schermata seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![screenshot che mostra le aree dell'interfaccia utente di Esplora risorse che possono essere personalizzate mediante proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="9cb8e-290">A ogni area di Esplora risorse è associato un set di proplists, che vengono specificati come proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="9cb8e-291">È possibile specificare proplists personalizzati per i singoli elementi nei set di risultati o per tutti gli elementi di un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="9cb8e-292">Area dell'interfaccia utente da personalizzare</span><span class="sxs-lookup"><span data-stu-id="9cb8e-292">UI Area to customize</span></span>               | <span data-ttu-id="9cb8e-293">Proprietà della shell di Windows che implementa la personalizzazione</span><span class="sxs-lookup"><span data-stu-id="9cb8e-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="9cb8e-294">Modalità di visualizzazione contenuto (durante la ricerca)</span><span class="sxs-lookup"><span data-stu-id="9cb8e-294">Content view mode (when searching)</span></span> | <span data-ttu-id="9cb8e-295">System. Propin. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="9cb8e-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="9cb8e-296">Modalità di visualizzazione contenuto (quando si Esplora)</span><span class="sxs-lookup"><span data-stu-id="9cb8e-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="9cb8e-297">System. Propin. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="9cb8e-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="9cb8e-298">Modalità visualizzazione affiancata</span><span class="sxs-lookup"><span data-stu-id="9cb8e-298">Tile view mode</span></span>                     | <span data-ttu-id="9cb8e-299">System. Propin. TileInfo</span><span class="sxs-lookup"><span data-stu-id="9cb8e-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="9cb8e-300">Riquadro dei dettagli</span><span class="sxs-lookup"><span data-stu-id="9cb8e-300">Details pane</span></span>                       | <span data-ttu-id="9cb8e-301">System. Propin. PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="9cb8e-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="9cb8e-302">Infotip (descrizione comando hover dell'elemento)</span><span class="sxs-lookup"><span data-stu-id="9cb8e-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="9cb8e-303">System. Propin. infotip</span><span class="sxs-lookup"><span data-stu-id="9cb8e-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="9cb8e-304">**Per specificare un oggetto univoco per un singolo elemento:**</span><span class="sxs-lookup"><span data-stu-id="9cb8e-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="9cb8e-305">Nell'output RSS aggiungere un elemento personalizzato che rappresenta l'oggetto di proprietà che si desidera personalizzare.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="9cb8e-306">Nell'esempio seguente viene impostato l'elenco per il riquadro Dettagli:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="9cb8e-307">Per applicare una proprietà a ogni elemento nei risultati della ricerca senza modificare l'output RSS, specificare un oggetto prop all'interno di un elemento **MS-OSE: PropertyDefaultValues** nel file con estensione osdx, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="9cb8e-308">Layout della modalità di visualizzazione contenuto delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9cb8e-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="9cb8e-309">L'elenco delle proprietà specificate in **System. propt. ContentViewModeForSearch** e **System. propName. ContentViewModeForBrowse** proplists determina ciò che viene visualizzato in modalità di visualizzazione contenuto.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="9cb8e-310">Per ulteriori informazioni sugli elenchi di proprietà, [vedere l'](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="9cb8e-311">Le proprietà sono disposte in base ai numeri mostrati nel modello di layout seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![screenshot che mostra il modello di layout predefinito nella visualizzazione contenuto](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="9cb8e-313">Se si usa l'elenco di proprietà seguente,</span><span class="sxs-lookup"><span data-stu-id="9cb8e-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="9cb8e-314">Viene visualizzata la schermata seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-314">Then we see the following display:</span></span>

![screenshot che mostra il layout delle proprietà di esempio.](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="9cb8e-316">Per una migliore leggibilità, è necessario etichettare le proprietà visualizzate nella colonna a destra.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="9cb8e-317">Flag elenco proprietà</span><span class="sxs-lookup"><span data-stu-id="9cb8e-317">Property List Flags</span></span>

<span data-ttu-id="9cb8e-318">Solo uno dei flag definiti nella documentazione di proplists si applica alla visualizzazione degli elementi nei layout della modalità di visualizzazione del contenuto: ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="9cb8e-319">Negli esempi precedenti, la visualizzazione Esplora risorse di Windows etichetta alcune proprietà, ad esempio `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="9cb8e-320">Questo è il comportamento predefinito quando si specifica una proprietà nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="9cb8e-321">Ad esempio, l'oggetto di proprietà `"System.Author"` è visualizzato come `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="9cb8e-322">Quando si vuole nascondere l'etichetta della proprietà, posizionare un oggetto `"~"` davanti al nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="9cb8e-323">Se, ad esempio, la proprietà contiene `"~System.Size"` , la proprietà viene visualizzata come un solo valore, senza l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="9cb8e-324">Anteprime</span><span class="sxs-lookup"><span data-stu-id="9cb8e-324">Previews</span></span>

<span data-ttu-id="9cb8e-325">Quando l'utente seleziona un elemento di risultato in Esplora risorse e il riquadro di anteprima è aperto, il contenuto dell'elemento viene visualizzato in anteprima.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="9cb8e-326">Il contenuto da visualizzare nell'anteprima viene specificato da un URL, determinato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="9cb8e-327">Se la proprietà della shell di Windows **System. WebPreviewUrl** è impostata per l'elemento, usare tale URL.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="9cb8e-328">La proprietà deve essere fornita nel feed RSS usando lo spazio dei nomi della shell di Windows o il mapping esplicito nel file. osdx.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="9cb8e-329">In caso contrario, usare invece l'URL del collegamento.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="9cb8e-330">Il diagramma di flusso seguente illustra questa logica.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-330">The following flowchart shows this logic.</span></span>

![diagramma di flusso che illustra in che modo Esplora risorse seleziona l'URL da usare per le anteprime](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="9cb8e-332">È possibile usare un URL diverso per l'anteprima rispetto all'elemento stesso.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="9cb8e-333">Ciò significa che se si specificano URL diversi per l'URL del collegamento e l'enclosure oppure `media:content URL` , Esplora risorse utilizza l'URL del collegamento per le anteprime dell'elemento, ma utilizza l'altro URL per il rilevamento del tipo di file, l'apertura, il download e così via.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="9cb8e-334">Modalità di determinazione dell'URL da utilizzare in Esplora risorse:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="9cb8e-335">Se si fornisce un mapping a [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), Esplora risorse usa tale URL</span><span class="sxs-lookup"><span data-stu-id="9cb8e-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="9cb8e-336">Se non si specifica un mapping, Esplora risorse indica se gli URL del collegamento e dell'enclosure sono diversi.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="9cb8e-337">In tal caso, Esplora risorse utilizza l'URL del collegamento.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="9cb8e-338">Se gli URL sono uguali o se è presente solo un URL di collegamento, Esplora risorse analizza il collegamento per trovare il contenitore padre rimuovendo il nome del file dall'URL completo.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="9cb8e-339">Se si riconosce che l'analisi degli URL comporterebbe collegamenti non recapitabili per il servizio, è necessario fornire un mapping esplicito per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="9cb8e-340">Voce di menu Apri percorso file</span><span class="sxs-lookup"><span data-stu-id="9cb8e-340">Open File Location Menu Item</span></span>

<span data-ttu-id="9cb8e-341">Quando si fa clic con il pulsante destro del mouse su un elemento, viene visualizzato il comando di menu **Apri percorso file** .</span><span class="sxs-lookup"><span data-stu-id="9cb8e-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="9cb8e-342">Questo comando porta l'utente al contenitore per la posizione o dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="9cb8e-343">Ad esempio, in una ricerca di SharePoint, la selezione di questa opzione per un file in una raccolta documenti apre la radice della raccolta documenti nel Web browser.</span><span class="sxs-lookup"><span data-stu-id="9cb8e-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="9cb8e-344">Quando un utente fa clic su **Apri percorso file**, Esplora risorse tenta di trovare un contenitore padre, usando la logica mostrata nel diagramma di flusso seguente:</span><span class="sxs-lookup"><span data-stu-id="9cb8e-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![diagramma di flusso che illustra come Windows Explorer identifica un contenitore padre](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="9cb8e-346">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9cb8e-346">Additional Resources</span></span>

<span data-ttu-id="9cb8e-347">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9cb8e-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cb8e-348">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cb8e-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb8e-349">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="9cb8e-350">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="9cb8e-351">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="9cb8e-352">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="9cb8e-353">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="9cb8e-354">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="9cb8e-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
