---
title: Enumerazione delle repliche di un servizio
description: Questo argomento include un esempio di codice che enumera le istanze installate di un servizio replicato in computer host diversi in un'organizzazione.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995cd665476a55b6bf717f356fafa54b0d2e10e6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104516708"
---
# <a name="enumerating-the-replicas-of-a-service"></a><span data-ttu-id="f0939-103">Enumerazione delle repliche di un servizio</span><span class="sxs-lookup"><span data-stu-id="f0939-103">Enumerating the Replicas of a Service</span></span>

<span data-ttu-id="f0939-104">Questo argomento include un esempio di codice che enumera le istanze installate di un servizio replicato in computer host diversi in un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0939-104">This topic includes a code example that enumerates the installed instances of a replicated service on different host computers throughout an enterprise.</span></span> <span data-ttu-id="f0939-105">Per modificare la password dell'account del servizio per ogni istanza di un servizio replicato, usare questo esempio di codice insieme all'esempio di codice nell'argomento [modifica della password per l'account utente di un servizio](changing-the-password-on-a-serviceampaposs-user-account.md) .</span><span class="sxs-lookup"><span data-stu-id="f0939-105">To change the service account password for each instance of a replicated service, use this code example in conjunction with the code example in the [Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md) topic.</span></span>

<span data-ttu-id="f0939-106">Nell'esempio di codice si presuppone che ogni istanza del servizio disponga di un proprio oggetto SCP (Service Connection Point) nella directory.</span><span class="sxs-lookup"><span data-stu-id="f0939-106">The code example assumes that each service instance has its own service connection point (SCP) object in the directory.</span></span> <span data-ttu-id="f0939-107">Un SCP è un oggetto della classe [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="f0939-107">An SCP is an object of the [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) class.</span></span> <span data-ttu-id="f0939-108">Questa classe dispone di un attributo **Keywords** , ovvero un attributo multivalore replicato in ogni catalogo globale (GC) nell'insieme di strutture.</span><span class="sxs-lookup"><span data-stu-id="f0939-108">This class has a **keywords** attribute, which is a multi-valued attribute replicated to each global catalog (GC) in the forest.</span></span> <span data-ttu-id="f0939-109">L'attributo **Keywords** dell'SCP di ogni istanza contiene il GUID del prodotto del servizio.</span><span class="sxs-lookup"><span data-stu-id="f0939-109">The **keywords** attribute of each instance's SCP contains the service's product GUID.</span></span> <span data-ttu-id="f0939-110">Ciò consente di trovare tutti i convergenza per le varie istanze del servizio eseguendo una ricerca in un GC per gli oggetti con un attributo **Keywords** che equivale al GUID del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f0939-110">This enables finding all of the SCPs for the various service instances by searching a GC for objects with a **keywords** attribute that equals the product GUID.</span></span>

<span data-ttu-id="f0939-111">Nell'esempio di codice viene ottenuto un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) a un GC e viene utilizzato il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) per cercare convergenza.</span><span class="sxs-lookup"><span data-stu-id="f0939-111">The code example obtains an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to a GC, and uses the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) method to search for the SCPs.</span></span> <span data-ttu-id="f0939-112">Tenere presente che il GC contiene una replica parziale per ogni SCP.</span><span class="sxs-lookup"><span data-stu-id="f0939-112">Be aware that the GC contains a partial replica for each SCP.</span></span> <span data-ttu-id="f0939-113">Ovvero, contiene alcuni degli attributi SCP, ma non tutti.</span><span class="sxs-lookup"><span data-stu-id="f0939-113">That is, it contains some of the SCP attributes, but not all.</span></span> <span data-ttu-id="f0939-114">In questo esempio di codice, concentrarsi sull'attributo **serviceDNSName** , che contiene il nome DNS del server host per l'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="f0939-114">In this code example, focus on the **serviceDNSName** attribute, which contains the DNS name of the host server for that service instance.</span></span> <span data-ttu-id="f0939-115">Poiché **serviceDNSName** non è uno degli attributi replicati in un catalogo globale, nell'esempio di codice viene usato un processo in due passaggi per recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="f0939-115">Because **serviceDNSName** is not one of the attributes replicated in a GC, the code example uses a two-step process to retrieve it.</span></span> <span data-ttu-id="f0939-116">In primo luogo, usa la ricerca GC per ottenere il nome distinto (DN) del SCP, quindi usa tale DN per eseguire il binding direttamente al SCP per recuperare la proprietà **serviceDNSName** .</span><span class="sxs-lookup"><span data-stu-id="f0939-116">First, it uses the GC search to get the distinguished name (DN) of the SCP, then it uses that DN to bind directly to the SCP to retrieve the **serviceDNSName** property.</span></span>


```C++
HRESULT EnumerateServiceInstances(
       LPWSTR szQuery,                // Search string filter.
       LPWSTR *pszAttribs,            // An array of attributes 
                                      // to retrieve.
       DWORD dwAttribs,               // # of attributes requested.
       DWORD *pdwAttribs,             // # of attributes retrieved.
       ADS_ATTR_INFO **ppPropEntries  // Returns a pointer to the 
                                      // retrieved attributes.
        )
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
BSTR  bstrPath = NULL;
ULONG lFetch;
IADs *pADs = NULL;
int iRows=0;
static IDirectorySearch *pSearch = NULL;
static ADS_SEARCH_HANDLE hSearch = NULL;

// Parameters for IDirectoryObject.
IDirectoryObject *pSCP = NULL;
 
// Structures and parameters for IDirectorySearch.
DWORD               dwPref;
ADS_SEARCH_COLUMN   Col;
ADS_SEARCHPREF_INFO SearchPref[2];
 
// First time through; set up the search.
if (pSearch == NULL) 
{
    // Bind to the GC: namespace container object. The GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained through enumeration.
    hr = ADsGetObject(L"GC:", 
        IID_IADsContainer, 
        (void**) &pCont );
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsGetObject(GC) failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Obtain an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont,&pEnum);
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum,1,&var,&lFetch);
    if (( hr == S_OK ) && ( lFetch == 1 ) ) 
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IADs, (void**)&pADs);
        if (hr == S_OK) 
            hr = pADs->get_ADsPath(&bstrPath);
    }
    if (FAILED(hr)) {
        _tprintf(TEXT("Enumeration failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Now bstrPath contains the ADsPath for the current GC.  
    // Bind the GC to get the search interface.
    hr = ADsGetObject(bstrPath, 
                      IID_IDirectorySearch, 
                      (void**)&pSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("Failed to bind search root: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Set up a deep search.
    // Thousands of objects are not expected
    // in this example; request 1000 rows per page.
    dwPref=sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;
 
    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;
 
    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    if (FAILED(hr))    {
        _tprintf(TEXT("Failed to set search prefs: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Execute the search. From the GC, get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    hr = pSearch->ExecuteSearch(szQuery, pszAttribs, 1, &hSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("ExecuteSearch failed: 0x%x\n"), hr);
        goto Cleanup;
    } 
}
 
// Get the next row.
hr = pSearch->GetNextRow(hSearch);
 
// Process the row.
if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
{
    // Get the distinguished name of the object in this row.
    hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
    if FAILED(hr) { 
        _tprintf(TEXT("GetColumn failed: 0x%x\n"), hr);
        goto Cleanup;
    }
    // Bind to the DN to get the properties.
    if (Col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
    {
        LPWSTR szSCPPath = 
          new WCHAR[7 + lstrlenW(Col.pADsValues->CaseIgnoreString) + 1];
        wcscpy_s(szSCPPath, L"LDAP://");
        wcscat_s(szSCPPath, Col.pADsValues->CaseIgnoreString);
        hr = ADsGetObject(szSCPPath, 
                          IID_IDirectoryObject,
                          (void**)&pSCP);
        delete szSCPPath;
        if (SUCCEEDED(hr)) 
        {
            hr = pSCP->GetObjectAttributes(pszAttribs, dwAttribs,
                          ppPropEntries, pdwAttribs);
            if(FAILED(hr)) {
                _tprintf(TEXT("GetObjectAttributes Failed."), hr);
                goto Cleanup;
            }
        }
    }
    pSearch->FreeColumn(&Col);}
 
Cleanup:
if (bstrPath)
    SysFreeString(bstrPath);
if (pSCP) 
    pSCP->Release();
if (pCont) 
    pCont->Release();
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pADs) 
    pADs->Release();
if (pDisp)
    pDisp->Release();
 
return hr;
 
}
```



 

 