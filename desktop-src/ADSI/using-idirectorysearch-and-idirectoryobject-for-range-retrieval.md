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
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="71684-107">Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli</span><span class="sxs-lookup"><span data-stu-id="71684-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="71684-108">Le interfacce [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) o [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) possono essere utilizzate per recuperare un intervallo di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="71684-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="71684-109">A tale scopo, specificare l'attributo e l'intervallo per uno degli attributi richiesti nella query.</span><span class="sxs-lookup"><span data-stu-id="71684-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="71684-110">Recupero di intervalli con IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="71684-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="71684-111">L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi nella matrice *pAttributesName* quando si chiama il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="71684-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="71684-112">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come utilizzare l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per il recupero di intervalli, vedere il [codice di esempio per la variabile con IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="71684-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="71684-113">Recupero di intervalli con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="71684-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="71684-114">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) può essere usata per il recupero dell'intervallo specificando l'attributo e l'intervallo per uno degli attributi recuperati nella matrice *pAttributesName* quando si chiama il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="71684-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="71684-115">Quando si usa l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero di intervalli, è necessario risolvere un problema specifico.</span><span class="sxs-lookup"><span data-stu-id="71684-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="71684-116">Quando l'intervallo richiesto supera il numero di valori rimanenti, [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) restituirà la **\_ colonna E Ads \_ \_ non \_ impostata**.</span><span class="sxs-lookup"><span data-stu-id="71684-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="71684-117">Per recuperare i valori rimanenti, è necessario usare il carattere jolly di intervallo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="71684-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="71684-118">Se, ad esempio, un gruppo contiene 150 membri, è possibile recuperare i valori dei membri 0-100 normalmente utilizzando il recupero con intervallo.</span><span class="sxs-lookup"><span data-stu-id="71684-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="71684-119">Se viene richiesto l'intervallo 101-200, **IDirectorySearch:: GetColumn** restituirà **E \_ la \_ colonna Ads \_ non è \_ impostata**.</span><span class="sxs-lookup"><span data-stu-id="71684-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="71684-120">Questo problema può essere evitato usando il metodo [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) .</span><span class="sxs-lookup"><span data-stu-id="71684-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="71684-121">In genere, **GetNextColumnName** restituirà la stringa di query originale.</span><span class="sxs-lookup"><span data-stu-id="71684-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="71684-122">Tuttavia, quando l'intervallo richiesto supera il numero di valori rimanenti, **GetNextColumnName** restituirà una versione modificata della stringa di query sostituendo il valore di intervallo massimo con il carattere jolly di intervallo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="71684-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="71684-123">Nell'esempio precedente, la prima query verrebbe eseguita con una stringa di attributo "member; range = 0-100" e **GetNextColumnName** restituirà "member; range = 0-100".</span><span class="sxs-lookup"><span data-stu-id="71684-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="71684-124">Nella seconda query, la stringa dell'attributo sarà "member; range = 101-200", ma **GetNextColumnName** restituirà "member; range = 101- \* ".</span><span class="sxs-lookup"><span data-stu-id="71684-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="71684-125">Questo caso può essere determinato confrontando la stringa dell'attributo originale con il risultato di **GetNextColumnName**.</span><span class="sxs-lookup"><span data-stu-id="71684-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="71684-126">Se le stringhe sono diverse, l'ultimo blocco di valori deve essere nuovamente richiesto con il carattere jolly di intervallo.</span><span class="sxs-lookup"><span data-stu-id="71684-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="71684-127">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come utilizzare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per il recupero di intervalli, vedere il [codice di esempio per la variabile con IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="71684-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




