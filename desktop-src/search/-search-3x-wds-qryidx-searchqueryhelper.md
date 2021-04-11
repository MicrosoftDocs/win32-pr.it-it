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
# <a name="querying-the-index-with-isearchqueryhelper"></a>Esecuzione di query sull'indice con ISearchQueryHelper

È possibile utilizzare l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) per eseguire una query sull'indice. Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ed è ottenuta chiamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Questa interfaccia consente di:

-   Ottenere una stringa di connessione OLE DB per connettersi al database di Windows Search.
-   Converte le query utente AQS (Advanced Query Syntax) in Windows Search Structured Query Language (SQL).
-   Specificare le restrizioni per le query che possono essere espresse in SQL, ma non in AQS.

Questo argomento è organizzato nel modo seguente:

-   [Introduzione con ISearchQueryHelper](#getting-started-with-isearchqueryhelper)
-   [Utilizzo del metodo GenerateSqlFromUserQuery](#using-the-generatesqlfromuserquery-method)
-   [Utilizzo degli identificatori delle impostazioni locali](#working-with-locale-identifiers)
-   [Utilizzo di proprietà e colonne](#working-with-properties-and-columns)
-   [Utilizzo dell'espansione del termine di query](#working-with-query-term-expansion)
-   [Utilizzo di altri metodi di ISearchQueryHelper](#working-with-other-isearchqueryhelper-methods)
-   [Argomenti correlati](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Introduzione con ISearchQueryHelper

Prima di poter iniziare a eseguire query a livello di codice tramite l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , è necessario tenere presenti alcune interfacce e metodi chiave. A un livello elevato, è necessario seguire questa procedura:

1.  Creare un'istanza di [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Ottenere un'istanza di [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) mediante [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). Il nome del catalogo di sistema per Windows Search è `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Ottenere un'istanza di [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) con [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Quando si dispone di un'istanza di [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), è possibile ottenere la stringa di connessione utilizzata per la connessione all'indice di ricerca di Windows OLE DB il connettore.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Utilizzo del metodo GenerateSqlFromUserQuery

Il metodo [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) trasforma l'input dell'utente in una stringa di query SQL che può quindi essere inviata al provider OLE DB per la ricerca di Windows. Questo metodo converte la query AQS ( [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) ) o NQS (Natural Query Syntax) immessa dall'utente in SQL e consente di aggiungere altri frammenti SQL in base alle esigenze.

La stringa di query SQL viene restituita nel formato seguente:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



Di seguito è riportato un esempio della stringa SQL restituita dalla chiamata `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> Il metodo genera sia FREETEXT che CONTAINs predicati perché CONTAINs alone non genera un rango significativo.

 

## <a name="working-with-locale-identifiers"></a>Utilizzo degli identificatori delle impostazioni locali



| Metodo                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: Get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Ottiene o imposta l'identificatore del codice lingua (LCID) della query. Questo consente di ottenere il Word breaker e lo stemmer corretti per confrontare i termini di query con il catalogo/indice invertito. Il valore predefinito corrisponde alle impostazioni locali di input correnti. |
| [**ISearchQueryHelper:: Get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Ottiene o imposta l'LCID per il linguaggio da utilizzare durante l'analisi delle parole chiave AQS (Advanced Query Syntax). Il valore predefinito corrisponde alle impostazioni locali dell'utente predefinite.                                                                              |



 

Le impostazioni locali del **contenuto** e le **impostazioni locali delle parole chiave** sono identificatori delle impostazioni locali (LCID) che consentono al motore di ricerca di usare i Word breaker corretti identificando la lingua dei termini della query e la lingua delle parole chiave AQS. Questi non sono sempre gli stessi LCID perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI (Multilingual User Interface) Pack per altre lingue. Le impostazioni locali del contenuto identificano l'identificatore LCID per il linguaggio con cui gli utenti immetteranno la query di ricerca in, mentre le impostazioni locali della parola chiave identificano il LCID utilizzato dal motore di ricerca durante l'analisi delle parole chiave AQS (Advanced Query Syntax).

Ad esempio, se si dispone della versione inglese (Stati Uniti) senza MUI Pack, le impostazioni locali del contenuto e le impostazioni locali della parola chiave sono 1033. Se si dispone della versione tedesca senza MUI Pack, le impostazioni locali del contenuto e le impostazioni locali della parola chiave sono 1031 (gr-gr). Tuttavia, se si dispone della versione in lingua inglese con MUI Pack Romeno, le impostazioni locali del contenuto sono 2072 (RO) e la parola chiave locale è 1033 (en-US).

## <a name="working-with-properties-and-columns"></a>Utilizzo di proprietà e colonne



| Metodi                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: Get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Ottiene o imposta le proprietà di contenuto per la ricerca (colonna della proprietà elencata nelle clausole CONTAINs o FREETEXT).                                   |
| [**ISearchQueryHelper:: Get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper::p UT \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Ottiene o imposta le colonne (o proprietà) richieste nell'istruzione SELECT. Il valore predefinito è System. ItemUrl e le proprietà utilizzate nella clausola WHERE. |



 

Gli elementi sono rappresentati nell'archivio delle proprietà come riga. Ogni riga contiene un numero di colonne che rappresentano le proprietà di tale elemento. Non tutti gli elementi avranno un valore per una determinata proprietà. Un file audio, ad esempio, in genere non contiene un valore per la proprietà System. Property. FromName, ma può contenere informazioni relative a System. Music. Artist.

Con questi metodi, è possibile accedere o modificare la proprietà con una stringa Unicode delimitata da virgole, con terminazione null, che specifica uno o più nomi di colonna dell'archivio delle proprietà: "System.Document. Autore, System.Document. Titolo ".

## <a name="working-with-query-term-expansion"></a>Utilizzo dell'espansione del termine di query



| Metodi                                                                                                                                                                                                                                 | Descrizione                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper:: Get \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper::p UT \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Ottiene o imposta il flag di espansione del termine di ricerca. |



 

Questo metodo consente l'espansione di alcuni termini di query con caratteri jolly, in modo analogo all'espansione delle espressioni regolari. L'espansione del prefisso Cerca parole con lo stesso prefisso (Fun/imbuto). Se non è impostato, il valore predefinito è il prefisso del termine di ricerca \_ \_ \_ all. I valori supportati dell'enumerazione [**di \_ \_ espansione del termine di ricerca**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) sono i seguenti:

-   \_Tutti i \_ termini di ricerca del prefisso del termine \_ di ricerca sono espansi
-   \_ \_ \_ Termini di ricerca senza espansione-nessun termine di ricerca espanso

## <a name="working-with-other-isearchqueryhelper-methods"></a>Utilizzo di altri metodi di ISearchQueryHelper

Molti dei metodi nell'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) vengono usati per impostare gli argomenti della query o definire le proprietà restituite.



| Metodi                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Restituisce la stringa di connessione OLE DB. Si tratta del metodo preferito per ottenere una stringa di connessione correttamente formattata e corretta.                                  |
| [**ISearchQueryHelper:: Get \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper::p UT \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Ottiene o imposta il numero massimo di risultati che devono essere restituiti da una query, ovvero SELECT TOP n. Il valore predefinito è-1, ovvero non viene generata alcuna clausola di risultati massima. |
| [**ISearchQueryHelper:: Get \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper::p UT \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Ottiene o imposta l'ordinamento per il set di risultati della query (ORDER BY). Se non esiste alcuna clausola ORDER BY, i risultati vengono restituiti in ordine non deterministico.                   |
| [**ISearchQueryHelper:: Get \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper::p UT \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Ottiene o imposta la sintassi della query: sintassi di query avanzata o sintassi di query naturale.                                                                                  |
| [**ISearchQueryHelper:: Get \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Ottiene o imposta le restrizioni accodate tramite le clausole WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




