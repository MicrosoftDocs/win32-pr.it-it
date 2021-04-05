---
title: Codice di esempio per la ricerca in una foresta
description: Questo argomento contiene codice di esempio che cerca una foresta.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, ricerca in una foresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c2fb0cde0f42167b19141ad178ea80ff8795b8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724527"
---
# <a name="example-code-for-searching-a-forest"></a><span data-ttu-id="9096a-104">Codice di esempio per la ricerca in una foresta</span><span class="sxs-lookup"><span data-stu-id="9096a-104">Example Code for Searching a Forest</span></span>

<span data-ttu-id="9096a-105">Questo argomento contiene codice di esempio che cerca una foresta.</span><span class="sxs-lookup"><span data-stu-id="9096a-105">This topic contains example code that searches a forest.</span></span>

<span data-ttu-id="9096a-106">Il seguente esempio di codice C/C++ viene associato alla radice del catalogo globale ed enumera il singolo oggetto, ovvero la radice della foresta, in modo che possa essere utilizzato per cercare l'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="9096a-106">The following C/C++ code example binds to the root of the Global Catalog and enumerates the single object, which is the root of the forest, so that it can be used to search the entire forest.</span></span>


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



<span data-ttu-id="9096a-107">Nell'esempio di codice C/C++ riportato di seguito è contenuta una funzione che restituisce un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) utilizzato per eseguire la ricerca nell'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="9096a-107">The following C/C++ code example contains a function that returns an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer used to search the entire forest.</span></span>

<span data-ttu-id="9096a-108">La funzione esegue un'associazione senza server alla radice del catalogo globale, enumera il singolo elemento, che è la radice della foresta e può essere usato per cercare l'intera foresta, chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) all'oggetto e restituisce tale puntatore per l'uso da parte del chiamante per la ricerca nella foresta.</span><span class="sxs-lookup"><span data-stu-id="9096a-108">The function performs a serverless bind to the root of the Global Catalog, enumerates the single item, which is the root of the forest and can be used to search the entire forest, calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to the object, and returns that pointer for use by the caller to search the forest.</span></span>


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 