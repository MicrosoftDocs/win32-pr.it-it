---
title: Ricerca con l'interfaccia IDirectorySearch
description: L'interfaccia IDirectorySearch fornisce un'interfaccia di alto livello e di basso overhead per l'esecuzione di query sui dati di una directory o di un catalogo globale.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Ricerca con l'interfaccia IDirectorySearch ADSI
- Query ADSI, interfacce di query, IDirectorySearch
- ADSI ADSI, esempio di codice C/C++, ricerca in una directory con IDirectorySearch
- IDirectorySearch ADSI, utilizzo di per la ricerca in una directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872970"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="f1ab7-107">Ricerca con l'interfaccia IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f1ab7-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="f1ab7-108">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce un'interfaccia di alto livello e di basso overhead per l'esecuzione di query sui dati di una directory o di un catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="f1ab7-109">L'interfaccia com **IDirectorySearch** può essere utilizzata solo con un oggetto vtable e pertanto non è disponibile per gli ambienti di sviluppo basati su automazione.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="f1ab7-110">**Per eseguire una ricerca**</span><span class="sxs-lookup"><span data-stu-id="f1ab7-110">**To perform a search**</span></span>

1.  <span data-ttu-id="f1ab7-111">Eseguire l'associazione a un oggetto nella directory.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="f1ab7-112">Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere il puntatore [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="f1ab7-113">Eseguire la ricerca usando il puntatore [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="f1ab7-114">Chiamare il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passare un filtro di ricerca, i nomi di attributo richiesti e altri parametri.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="f1ab7-115">Per ulteriori informazioni sulla sintassi del filtro di ricerca, vedere la [sintassi del filtro di ricerca](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="f1ab7-116">L'esecuzione della query è specifica del provider.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-116">Query execution is provider-specific.</span></span> <span data-ttu-id="f1ab7-117">Con alcuni provider, l'esecuzione effettiva della query non viene eseguita fino a quando non viene chiamato [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="f1ab7-118">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funziona direttamente con i filtri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="f1ab7-119">Non sono richiesti né il dialetto SQL né il dialetto LDAP.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="f1ab7-120">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce metodi per enumerare il set di risultati, riga per riga.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="f1ab7-121">Il metodo [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la prima riga e [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) passa alla riga successiva dalla riga corrente.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="f1ab7-122">Una volta raggiunta l'ultima riga, la chiamata a questi metodi restituisce il codice di errore per le \_ \_ \_ righe.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="f1ab7-123">Viceversa, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) sposta indietro una riga alla volta.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="f1ab7-124">Una S \_ Ads \_ nomore \_ Rows valore restituito indica che è stata raggiunta la prima riga del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="f1ab7-125">Questi metodi operano sul set di risultati, residente in memoria, nel client.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="f1ab7-126">Pertanto, quando vengono eseguite le ricerche di paging e asincrone e l' \_ opzione relativa ai risultati della cache è disattivata \_ , lo scorrimento a ritroso può avere conseguenze impreviste.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="f1ab7-127">Dopo aver individuato la riga appropriata, chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per ottenere gli elementi di dati, column by column.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="f1ab7-128">Per ogni chiamata si passa il nome della colonna di interesse.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="f1ab7-129">L'elemento dati restituito è un puntatore a una struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="f1ab7-130">**GetColumn** alloca questa struttura per l'utente, ma è necessario liberarla usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="f1ab7-131">Chiamare [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) per completare l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="f1ab7-132">**Per eseguire una ricerca nella directory**</span><span class="sxs-lookup"><span data-stu-id="f1ab7-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="f1ab7-133">Eseguire l'associazione a un provider LDAP.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="f1ab7-134">Può essere un controller di dominio o un provider del catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="f1ab7-135">Recuperare l'interfaccia com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una chiamata a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Questa operazione potrebbe essere stata eseguita nel passaggio 1 durante l'associazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="f1ab7-136">Facoltativamente, chiamare [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) per selezionare le opzioni per la gestione dei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="f1ab7-137">Chiamare [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="f1ab7-138">A seconda delle opzioni impostate in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , è possibile che venga avviata l'esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="f1ab7-139">Chiamare [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) per spostare l'indice di riga (interno a [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="f1ab7-140">Leggere i dati dalla riga tramite [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), quindi chiamare [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) per rilasciare la memoria allocata da **GetColumn**.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="f1ab7-141">Ripetere il passaggio 5 fino a quando non vengono recuperati tutti i dati dal risultato della ricerca o fino a quando [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) non restituisce \_ \_ più righe per ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="f1ab7-142">Chiamare [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="f1ab7-143">Nell'esempio di codice riportato di seguito viene illustrato questo scenario.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-143">The following code example shows this scenario.</span></span> <span data-ttu-id="f1ab7-144">Per avviare l'associazione a ADSI, chiamare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="f1ab7-145">In questo modo viene fornito un puntatore all'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="f1ab7-146">Ora che è disponibile un'interfaccia COM per un'istanza di IDirectoryInterface, chiamare [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="f1ab7-147">Compilare una matrice di nomi di attributo per preparare la chiamata della funzione [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="f1ab7-148">I nomi degli attributi vengono definiti all'interno dello schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="f1ab7-149">Per ulteriori informazioni sulla definizione dello schema, vedere [ADSI schema Model](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="f1ab7-150">I nomi degli attributi elencati vengono restituiti, se supportati dall'oggetto, come set di risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="f1ab7-151">A questo punto, chiamare la funzione [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="f1ab7-152">La ricerca non viene eseguita fino a quando non si chiama il metodo [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="f1ab7-153">Chiamare [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) per eseguire l'iterazione delle righe nel risultato.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="f1ab7-154">Ogni riga viene quindi sottoposta a query per l'attributo "Description".</span><span class="sxs-lookup"><span data-stu-id="f1ab7-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="f1ab7-155">Se l'attributo viene trovato, viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="f1ab7-156">Per terminare la ricerca, chiamare il metodo [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="f1ab7-157">Tenere presente che, se le dimensioni della pagina non sono impostate, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) si blocca fino a quando non viene restituito al client l'intero set di risultati.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="f1ab7-158">Se viene impostata la dimensione di pagina, **GetNextRow** si blocca fino a quando non viene restituita la prima pagina (dimensione pagina = numero di righe in una pagina).</span><span class="sxs-lookup"><span data-stu-id="f1ab7-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="f1ab7-159">Se le dimensioni della pagina sono impostate e la query deve essere ordinata e non si sta eseguendo la ricerca in almeno un attributo indicizzato, il valore delle dimensioni della pagina viene ignorato e il server calcola l'intero set di risultati prima di restituire i dati.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="f1ab7-160">Questa operazione ha effetto del blocco **GetNextRow** fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="f1ab7-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="f1ab7-161">Per modificare questa query da una ricerca di directory a una ricerca nel catalogo globale, viene modificata la chiamata [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="f1ab7-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 