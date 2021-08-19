---
title: Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli
description: Le interfacce IDirectoryObject o IDirectorySearch possono essere usate per recuperare un intervallo di valori di proprietà. A tale scopo, specificare l'attributo e l'intervallo per uno degli attributi richiesti nella query.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI , Uso per il recupero di membri di un gruppo
- IDirectoryObject ADSI , Uso per il recupero di membri di un gruppo
- Recupero di intervalli ADSI tramite IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d061dd49c98bdb3b8cc731a28d0dc0ee5fe9a0df5816abf259ece17e456ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023059"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli

Le [**interfacce IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) o [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) possono essere usate per recuperare un intervallo di valori di proprietà. A tale scopo, specificare l'attributo e l'intervallo per uno degli attributi richiesti nella query.

## <a name="range-retrieval-with-idirectoryobject"></a>Recupero di intervalli con IDirectoryObject

[**L'interfaccia IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi nella matrice *pAttributesName* quando si chiama il metodo [**IDirectoryObject::GetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Per altre informazioni e un esempio di codice che illustra come usare [**l'interfaccia IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per il recupero di intervalli, vedere Codice di esempio per [ranging con IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recupero di intervalli con IDirectorySearch

[**L'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi recuperati nella matrice *pAttributesName* quando si chiama il metodo [**IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Quando si usa [**l'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero dell'intervallo, esiste un problema che deve essere risolto in modo specifico. Quando l'intervallo richiesto supera il numero di valori rimanenti, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) restituirà **E \_ ADS \_ COLUMN NOT \_ \_ SET**. Per recuperare i valori rimanenti, è necessario usare il carattere jolly dell'intervallo ' \* '. Ad esempio, se un gruppo contiene 150 membri, i valori dei membri da 0 a 100 possono essere recuperati normalmente usando il recupero a intervalli. Se viene richiesto l'intervallo 101-200, **IDirectorySearch::GetColumn** restituirà **E \_ ADS \_ COLUMN NOT \_ \_ SET**. Questo problema può essere evitato usando il [**metodo IDirectorySearch::GetNextColumnName.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) In **genere, GetNextColumnName** restituirà la stringa di query originale. Tuttavia, quando l'intervallo richiesto supera il numero di valori rimanenti, **GetNextColumnName** restituirà una versione modificata della stringa di query sostituendo il valore di intervallo elevato con il carattere jolly dell'intervallo ' \* '. Nell'esempio precedente la prima query verrà eseguita con una stringa di attributo "member;range=0-100" e **GetNextColumnName** restituirà "member;range=0-100". Nella seconda query la stringa dell'attributo sarà "member;range=101-200", ma **GetNextColumnName** restituirà "member;range=101- \* ". Questo caso può essere determinato confrontando la stringa dell'attributo originale con il risultato di **GetNextColumnName**. Se le stringhe sono diverse, l'ultimo blocco di valori deve essere nuovamente richiesto con il carattere jolly dell'intervallo.

Per altre informazioni e un esempio di codice che illustra come usare [**l'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero di intervalli, vedere Codice di esempio per [ranging con IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




