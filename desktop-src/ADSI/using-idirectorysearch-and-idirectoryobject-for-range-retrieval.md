---
title: Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli
description: Le interfacce IDirectoryObject o IDirectorySearch possono essere utilizzate per recuperare un intervallo di valori di proprietà. A tale scopo, specificare l'attributo e l'intervallo per uno degli attributi richiesti nella query.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, utilizzo di per il recupero dei membri di un gruppo
- IDirectoryObject ADSI, utilizzo di per il recupero dei membri di un gruppo
- Recupero intervallo ADSI, uso di IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297639"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli

Le interfacce [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) o [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) possono essere utilizzate per recuperare un intervallo di valori di proprietà. A tale scopo, specificare l'attributo e l'intervallo per uno degli attributi richiesti nella query.

## <a name="range-retrieval-with-idirectoryobject"></a>Recupero di intervalli con IDirectoryObject

L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi nella matrice *pAttributesName* quando si chiama il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Per ulteriori informazioni e un esempio di codice in cui viene illustrato come utilizzare l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per il recupero di intervalli, vedere il [codice di esempio per la variabile con IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recupero di intervalli con IDirectorySearch

L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi recuperati nella matrice *pAttributesName* quando si chiama il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Quando si usa l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero di intervalli, è necessario risolvere un problema specifico. Quando l'intervallo richiesto supera il numero di valori rimanenti, [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) restituirà la **\_ colonna E Ads \_ \_ non \_ impostata**. Per recuperare i valori rimanenti, è necessario usare il carattere jolly di intervallo ' \* '. Se, ad esempio, un gruppo contiene 150 membri, è possibile recuperare i valori dei membri 0-100 normalmente utilizzando il recupero con intervallo. Se viene richiesto l'intervallo 101-200, **IDirectorySearch:: GetColumn** restituirà **E \_ la \_ colonna Ads \_ non è \_ impostata**. Questo problema può essere evitato usando il metodo [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) . In genere, **GetNextColumnName** restituirà la stringa di query originale. Tuttavia, quando l'intervallo richiesto supera il numero di valori rimanenti, **GetNextColumnName** restituirà una versione modificata della stringa di query sostituendo il valore di intervallo massimo con il carattere jolly di intervallo ' \* '. Nell'esempio precedente, la prima query verrebbe eseguita con una stringa di attributo "member; range = 0-100" e **GetNextColumnName** restituirà "member; range = 0-100". Nella seconda query, la stringa dell'attributo sarà "member; range = 101-200", ma **GetNextColumnName** restituirà "member; range = 101- \* ". Questo caso può essere determinato confrontando la stringa dell'attributo originale con il risultato di **GetNextColumnName**. Se le stringhe sono diverse, l'ultimo blocco di valori deve essere nuovamente richiesto con il carattere jolly di intervallo.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come utilizzare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero di intervalli, vedere il [codice di esempio per la variabile con IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




