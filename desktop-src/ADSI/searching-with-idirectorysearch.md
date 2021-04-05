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
# <a name="searching-with-the-idirectorysearch-interface"></a>Ricerca con l'interfaccia IDirectorySearch

L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce un'interfaccia di alto livello e di basso overhead per l'esecuzione di query sui dati di una directory o di un catalogo globale. L'interfaccia com **IDirectorySearch** può essere utilizzata solo con un oggetto vtable e pertanto non è disponibile per gli ambienti di sviluppo basati su automazione.

**Per eseguire una ricerca**

1.  Eseguire l'associazione a un oggetto nella directory.
2.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere il puntatore [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .
3.  Eseguire la ricerca usando il puntatore [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Chiamare il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passare un filtro di ricerca, i nomi di attributo richiesti e altri parametri.

Per ulteriori informazioni sulla sintassi del filtro di ricerca, vedere la [sintassi del filtro di ricerca](search-filter-syntax.md).

L'esecuzione della query è specifica del provider. Con alcuni provider, l'esecuzione effettiva della query non viene eseguita fino a quando non viene chiamato [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) . L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funziona direttamente con i filtri di ricerca. Non sono richiesti né il dialetto SQL né il dialetto LDAP.

L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce metodi per enumerare il set di risultati, riga per riga. Il metodo [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la prima riga e [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) passa alla riga successiva dalla riga corrente. Una volta raggiunta l'ultima riga, la chiamata a questi metodi restituisce il codice di errore per le \_ \_ \_ righe. Viceversa, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) sposta indietro una riga alla volta. Una S \_ Ads \_ nomore \_ Rows valore restituito indica che è stata raggiunta la prima riga del set di risultati. Questi metodi operano sul set di risultati, residente in memoria, nel client. Pertanto, quando vengono eseguite le ricerche di paging e asincrone e l' \_ opzione relativa ai risultati della cache è disattivata \_ , lo scorrimento a ritroso può avere conseguenze impreviste.

Dopo aver individuato la riga appropriata, chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per ottenere gli elementi di dati, column by column. Per ogni chiamata si passa il nome della colonna di interesse. L'elemento dati restituito è un puntatore a una struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) . **GetColumn** alloca questa struttura per l'utente, ma è necessario liberarla usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Chiamare [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) per completare l'operazione di ricerca.

**Per eseguire una ricerca nella directory**

1.  Eseguire l'associazione a un provider LDAP. Può essere un controller di dominio o un provider del catalogo globale.
2.  Recuperare l'interfaccia com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una chiamata a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Questa operazione potrebbe essere stata eseguita nel passaggio 1 durante l'associazione iniziale.

    Facoltativamente, chiamare [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) per selezionare le opzioni per la gestione dei risultati della ricerca.

3.  Chiamare [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). A seconda delle opzioni impostate in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , è possibile che venga avviata l'esecuzione della query.
4.  Chiamare [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) per spostare l'indice di riga (interno a [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) nella prima riga.
5.  Leggere i dati dalla riga tramite [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), quindi chiamare [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) per rilasciare la memoria allocata da **GetColumn**.
6.  Ripetere il passaggio 5 fino a quando non vengono recuperati tutti i dati dal risultato della ricerca o fino a quando [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) non restituisce \_ \_ più righe per ADS \_ .
7.  Chiamare [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) al termine dell'operazione.

Nell'esempio di codice riportato di seguito viene illustrato questo scenario. Per avviare l'associazione a ADSI, chiamare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


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



In questo modo viene fornito un puntatore all'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Ora che è disponibile un'interfaccia COM per un'istanza di IDirectoryInterface, chiamare [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Compilare una matrice di nomi di attributo per preparare la chiamata della funzione [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . I nomi degli attributi vengono definiti all'interno dello schema di Active Directory. Per ulteriori informazioni sulla definizione dello schema, vedere [ADSI schema Model](adsi-schema-model.md). I nomi degli attributi elencati vengono restituiti, se supportati dall'oggetto, come set di risultati della ricerca.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



A questo punto, chiamare la funzione [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . La ricerca non viene eseguita fino a quando non si chiama il metodo [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Chiamare [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) per eseguire l'iterazione delle righe nel risultato. Ogni riga viene quindi sottoposta a query per l'attributo "Description". Se l'attributo viene trovato, viene visualizzato.


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



Per terminare la ricerca, chiamare il metodo [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .

Tenere presente che, se le dimensioni della pagina non sono impostate, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) si blocca fino a quando non viene restituito al client l'intero set di risultati. Se viene impostata la dimensione di pagina, **GetNextRow** si blocca fino a quando non viene restituita la prima pagina (dimensione pagina = numero di righe in una pagina). Se le dimensioni della pagina sono impostate e la query deve essere ordinata e non si sta eseguendo la ricerca in almeno un attributo indicizzato, il valore delle dimensioni della pagina viene ignorato e il server calcola l'intero set di risultati prima di restituire i dati. Questa operazione ha effetto del blocco **GetNextRow** fino al completamento della query.

> [!Note]  
> Per modificare questa query da una ricerca di directory a una ricerca nel catalogo globale, viene modificata la chiamata [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 