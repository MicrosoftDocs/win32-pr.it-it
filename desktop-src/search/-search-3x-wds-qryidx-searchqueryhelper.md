---
description: "È possibile utilizzare l'interfaccia ISearchQueryHelper per eseguire una query sull'indice. Questa interfaccia viene implementata come classe helper per ISearchCatalogManager (e ISearchCatalogManager2) ed è ottenuta chiamando ISearchCatalogManager:: GetQueryHelper."
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Esecuzione di query sull'indice con ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225957"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="f4c58-104">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f4c58-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="f4c58-105">È possibile utilizzare l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per eseguire una query sull'indice.</span><span class="sxs-lookup"><span data-stu-id="f4c58-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="f4c58-106">Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ed è ottenuta chiamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="f4c58-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="f4c58-107">Questa interfaccia consente di:</span><span class="sxs-lookup"><span data-stu-id="f4c58-107">This interface permits you to:</span></span>

-   <span data-ttu-id="f4c58-108">Ottenere una stringa di connessione OLE DB per connettersi al database di Windows Search.</span><span class="sxs-lookup"><span data-stu-id="f4c58-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="f4c58-109">Converte le query utente AQS (Advanced Query Syntax) in Windows Search Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="f4c58-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="f4c58-110">Specificare le restrizioni per le query che possono essere espresse in SQL, ma non in AQS.</span><span class="sxs-lookup"><span data-stu-id="f4c58-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="f4c58-111">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f4c58-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f4c58-112">Introduzione con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f4c58-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="f4c58-113">Utilizzo del metodo GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="f4c58-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="f4c58-114">Utilizzo degli identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="f4c58-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="f4c58-115">Utilizzo di proprietà e colonne</span><span class="sxs-lookup"><span data-stu-id="f4c58-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="f4c58-116">Utilizzo dell'espansione del termine di query</span><span class="sxs-lookup"><span data-stu-id="f4c58-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="f4c58-117">Utilizzo di altri metodi di ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f4c58-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="f4c58-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4c58-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="f4c58-119">Introduzione con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f4c58-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="f4c58-120">Prima di poter iniziare a eseguire query a livello di codice tramite l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , è necessario tenere presenti alcune interfacce e metodi chiave.</span><span class="sxs-lookup"><span data-stu-id="f4c58-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="f4c58-121">A un livello elevato, è necessario seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="f4c58-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="f4c58-122">Creare un'istanza di [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="f4c58-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="f4c58-123">Ottenere un'istanza di [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) mediante [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span><span class="sxs-lookup"><span data-stu-id="f4c58-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="f4c58-124">Il nome del catalogo di sistema per Windows Search è `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="f4c58-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="f4c58-125">Ottenere un'istanza di [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) con [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="f4c58-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="f4c58-126">Quando si dispone di un'istanza di [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), è possibile ottenere la stringa di connessione utilizzata per la connessione all'indice di ricerca di Windows OLE DB il connettore.</span><span class="sxs-lookup"><span data-stu-id="f4c58-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="f4c58-127">Utilizzo del metodo GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="f4c58-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="f4c58-128">Il metodo [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) trasforma l'input dell'utente in una stringa di query SQL che può quindi essere inviata al provider OLE DB per la ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="f4c58-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="f4c58-129">Questo metodo converte la query AQS ( [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) ) o NQS (Natural Query Syntax) immessa dall'utente in SQL e consente di aggiungere altri frammenti SQL in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f4c58-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="f4c58-130">La stringa di query SQL viene restituita nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="f4c58-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="f4c58-131">Di seguito è riportato un esempio della stringa SQL restituita dalla chiamata `GenerateSQLFromUserQuery("comput")` :</span><span class="sxs-lookup"><span data-stu-id="f4c58-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="f4c58-132">Il metodo genera sia FREETEXT che CONTAINs predicati perché CONTAINs alone non genera un rango significativo.</span><span class="sxs-lookup"><span data-stu-id="f4c58-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="f4c58-133">Utilizzo degli identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="f4c58-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="f4c58-134">Metodo</span><span class="sxs-lookup"><span data-stu-id="f4c58-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="f4c58-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c58-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c58-136">[**ISearchQueryHelper:: Get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="f4c58-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="f4c58-137">**ISearchQueryHelper::p UT \_ QueryContentLocale**</span><span class="sxs-lookup"><span data-stu-id="f4c58-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="f4c58-138">Ottiene o imposta l'identificatore del codice lingua (LCID) della query.</span><span class="sxs-lookup"><span data-stu-id="f4c58-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="f4c58-139">Questo consente di ottenere il Word breaker e lo stemmer corretti per confrontare i termini di query con il catalogo/indice invertito.</span><span class="sxs-lookup"><span data-stu-id="f4c58-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="f4c58-140">Il valore predefinito corrisponde alle impostazioni locali di input correnti.</span><span class="sxs-lookup"><span data-stu-id="f4c58-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="f4c58-141">[**ISearchQueryHelper:: Get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="f4c58-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="f4c58-142">**ISearchQueryHelper::p UT \_ QueryKeywordLocale**</span><span class="sxs-lookup"><span data-stu-id="f4c58-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="f4c58-143">Ottiene o imposta l'LCID per il linguaggio da utilizzare durante l'analisi delle parole chiave AQS (Advanced Query Syntax).</span><span class="sxs-lookup"><span data-stu-id="f4c58-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="f4c58-144">Il valore predefinito corrisponde alle impostazioni locali dell'utente predefinite.</span><span class="sxs-lookup"><span data-stu-id="f4c58-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="f4c58-145">Le impostazioni locali del **contenuto** e le **impostazioni locali delle parole chiave** sono identificatori delle impostazioni locali (LCID) che consentono al motore di ricerca di usare i Word breaker corretti identificando la lingua dei termini della query e la lingua delle parole chiave AQS.</span><span class="sxs-lookup"><span data-stu-id="f4c58-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="f4c58-146">Questi non sono sempre gli stessi LCID perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI (Multilingual User Interface) Pack per altre lingue.</span><span class="sxs-lookup"><span data-stu-id="f4c58-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="f4c58-147">Le impostazioni locali del contenuto identificano l'identificatore LCID per il linguaggio con cui gli utenti immetteranno la query di ricerca in, mentre le impostazioni locali della parola chiave identificano il LCID utilizzato dal motore di ricerca durante l'analisi delle parole chiave AQS (Advanced Query Syntax).</span><span class="sxs-lookup"><span data-stu-id="f4c58-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="f4c58-148">Ad esempio, se si dispone della versione inglese (Stati Uniti) senza MUI Pack, le impostazioni locali del contenuto e le impostazioni locali della parola chiave sono 1033.</span><span class="sxs-lookup"><span data-stu-id="f4c58-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="f4c58-149">Se si dispone della versione tedesca senza MUI Pack, le impostazioni locali del contenuto e le impostazioni locali della parola chiave sono 1031 (gr-gr).</span><span class="sxs-lookup"><span data-stu-id="f4c58-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="f4c58-150">Tuttavia, se si dispone della versione in lingua inglese con MUI Pack Romeno, le impostazioni locali del contenuto sono 2072 (RO) e la parola chiave locale è 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="f4c58-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="f4c58-151">Utilizzo di proprietà e colonne</span><span class="sxs-lookup"><span data-stu-id="f4c58-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="f4c58-152">Metodi</span><span class="sxs-lookup"><span data-stu-id="f4c58-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="f4c58-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c58-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c58-154">[**ISearchQueryHelper:: Get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="f4c58-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="f4c58-155">**ISearchQueryHelper::p UT \_ QueryContentProperties**</span><span class="sxs-lookup"><span data-stu-id="f4c58-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="f4c58-156">Ottiene o imposta le proprietà di contenuto per la ricerca (colonna della proprietà elencata nelle clausole CONTAINs o FREETEXT).</span><span class="sxs-lookup"><span data-stu-id="f4c58-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="f4c58-157">[**ISearchQueryHelper:: Get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="f4c58-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="f4c58-158">**ISearchQueryHelper::p UT \_ QuerySelectColumns**</span><span class="sxs-lookup"><span data-stu-id="f4c58-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="f4c58-159">Ottiene o imposta le colonne (o proprietà) richieste nell'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="f4c58-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="f4c58-160">Il valore predefinito è System. ItemUrl e le proprietà utilizzate nella clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="f4c58-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="f4c58-161">Gli elementi sono rappresentati nell'archivio delle proprietà come riga.</span><span class="sxs-lookup"><span data-stu-id="f4c58-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="f4c58-162">Ogni riga contiene un numero di colonne che rappresentano le proprietà di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="f4c58-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="f4c58-163">Non tutti gli elementi avranno un valore per una determinata proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4c58-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="f4c58-164">Un file audio, ad esempio, in genere non contiene un valore per la proprietà System. Property. FromName, ma può contenere informazioni relative a System. Music. Artist.</span><span class="sxs-lookup"><span data-stu-id="f4c58-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="f4c58-165">Con questi metodi, è possibile accedere o modificare la proprietà con una stringa Unicode delimitata da virgole, con terminazione null, che specifica uno o più nomi di colonna dell'archivio delle proprietà: "System.Document. Autore, System.Document. Titolo ".</span><span class="sxs-lookup"><span data-stu-id="f4c58-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="f4c58-166">Utilizzo dell'espansione del termine di query</span><span class="sxs-lookup"><span data-stu-id="f4c58-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="f4c58-167">Metodi</span><span class="sxs-lookup"><span data-stu-id="f4c58-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="f4c58-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c58-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="f4c58-169">**ISearchQueryHelper:: Get \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="f4c58-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="f4c58-170">**ISearchQueryHelper::p UT \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="f4c58-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="f4c58-171">Ottiene o imposta il flag di espansione del termine di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f4c58-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="f4c58-172">Questo metodo consente l'espansione di alcuni termini di query con caratteri jolly, in modo analogo all'espansione delle espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="f4c58-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="f4c58-173">L'espansione del prefisso Cerca parole con lo stesso prefisso (Fun/imbuto).</span><span class="sxs-lookup"><span data-stu-id="f4c58-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="f4c58-174">Se non è impostato, il valore predefinito è il prefisso del termine di ricerca \_ \_ \_ all.</span><span class="sxs-lookup"><span data-stu-id="f4c58-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="f4c58-175">I valori supportati dell'enumerazione [**di \_ \_ espansione del termine di ricerca**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c58-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="f4c58-176">\_Tutti i \_ termini di ricerca del prefisso del termine \_ di ricerca sono espansi</span><span class="sxs-lookup"><span data-stu-id="f4c58-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="f4c58-177">\_ \_ \_ Termini di ricerca senza espansione-nessun termine di ricerca espanso</span><span class="sxs-lookup"><span data-stu-id="f4c58-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="f4c58-178">Utilizzo di altri metodi di ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="f4c58-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="f4c58-179">Molti dei metodi nell'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) vengono usati per impostare gli argomenti della query o definire le proprietà restituite.</span><span class="sxs-lookup"><span data-stu-id="f4c58-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="f4c58-180">Metodi</span><span class="sxs-lookup"><span data-stu-id="f4c58-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="f4c58-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c58-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c58-182">**ISearchQueryHelper:: Get \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f4c58-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="f4c58-183">Restituisce la stringa di connessione OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f4c58-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="f4c58-184">Si tratta del metodo preferito per ottenere una stringa di connessione correttamente formattata e corretta.</span><span class="sxs-lookup"><span data-stu-id="f4c58-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="f4c58-185">**ISearchQueryHelper:: Get \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="f4c58-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="f4c58-186">**ISearchQueryHelper::p UT \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="f4c58-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="f4c58-187">Ottiene o imposta il numero massimo di risultati che devono essere restituiti da una query, ovvero SELECT TOP n.</span><span class="sxs-lookup"><span data-stu-id="f4c58-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="f4c58-188">Il valore predefinito è-1, ovvero non viene generata alcuna clausola di risultati massima.</span><span class="sxs-lookup"><span data-stu-id="f4c58-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="f4c58-189">**ISearchQueryHelper:: Get \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="f4c58-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="f4c58-190">**ISearchQueryHelper::p UT \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="f4c58-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="f4c58-191">Ottiene o imposta l'ordinamento per il set di risultati della query (ORDER BY).</span><span class="sxs-lookup"><span data-stu-id="f4c58-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="f4c58-192">Se non esiste alcuna clausola ORDER BY, i risultati vengono restituiti in ordine non deterministico.</span><span class="sxs-lookup"><span data-stu-id="f4c58-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="f4c58-193">**ISearchQueryHelper:: Get \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="f4c58-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="f4c58-194">**ISearchQueryHelper::p UT \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="f4c58-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="f4c58-195">Ottiene o imposta la sintassi della query: sintassi di query avanzata o sintassi di query naturale.</span><span class="sxs-lookup"><span data-stu-id="f4c58-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="f4c58-196">**ISearchQueryHelper:: Get \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="f4c58-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="f4c58-197">**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="f4c58-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="f4c58-198">Ottiene o imposta le restrizioni accodate tramite le clausole WHERE.</span><span class="sxs-lookup"><span data-stu-id="f4c58-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f4c58-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4c58-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4c58-200">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="f4c58-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f4c58-201">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="f4c58-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f4c58-202">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="f4c58-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="f4c58-203">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="f4c58-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="f4c58-204">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="f4c58-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




