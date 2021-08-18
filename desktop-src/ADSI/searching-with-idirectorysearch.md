---
title: Ricerca con l'interfaccia IDirectorySearch
description: L'interfaccia IDirectorySearch offre un'interfaccia di alto livello e a basso sovraccarico per l'esecuzione di query sui dati di una directory o di un catalogo globale.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Ricerca con l'interfaccia IDirectorySearch ADSI
- Esegue query su ADSI, interfacce di query, IDirectorySearch
- ADSI ADSI , Codice di esempio C/C++, Ricerca di una directory con IDirectorySearch
- IDirectorySearch ADSI , uso per la ricerca in una directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46700c48f82955bd01967808cd30f2fa078e3b6c998fb3beaac4bf7c7fe8707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023219"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Ricerca con l'interfaccia IDirectorySearch

[**L'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) offre un'interfaccia di alto livello e a basso sovraccarico per l'esecuzione di query sui dati di una directory o di un catalogo globale. L'interfaccia COM **IDirectorySearch** può essere usata solo con una tabella vtable e pertanto non è disponibile per gli ambienti di sviluppo basati su Automazione.

**Per eseguire una ricerca**

1.  Eseguire l'associazione a un oggetto nella directory.
2.  Chiamare [**QueryInterface per**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ottenere il [**puntatore IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
3.  Eseguire la ricerca usando il [**puntatore IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Chiamare il [**metodo IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passare un filtro di ricerca, i nomi degli attributi richiesti e altri parametri.

Per altre informazioni sulla sintassi del filtro di ricerca, vedere [Sintassi del filtro di ricerca](search-filter-syntax.md).

L'esecuzione di query è specifica del provider. Con alcuni provider, l'esecuzione effettiva della query non viene eseguita fino a quando non viene chiamato [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) [**L'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funziona direttamente con i filtri di ricerca. Né il SQL né il dialetto LDAP sono necessari.

[**L'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce metodi per enumerare il set di risultati, riga per riga. Il [**metodo IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la prima riga e [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) sposta l'utente alla riga successiva dalla riga corrente. Dopo aver raggiunto l'ultima riga, la chiamata di questi metodi restituisce il codice di errore S \_ ADS \_ NOMORE \_ ROWS. Al contrario, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) consente di tornare indietro di una riga alla volta. Un valore restituito S ADS NOMORE ROWS indica che è stata raggiunta \_ la prima riga del set di \_ \_ risultati. Questi metodi operano sul set di risultati, residente in memoria, nel client. Pertanto, quando vengono eseguite ricerche di pagine e asincrone e l'opzione CACHE RESULTS è disattivata, lo scorrimento all'indietro \_ \_ può avere conseguenze impreviste.

Dopo aver individuato la riga appropriata, chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per ottenere gli elementi di dati, colonna per colonna. Per ogni chiamata si passa il nome della colonna di interesse. L'elemento di dati restituito è un puntatore a [**una struttura ADS \_ SEARCH \_ COLUMN.**](/windows/desktop/api/Iads/ns-iads-ads_search_column) **GetColumn** alloca automaticamente questa struttura, ma è necessario liberarla usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Chiamare [**CloseSearchHandle per**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) completare l'operazione di ricerca.

**Per eseguire una ricerca nella directory**

1.  Eseguire l'associazione a un provider LDAP. Può essere un controller di dominio o un provider di catalogo globale.
2.  Recuperare [**l'interfaccia COM IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una chiamata a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Questa operazione potrebbe essere stata eseguita nel passaggio 1 durante l'associazione iniziale.

    Facoltativamente, chiamare [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) per selezionare le opzioni per la gestione dei risultati della ricerca.

3.  Chiamare [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). A seconda delle opzioni impostate in [**SetSearchPreference,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) l'esecuzione della query può essere avviata o meno.
4.  Chiamare [**GetNextRow per**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) spostare l'indice di riga (interno a [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) nella prima riga.
5.  Leggere i dati dalla riga usando [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), quindi chiamare [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) per rilasciare la memoria allocata da **GetColumn**.
6.  Ripetere il passaggio 5 finché tutti i dati non vengono recuperati dal risultato della ricerca o finché [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) non restituisce S \_ ADS \_ NOMORE \_ ROWS.
7.  Chiamare [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) al termine.

L'esempio di codice seguente illustra questo scenario. Per avviare l'associazione ad ADSI, chiamare la [**funzione ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)


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



Fornisce un puntatore [**all'interfaccia IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Ora che è disponibile un'interfaccia COM per un'istanza di IDirectoryInterface, chiamare [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Compilare una matrice di nomi di attributi per preparare la chiamata alla [**funzione IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) I nomi degli attributi sono definiti all'interno dello schema di Active Directory. Per altre informazioni sulla definizione dello schema, vedere [Modello di schema ADSI](adsi-schema-model.md). I nomi degli attributi elencati vengono restituiti, se supportati dall'oggetto , come set di risultati della ricerca.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Chiamare ora la [**funzione ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) La ricerca non viene eseguita fino a quando non si chiama il [**metodo GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Chiamare [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) per scorrere le righe nel risultato. A ogni riga viene quindi eseguita una query per l'attributo "description". Se l'attributo viene trovato, viene visualizzato.


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



Per terminare la ricerca, chiamare il [**metodo AbandonSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch)

Tenere presente che se le dimensioni della pagina non sono impostate, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) si blocca fino a quando l'intero set di risultati non viene restituito al client. Se le dimensioni della pagina sono impostate, **GetNextRow** si blocca fino a quando non viene restituita la prima pagina (dimensioni pagina = numero di righe in una pagina). Se le dimensioni della pagina sono impostate e la query deve essere ordinata e non si esegue la ricerca in almeno un attributo indicizzato, il valore delle dimensioni della pagina viene ignorato e il server calcola l'intero set di risultati prima di restituire i dati. Ciò ha effetto sul blocco **di GetNextRow** fino al completamento della query.

> [!Note]  
> Per modificare questa query da una ricerca di directory a una ricerca nel catalogo globale, la [**chiamata ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) viene modificata.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 